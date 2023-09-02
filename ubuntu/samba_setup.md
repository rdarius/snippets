# SAMBA

## Install Samba

```sh
sudo apt update
sudo apt install samba
```

## Update Samba Config

```sh
sudo nano /etc/samba/smb.conf
```

Add at the bottom [example]
```
[share_name]
    comment = Samba Share Name
    path = /location/of/directory/shared
    read only = no
    browsable = yes
```

Restart samba service to apply changes
```sh
sudo service smbd restart
```

## Add samba used to access the content

```sh
smbpasswd -a samba_user
```

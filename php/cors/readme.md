
# Allow requests from external origins

### Allowing requests from any origin
```injectablephp
header('Access-Control-Allow-Origin: *');
```

### Allow requests from specific origins

```injectablephp
header('Access-Control-Allow-Origin: *');
```


## Other useful options

### Allow credentials ( description TBD )
```injectablephp
header("Access-Control-Allow-Credentials: true");
```

### Allow only specific call methods

Select methods you will be using separated by comma

`OPTIONS` method is recommended to be added as browsers usually send OPTIONS
request before sending actual request to the backed 

```injectablephp
header('Access-Control-Allow-Methods: GET, PUT, POST, DELETE, OPTIONS');
```

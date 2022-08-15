
# Allow requests from external origins

### Allowing requests from any origin
```injectablephp
header('Access-Control-Allow-Origin: *');
```

### Allow requests from specific origins

to enable cors for multiple origins you should do a check on PHP
side if origin is in the list, then enable cors on that request
to allow that specific origin
```injectablephp
$allowOrigins = [
  'https://example.com',
  'https://api.example.com'
];
if (in_array($_SERVER['HTTP_ORIGIN'], $allowOrigins)) {
  header('Access-Control-Allow-Origin: ' . $_SERVER['HTTP_ORIGIN']);
}
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

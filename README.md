links
-------------

## Documentations

* [Backbone.js Chinese Documentation](https://www.css88.com/doc/backbone/#Model-escape)
* [Under score](https://underscorejs.org/#template)

## Interesting Sites

* [Preloaders For Git generation](https://icons8.com/preloaders/)

## Interesting Code Pieces


### Close the connection and run in background.###

It tells the client to close the connection. It works fine on httpd && chrome.

```php

ob_start();
echo "Backgrounding...";

// get the size of the output
$size = ob_get_length();

// send headers to tell the browser to close the connection
header("Content-Length: $size");
header('Connection: close');

// close current session
if (session_id()) session_write_close();

// flush all output
ob_end_flush();
ob_flush();
flush();

```

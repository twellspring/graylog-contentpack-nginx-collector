# Graylog content pack for nginx using gelf input from Graylog Collectors.  

This content pack creates a GELF Input for use by the graylog-collector.  Extractors are applied to all received messages to extract nginx access log fields and error log severity. Extracted fields are prefixed by http_. Graylog timestamp is set to the timestamp in the access/error log.  The extractors are configured for combined log format, so other applications using combined log format should also be matched by these extractors ( apache, node.js/morgan).

The graylog collector needs to be installed on your web servers.  See collector.conf.EXAMPLE for a sample configuration to collect nginx logs from /var/log/nginx and send them to the GELF input on graylog server.


![Screenshots](https://github.com/twellspring/graylog-contentpack-nginx-collector/blob/master/images/screenshot_gelf_12201_collector.png)

![Screenshots](https://github.com/twellspring/graylog-contentpack-nginx-collector/blob/master/images/screenshot_extractors.png)

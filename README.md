<!--
 * @Author: Xiuxu Jin(jyxk)
 * @Date: 2019-10-10 11:54:55
 * @LastEditors: Xiuxu Jin
 * @LastEditTime: 2019-10-10 21:25:07
 * @Description: file content
 * @Email: jyxking007@gmail.com
 -->
[juson]: https://github.com/wgtdkp/juson
[nginx]: https://nginx.org/
[lighttpd]: https://www.lighttpd.net/

## Environment

* gcc 9.2.0
* linux 5.3.5

## Dependency

* _[juson]_

## Install

```shell
  $ cd src && make all
  # make install 
```

## Run

```shell
$ sudo mginx # default listening at 8000
```

You may modify the config file to specify the port if there is a confliction.

## Debug

As julia run as a daemon, it is not convenient to debug.
Follow the steps to make it run in debug mode:

1. change the _INSTALL\_DIR_ in Makefile to your local repo, like:
  ```shell
  INSTALL_DIR = /home/foo/mginx/ # the last slash required
  ```

2. turn on the _debug_ instruction in config.json
  ```json
  "debug": true,
  ```

## Todo

1. ~~fastcgi~~
2. chunked transform
3. benchmark

## Reference

1. _[nginx]_
2. _[lighttpd]_
3. _[juson]_

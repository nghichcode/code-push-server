# CodePush Server ![Node.js CI](https://github.com/shm-open/code-push-server/workflows/Node.js%20CI/badge.svg)

CodePush Server is a CodePush program server. The official Microsoft CodePush service is slow in China, therefore we use this to host our own server.

## Support Storage mode

-   local: store bundle files in local machine
-   qiniu: store bundle files in [qiniu](http://www.qiniu.com/)
-   s3: store bundle files in [aws](https://aws.amazon.com/)
-   oss: store bundle files in [aliyun](https://www.aliyun.com/product/oss)
-   tencentcloud: store bundle files in [tencentcloud](https://cloud.tencent.com/product/cos)


### CodePush Cli

check out the [code-push-cli](https://github.com/shm-open/code-push-cli) which works with server for manage apps and publish releases

### Clients

-   [React Native](https://github.com/Microsoft/react-native-code-push)
-   [Cordova](https://github.com/microsoft/cordova-plugin-code-push)
-   [Capacitor](https://github.com/mapiacompany/capacitor-codepush)

## How To Install code-push-server

-   [docker](./docs/install-server-by-docker.md) (recommended)
-   [manual operation](./docs/install-server.md)

### Quick guide
#### Init Database (your database must not exits)
```shell
$ yarn run init --dbhost "mysql_host" --dbport "mysql_port"  --dbuser "mysql_user" --dbpassword "mysql_password" --dbname "mysql_dbname"
```
Example:
```shell
$ yarn run init --dbhost "127.0.0.1" --dbport "3306"  --dbuser "username" --dbpassword "password" --dbname "codepush"
```
#### Config .env
Copy [.env.example](.env.example) to .env and update config
#### Build
```shell
$ yarn build
```
#### Start Service
```shell
$ yarn start
```
### DONE!!!!!!!

## Default Account and Password

-   account: `admin`
-   password: `123456`

## FAQ

-   [modify password](https://github.com/lisong/code-push-server/issues/43)
-   [code-push-server normal solution (CN)](https://github.com/lisong/code-push-server/issues/135)
-   targetBinaryVersion support
    -   `*`
    -   `1.2.3`
    -   `1.2`/`1.2.*`
    -   `1.2.3 - 1.2.7`
    -   `>=1.2.3 <1.2.7`
    -   `~1.2.3`
    -   `^1.2.3`

line-echo-bot-sample
==

A sample echo bot implementation of the LINE Messaging API.

This project uses the [Slim framework](http://www.slimframework.com/).

Getting started local env
--

```
$ curl -sS https://getcomposer.org/installer | php # Install composer.phar
$ ./composer.phar install
$ $EDITOR ./src/LINEBot/EchoBot/Setting.php # <= edit your bot information
$ php -S 0.0.0.0:8080 -t public
```

## Getting started with Heroku

### heruku button

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/krrrr38/line-bot-sdk-php)

then set Webhook URL: `https://{YOUR_APP}.herokuapp.com/callback`

### deploy by yourself

```sh
heroku create
heroku info # then set Webhook URL: https://{YOUR_APP}.herokuapp.com/callback
heroku config:set LINEBOT_CHANNEL_SECRET="..."
heroku config:set LINEBOT_CHANNEL_TOKEN="..."
git push heroku master
heroku logs
```

Hints
--

### [public/index.php](./public/index.php)

Entry point of this application.

### [src/LINEBot/EchoBot/Route.php](./src/LINEBot/EchoBot/Route.php)

Core logic of this application that uses the LINE Messaging API.

License
--

```
Copyright 2016 LINE Corporation

LINE Corporation licenses this file to you under the Apache License,
version 2.0 (the "License"); you may not use this file except in compliance
with the License. You may obtain a copy of the License at:

  https://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the
License for the specific language governing permissions and limitations
under the License.
```

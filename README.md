Hearsay Live News App (Frontend)
================================

#### Introduction:
A clean reading experience for your news. [Live demo](http://hearsay.me/).

##### Accompanying repos:
* [hearsay-collector](https://github.com/eiriklv/hearsay-collector/)
* [hearsay-common](https://github.com/eiriklv/hearsay-common/)
* [congregator-rssreader](https://github.com/eiriklv/congregator-rssreader/)
* [congregator-sitescraper](https://github.com/eiriklv/congregator-sitescraper/)
* [congregator-jsonfetcher](https://github.com/eiriklv/congregator-jsonfetcher/)

![hearsay](http://www.hearsay.me/logo.png)

Landing                                                                       |  Article View
:----------------------------------------------------------------------------:|:-------------------------------------------------:
![](http://s12.postimg.org/w78nzhwq5/Skjermbilde_2014_08_27_kl_01_16_08.png)  |  ![](http://s12.postimg.org/ffncgqwh9/Skjermbilde_2014_08_27_kl_01_16_39.png)
![](http://s12.postimg.org/bltw7lf59/Skjermbilde_2014_08_27_kl_01_16_25.png)  |  ![](http://s12.postimg.org/ucvthr9pp/Skjermbilde_2014_08_27_kl_01_16_46.png)

#### Built with:
* [node.js](http://www.nodejs.org/)
* [express](http://www.expressjs.com/)
* [gulp](http://www.gulpjs.com/)
* [convict](http://github.com/mozilla/node-convict/)
* [browserify](http://www.browserify.org/)
 * [envify](http://github.com/hughsk/envify/)
 * [reactify](https://github.com/andreypopp/reactify)
* [react](http://facebook.github.io/react/)
* [stylus](http://learnboost.github.io/stylus/)
* [bootstrap](http://getbootstrap.com/)
* [fontawesome](http://fortawesome.github.io/Font-Awesome/)

#### Testing:
* [jest](http://facebook.github.io/jest/)

#### Dependencies:
* [nodejs](http://www.nodejs.org/)
* [mongodb](http://www.mongodb.org/)
* [redis](http://redis.io/)

#### Install dependencies:
* `brew/apt-get install nodejs`
* `brew/apt-get install redis`
* `brew/apt-get install mongodb`
* `npm install -g mocha`
* `npm install -g gulp`
* `npm install`

#### Environment variables:
* `PORT` - Port exposed by this component.
 * example: `3000`
* `DEBUG` - Debug output (* for all) (optional)
 * example: `*`
* `NODE_ENV` - Environment ('development', 'staging', 'production')
 * example: `development`
* `CLIENT_API_PATH` - Path to the client REST api (relative)
 * example: `/api`
* `CLIENT_DOMAIN` - Server domain
 * example: `localhost`
* `APPSECRET` - Application session secret
 * example: `sOmeCrAzYhAsH894372`
* `SESSION_KEY` - Application session secret (optional)
 * example: `express.sid` (defaults to `connect.sid`)
* `REDIS_URL` - Redis url (including authentication)
 * example: `redis://user:pass@localhost:6379`
* `REDIS_DB` - Redis database number (optional)
 * example: `1`
* `REDIS_SESSION_PREFIX` - Prefix for redis session entries (optional)
 * example: `sess:`
* `MONGO_URL` - MongoDB url (including authentication)
 * example: `mongodb://user:pass@localhost:27017/mydatabase`

#### Run tests:
* `npm test`

#### Run the application:
* set environment variables
* `gulp`
* (create a shellscript with the above for convenience if you want)
* navigate your browser to `http://localhost:3000` (or whatever port you chose for `PORT`)

#### Development shellscript example:
```sh
#!/bin/sh
export PORT=3000 \
export DEBUG="*" \
export NODE_ENV="development" \
export APPSECRET="somecrazyhash" \
export CLIENT_API_PATH="/api" \
export CLIENT_DOMAIN="localhost" \
export CLIENT_API_DOMAIN="localhost" \
export SESSION_KEY="express.sid" \
export MONGO_URL="mongodb://localhost/hearsay" \
export REDIS_URL="redis://localhost:6379" \

gulp
```

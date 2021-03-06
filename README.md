# aurelia-amd-bundler

## what's new

1. [aurelia-animator-velocity](https://github.com/gooy/aurelia-animator-velocity/) now part of [aurelia-amd-bundler](https://github.com/cmichaelgraham/aurelia-amd-bundler) including `velocity` and `jsol` dependencies

## steps to bundle

1. if you've run before and you want a fresh build of the latest aurelia bits, remove the `` folder
2. remove the `bower_components` folder
2. open `git bash shell`
2. run ``
3. bundle
  1. if you are doing a fresh build: run `./fresh-build.sh`
  2. if you are updating the bundle: run `./update-build.sh`
4. install [node](https://nodejs.org/)
3. install bower (run `npm install -g bower`)


## bundling

* [link to un-minimized bundle](https://github.com/cmichaelgraham/aurelia-typescript/blob/master/aurelia-require-bundle/aurelia-bundle.js) - 435K
* [link to minimized bundle](https://github.com/cmichaelgraham/aurelia-typescript/blob/master/aurelia-require-bundle/aurelia-bundle.min.js) - 193K



![nav 01](https://cloud.githubusercontent.com/assets/10272832/6092927/9595bd04-aeb0-11e4-9773-ea07da1e04af.png)

1. open `git bash shell`
2. install `node.js`
2. install `bower`
3. change to `aurelia-require-bundle` folder
3. get the latest aurelia libraries

   run `bower install`

4. have a look at the bundling dependencies

  * [manifest of dependencies](https://github.com/cmichaelgraham/aurelia-typescript/blob/master/aurelia-require-bundle/aurelia-bundle-manifest.js)
  * [main-config](https://github.com/cmichaelgraham/aurelia-typescript/blob/master/aurelia-require-bundle/main-config.js)
  * [bower config](https://github.com/cmichaelgraham/aurelia-typescript/blob/master/aurelia-require-bundle/bower.json)

5. bundle the files for development

   run `node r.js -o name=aurelia-bundle-manifest baseUrl=. mainConfigFile=main-config.js out=aurelia-bundle.js optimize=none`

6. bundle the files for production (minified)

   run `node r.js -o name=aurelia-bundle-manifest baseUrl=. mainConfigFile=main-config.js out=aurelia-bundle.min.js`

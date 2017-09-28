#

## Packages used in this template

### devDependencies

- `babel-cli` – [docs](http://babeljs.io/docs/usage/cli/) | [gist](#babel-cli)
- `html-minifier` – [docs](https://www.npmjs.com/package/html-minifier) (NOT included)
- `imagemin` - [docs](https://www.npmjs.com/package/imagemin) | [gist](#imagemin) (NOT included)
- `live-server` – [docs](https://www.npmjs.com/package/live-server) | [gist](#live-server)
- `mkdirp` – [docs](https://www.npmjs.com/package/mkdirp) | [gist](#mkdirp)
- `node-sass` – [docs](https://www.npmjs.com/package/node-sass) | [gist](#node-sass)
- `npm-run-all` – [docs](https://www.npmjs.com/package/npm-run-all) | [gist](#npm-run-all)
- `uglify-js` – [docs](https://www.npmjs.com/package/uglify-js) | [gist](#uglify-js)

#### <a name="babel-cli"></a> babel-cli

> [Requires](http://babeljs.io/docs/plugins/preset-env/) `babel-preset-env`.
> Without any configuration options, `babel-preset-env` behaves exactly the same as `babel-preset-latest` (or `babel-preset-es2015`, `babel-preset-es2016`, and `babel-preset-es2017` together).


#### <a name="live-server"></a> live-server

```json
"dev:serve": "live-server dist --port=6262 --browser='Google Chrome'",
"prod:serve": "live-server dist --port=6262 --browser='Google Chrome'"
```

[Options used](https://www.npmjs.com/package/live-server#usage-from-command-line):

- `--port=NUMBER` - select port to use, default: PORT env var or 8080
- `--browser=BROWSER` - specify browser to use instead of system default


#### <a name="node-sass"></a> node-sass

```json
"dev:sass": "node-sass --output-style expanded --source-map true src/scss/style.scss --output builds/css"
```

Transpiles SASS to CSS.

```json
"dev:sass": "node-sass --watch process/scss --output-style expanded --source-map true src/scss/style.scss --output builds/css",
"prod:sass": "node-sass --output-style compressed src/scss/style.scss --output dist/css"
```

[Options used](https://www.npmjs.com/package/node-sass#usage-1):

- `--output-style expanded` – CSS output style (nested | expanded | compact | compressed)
- `--source-map true` – Emit source map


#### <a name="imagemin"></a> imagemin

Minify images.

```json
"prod:img-compress": "imagemin src/assets/img/**/*.* --out-dir=build/assets/img  --plugin=jpeg-recompress --plugin=svgo"
```

> You also need to install [`imagemin-cli`](https://github.com/imagemin/imagemin-cli) in order to use `imagemin` AND [plugins](https://www.npmjs.com/browse/keyword/imageminplugin) for this package that you want to use.


#### <a name="uglify-js"></a> uglify-js

```json
"prod:js-uglify": "uglifyjs src/js/index.js --compress --mangle --output dist/js/script.js",
```

[Options used](https://www.npmjs.com/package/uglify-js#command-line-options):

- `--compress` – Enable compressor/specify compressor options...
- `--mangle` – Mangle names/specify mangler options...

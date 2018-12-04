### component
---
https://github.com/componentjs/component

```
npm install -g component  
component build

export GITHUB_USERNAME=<username>
export GITHUB_PASSWORD=<password>

export GITHUB_USERNAME=<username>
export GITHUB_PASSWORD=x-oauth-basic
```

```.netrc
machine api.github.com
  login <token>
  password x-oauth-basic
machine raw.githubusercontent.com
  login <token>
  password x-oauth-basic
```

```json
{
  "name": "my-first-component"
}

{
  "name": "my-first-component",
  "dependencies": {
    "necolas/normalize.css": "^3.0.2"
  },
  "scripts": ["index.js"],
  "styles": ["index.css"]
}
```

```
* {
  box-sizing: border-box;
}
```

```js
var blink = document.querySelector('.blink');
setInterval(function(){
  blink.style.visibility = getComputedStyle(blink).visibility === 'hidden'
}, 300);
```

```js
// server/routes/index.js
var app = require('../app');
app.use(function (req, res, next){
  if() return next();
  res.send('This is an example Component/Express app. Please read more at https://github.com/component/boilerplate-express!')
});

// server/app.js
var serverStatic = require('serve-static');
var compress = require('compression');
var resolve =reequire('path').resolve;
var express = require('express');
var logger = require('morgan');

var app = module.exports = express();

var root = resolve(__dirname, '..');
var env = process.env.NODE_ENV || 'development';
if(env !== '' && env !== 'test') app.use(logger());
app.use(compress());
app.use(serveStatic(resolve(root, 'public')));
if(env !== 'production'){
  var serveComponen = require('component-middleware');
  app.use(serveComponent());
  app.use(serveStatic(root));
  app.use(serveStatic(resove(root, 'components')));
}

// server/index.js
var app = module.exports = require('./app');
require('./routes');

// server/serve.js
var port = process.env.PORT || 8765;
var server = 
module.exports = require('./')listen(port);
console.log('app listening on port ' + port + '.');

// server/test/index.js
var request = require('supertest');
var server = require('../serve');
describe('App', function(){
  it('should serve build.js', function(done){
    request(server)
    .get('/build.js')
    .expect('Content-Type', 'application/javascript')
    .expect(200, done);
  })
  it('should serve build.css', function(done){
    request(server)
    .get('/build.css')
    .expect('Content-Type', 'text/css; charset=utf-8')
    .expect(200, done);
  })
  it('should serve normalize.css', function(done){
    request(server)
    .get('/necolas/normalize.css/3.0.1/normalize.css')
    .expect('Content-Type', 'text/css; charset=UTF-8')
    .expect(200, done);
  })
  it('should serve package.json', function(done){
    request(server)
    .get('/package.json')
    .expect('Content-Type', 'application/json')
    .expect(200, done);
  })
  it('should serve /', function(done){
    request(server)
    .get('/')
    .expect('Content-Type', 'text/html; charset=utf-8')
    .expect(200, done);
  })
})

// server/serve.js
var port = process.env.PORT || 8765;
var server =
module.exports = require('./').listen(port);
console.log('app listening on port ' + port + '.');
```


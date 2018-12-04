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


# Koa Sleep Middleware

This koa middleware will "sleep" or delay moving forward for the defined timeout.

## Usage

Require the middleware and add it to your middleware pipeline where you want a delay.

```
// sleep for 100ms
app.use(sleep(100))
```

## Example

```shell
npm install koa-sleep --save
```

```javascript
var koa = require('koa')
var app = koa()

var sleep = require('koa-sleep')
 
// Sleep for 100ms
app.use(sleep(100))

// Send the response body
app.use(function *(next){

  // Obligatory hello world
  this.body = 'Hello World'
  
})

// Listen for incoming requests
app.listen(1337)
```
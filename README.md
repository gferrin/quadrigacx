# Node QuadrigaCX
This is a node.js wrapper for the QuadrigaCX [API](https://www.quadrigacx.com/api_info).

### Install

`npm install cointrader`

```js
var QuadrigaCX = require('quadrigacx');

var quadrigacx = new QuadrigaCX(client_id, key, secret);

var params = {
	amount: 1.1
	price: 342.42
	book: 'btc_cad'	
};

quadrigacx.api('buy', params, function(err, order){
	if(err){
		throw(err)
	}

	console.log(order);
});
```

## Functions

`api` is the main function which accepts any method name, either public or private, and parameters and makes the request.  

`api(method, params, cb)`

`public_request(path, params, cb)`

`private_request(path, params, cb)`



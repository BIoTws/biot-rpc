# biot-rpc


### The library for initializing the rpc connection, in conjunction with [biot-core](https://github.com/BIoTws/biot-core), is used for remote invocation of async / await functions.
</br></br>

## How to install
</br>

#### downloads project files
```
$ git clone https://github.com/BIoTws/biot-rpc
```

#### install dependencies
```
$ npm install
```

#### run server
```
$ node server
```
</br>


## Example client

> For an example on nodejs, we will use the jayson library

</br>

```
$ npm --save -i jayson
```

</br></br>

```javascript
const jayson = require('jayson');

let stream = jayson.client.http({port:4303, headers:{'X-AUTH': 123456}});

stream.request('getMyDeviceWallets', [], (err, state) => {
    if(err)
        throw err;

    console.log(state);
});
```
#### terminal
```
> node examples/example1
```

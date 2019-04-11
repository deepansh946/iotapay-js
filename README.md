# [IOTAPAY](https://iotapay.dev/)

[![GitHub package.json version](https://img.shields.io/github/package-json/v/acycliclabs/iotapay-js.svg)](https://github.com/acycliclabs/iotapay-js/releases)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![node](https://img.shields.io/badge/node-%3E%3D8.9.4-brightgreen.svg)](https://nodejs.org/download/release/v8.9.4/)
[![npm](https://img.shields.io/npm/dt/iotapay.svg)](https://www.npmjs.com/package/iotapay)
[![NPM](https://nodei.co/npm/iotapay.png)](https://nodei.co/npm/iotapay/)


[NodeJs](https://nodejs.org/) library to Pay using IOTA

# Setup

Install the library `npm install iotapay`

Import package: `require('iotapay');`

Initialize:
```
new IOTAPAY({
    host : 'http://node06.iotatoken.nl:14265'
});
```

***

## Basic functions

<details><summary>Get Balance:</summary>
<p>

<details><summary>Initialize:</summary>
<p>

#### Initialize the iotapay object.

```javascript
const iotapay = new IOTAPAY({
    host : 'http://node06.iotatoken.nl:14265'
});
```

</p>
</details>

<details><summary>Retreive Balance:</summary>
<p>

#### Initialize the iotapay object.

```javascript
iotapay.getBalance(['ADDRESS'], function (err, balance) {
    if(err) {
        console.log('error:', err);
    }
    console.log('balance:', balance);
})
```

</p>
</details>

</p>
</details>

***

<details><summary>Pay:</summary>
<p>

#### Initialize the iotapay object.

```javascript
iotapay.transfer({
    address: 'ADDRESS',
    value: 1,
    message: 'Testing',
    seed: 'SEED'
}, function (err, result) {
    if(err) {
        console.log('error:', err);
    }
    console.log('result:', result);
})
```

Result gives bundle hash.

</p>
</details>

***

#### More Functions coming soon.

NOTE: Please, use proper iota node url, ADDRESS and your SEED to initialise. These are simple dummy values. NOT meant for production usage.

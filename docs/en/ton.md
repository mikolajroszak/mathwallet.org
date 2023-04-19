# TON

## Integrating

### Detecting the Provider

MathWallet will inject an object called `ton` on the [window](https://developer.mozilla.org/en-US/docs/Web/API/Window) object of any web application the user visits.

To detect if a browser extension using this API is installed, you can check for the existence of the `ton` object.

To make it easy to detect MathWallet specifically, the extension adds an additional `isMathWallet` flag.

```javascript
const isMathWalletInstalled = window.ton && window.ton.isMathWallet
```
or

```javascript
const isMathWalletInstalled = window.openmask.provider && window.openmask.provider.isMathWallet
```

If MathWallet is not installed, we recommend you redirect your users to [our website](https://mathwallet.org/). Altogether, this may look like the following.

## Workflows.
[https://github.com/ton-blockchain/ton-connect/blob/main/workflows.md#first-time-connection-via-js-bridge](https://github.com/ton-blockchain/ton-connect/blob/main/workflows.md#first-time-connection-via-js-bridge)

1. App checks existing of the `window.openmask.tonconnect`
2. App calls `window.openmask.tonconnect.connect()` and waits for a response
3. Wallet sends account information to the app;

### Dapp Developer Guide
[https://github.com/ton-blockchain/ton-connect/blob/main/bridge.md#js-bridge](https://github.com/ton-blockchain/ton-connect/blob/main/bridge.md#js-bridge)

## More Resources
[https://github.com/ton-blockchain/ton-connect/blob/main/requests-responses.md#methods](https://github.com/ton-blockchain/ton-connect/blob/main/requests-responses.md#methods)

[https://github.com/ton-connect/sdk](https://github.com/ton-connect/sdk)


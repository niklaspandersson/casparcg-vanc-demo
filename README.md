# Demo on VANC in caspar

This repo contains everything you need to send OP47 and SCTE104 vanc payload to a casparcg server

## The casparcg sercer

1. Using the branch `https://github.com/nxtedition/casparcg/tree/fix/decklink-vanc-parity`
2. Add the following to your decklink config in casparcg.config

```xml
<vanc>
    <op47-line>12</op47-line>
    <op47-line-2>575</op47-line-2>
    <op42-sd-line>21</op42-sd-line>
    <op47-dummy-header>VVUnFRXq6v0v6pteFSAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAg</dummy-header>
    <scte104-line>13</scte104-line>
</vanc>
```

Refer to the `op47-client.js` and `sce104-client.js` for how to format AMCP commands to push vanc data to the server

## OP47

Run `node op47-client.js`

## SCTE104

Run `node scte104-client.js`

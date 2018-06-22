# shipit-better-deploy

Fork from [shipitjs/shipit-deploy](https://github.com/shipitjs/shipit-deploy)

Upgrade for large project deploy.

In the original function, provide incremental updates.
The `workspace` folder will not be deleted, it will always exist as a cache, and the file will be synchronized with the remote.

## Install

```bash
npm i -D shipit-better-deploy
```

## How to use

```javascript
module.exports = function(shipit) {
  require("shipit-better-deploy")(shipit);
  // same code
  shipit.initConfig({
    default: {
      pullDataDeploy: true // default is `false`
    }
  });
};
```

### Tips

~~If you have used `shipit-deploy` before, you need to delete the `workspace` folder first, only to be slow for the first time.~~

You need not remove the old folder after [0.0.6](/CHANGELOG.md#v006).

have fun, enjoy the fast deploy.

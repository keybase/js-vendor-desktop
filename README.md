# Desktop JS vendored deps

This repository contains vendored dependencies for [keybase/client/desktop][keybase/client/desktop] using [shrinkpack][shrinkpack].


## Installing vendored npm deps

Within [keybase/client/desktop][keybase/client/desktop], run:

```sh
KEYBASE_JS_VENDOR_DIR=this/repo/path npm run vendor-install
```

## Adding/updating vendored npm deps

### Automatically

```sh
KEYBASE_JS_VENDOR_DIR=this/repo/path npm run vendor-update
```
### Manually

1. `npm install` your new/changed packages locally.
1. Run `npm run wrap` to remove extraneous packages and update the shrinkwrap file.
1. Run `shrinkpack` (`npm install -g shrinkpack` if not installed).
1. Copy updated `npm-shrinkwrap.json` and `node_shrinkwrap` files to this repository, and push a new commit.
1. Update the `"keybaseVendoredDependencies"` value in the [keybase/client/desktop][keybase/client/desktop] `package.json` to point to your new commit.


## Updating Flow

The flow binary is stored in the flow/ directory. The release is downloaded
from the [Flow release page on GitHub][flow-release].


## Updating Electron

The electron binaries for each platform are stored in the electron/ directory.
The releases are downloaded from the [Electron release page on
GitHub][electron-release].


[keybase/client/desktop]: https://github.com/keybase/client/tree/master/desktop
[shrinkpack]: https://github.com/JamieMason/shrinkpack/
[flow-release]: https://github.com/flowtype/flow-bin/releases
[electron-release]: https://github.com/electron/electron/releases

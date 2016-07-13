# Desktop JS vendored deps

This repository contains vendored dependencies for [keybase/client/desktop][keybase/client/desktop] using [shrinkpack][shrinkpack].


## Usage

Within [keybase/client/desktop][keybase/client/desktop], run:

```sh
node vendor-install
```


## Updating dependencies

1. `npm install` your new/changed packages locally.
1. Run `npm run wrap` to remove extraneous packages and update the shrinkwrap file.
1. Run `shrinkpack` (`npm install -g shrinkpack` if not installed).
1. Copy updated `npm-shrinkwrap.json` and `node_shrinkwrap` files to this repository, and push a new commit.
1. Update the `"keybaseVendoredDependencies"` value in the [keybase/client/desktop][keybase/client/desktop] `package.json` to point to your new commit.


[keybase/client/desktop]: https://github.com/keybase/client/tree/master/desktop
[shrinkpack]: https://github.com/JamieMason/shrinkpack/

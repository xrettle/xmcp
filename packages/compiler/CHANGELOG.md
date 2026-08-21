# @xmcp-dev/compiler

## 1.0.0

### Minor Changes

- dfaf370: Emit ESM server bundles when the application's `package.json` declares `"type": "module"`. The build writes a `dist/package.json` module marker so the self-contained output keeps running when deployed without the project, and node builtins resolve through `createRequire`. Projects without the field keep CommonJS output unchanged.

### Patch Changes

- af43435: Declare `serverCardHandler` in the generated Next.js adapter types so the documented server-card route passes application type checking.
  - xmcp@1.0.0

## 0.8.0

### Minor Changes

- b7a2b3c: Move the development compiler into `@xmcp-dev/compiler` so production `xmcp` installs contain only the self-contained runtime. Existing `xmcp dev`, `xmcp build`, and `xmcp create` commands remain available through a runtime-package shim, but projects must add `@xmcp-dev/compiler` as a development dependency.

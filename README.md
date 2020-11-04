# Build issue with thread-loader and ts-loader

This repo demonstrates a build error when using `thread-loader` in combination with `ts-loader` 8.0.8.

## Running it

- install modules `yarn install`
- try to build `yarn build`

An error should be displayed:
```
yarn run v1.16.0
warning package.json: No license field
warning ../../package.json: No license field
$ webpack
[webpack-cli] Compilation finished
assets by status 763 bytes [cached] 1 asset
./src/app.ts 39 bytes [built] [code generated] [1 error]

ERROR in ./src/app.ts
Module build failed (from ./node_modules/thread-loader/dist/cjs.js):
Thread Loader (Worker 0)
Invalid value used as weak map key
    at PoolWorker.fromErrorObj (/Users/valeriopipolo/repos/tsloader-build-issue-with-thread-loader/node_modules/thread-loader/dist/WorkerPool.js:344:12)
    at /Users/valeriopipolo/repos/tsloader-build-issue-with-thread-loader/node_modules/thread-loader/dist/WorkerPool.js:217:29
    at WeakMap.set (<anonymous>)
    at Object.getTypeScriptInstance (/Users/valeriopipolo/repos/tsloader-build-issue-with-thread-loader/node_modules/ts-loader/dist/instances.js:37:23)
    at Object.loader (/Users/valeriopipolo/repos/tsloader-build-issue-with-thread-loader/node_modules/ts-loader/dist/index.js:16:41)

webpack 5.3.2 compiled with 1 error in 473 ms
```
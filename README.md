#  Serverless & NextJS & IPFS

Executing 'serverless' command does not go through and fails with error as below.


## Reproducing
Please clone and execute the two commands 

### NPM build works

> npm run build 

### Serverless build fails

> serverless 

### Error trace


```
./node_modules/ipfs-utils/src/http/fetch.js
Critical dependency: the request of a dependency is an expression

Import trace for requested module:
./node_modules/ipfs-utils/src/http.js
./node_modules/ipfs-http-client/src/files/rm.js
./node_modules/ipfs-http-client/src/files/index.js
./node_modules/ipfs-http-client/src/index.js
./pages/index.js
./node_modules/next/dist/build/webpack/loaders/next-serverless-loader/index.js?absolute404Path=&absoluteAppPath=private-next-pages%2F_app.js&absoluteDocumentPath=next%2Fdist%2Fpages%2F_document&absoluteErrorPath=next%2Fdist%2Fpages%2F_error&absolutePagePath=private-next-pages%2Findex.js&assetPrefix=&basePath=&buildId=gQxHDOJ8lrMT5Qk0kmIBT&canonicalBase=&distDir=private-dot-next&generateEtags=true&i18n=&loadedEnvFiles=W10%3D&page=%2F&poweredByHeader=true&previewProps=%7B%22previewModeId%22%3A%22e8816b52814ebe1a5c7a63e4cd2cc76f%22%2C%22previewModeSigningKey%22%3A%22e2f4a2cb9ee7dfffa7eeadd21b586da46da0e0c6e6508763a065ff607af68dbb%22%2C%22previewModeEncryptionKey%22%3A%22ba043e56184bcb1b09ecd38aec6cab26aa6ab009dfd1b079d1c6cb017b6619dd%22%7D&runtimeConfig=!

Error: Cannot find module './fetch.node'
    at webpackEmptyContext (/Users/thorsten/Documents/Projects/my-app/.next/serverless/pages/index.js:11:10)
    at Object.2548 (/Users/thorsten/Documents/Projects/my-app/.next/serverless/chunks/247.js:5107:40)
    at __webpack_require__ (/Users/thorsten/Documents/Projects/my-app/.next/serverless/webpack-runtime.js:25:43)
    at Object.7137 (/Users/thorsten/Documents/Projects/my-app/.next/serverless/chunks/247.js:4683:37)
    at __webpack_require__ (/Users/thorsten/Documents/Projects/my-app/.next/serverless/webpack-runtime.js:25:43)
    at Object.1781 (/Users/thorsten/Documents/Projects/my-app/.next/serverless/chunks/247.js:16970:12)
    at __webpack_require__ (/Users/thorsten/Documents/Projects/my-app/.next/serverless/webpack-runtime.js:25:43)
    at Module.3678 (/Users/thorsten/Documents/Projects/my-app/.next/serverless/pages/index.js:158:74)
    at __webpack_require__ (/Users/thorsten/Documents/Projects/my-app/.next/serverless/webpack-runtime.js:25:43)
    at Module.4883 (/Users/thorsten/Documents/Projects/my-app/.next/serverless/pages/index.js:85:23) {
  code: 'MODULE_NOT_FOUND'
}
```
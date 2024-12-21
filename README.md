# rollup+ts脚手架
打包后将readme和package.json复制到dist目录
然后再发布npm包
dist下的package需要修改为
```json
{
  "name": "rollup-ts-cli",
  "version": "1.0.0",
  "main": "index.js",
  "type": "module",
  "typings": "types/index.d.ts",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "build": "rimraf dist&&rollup --config"
  },
  "keywords": [],
  "author": "刘范思哲",
  "license": "ISC",
  "description": "rollup+ts脚手架",
  "devDependencies": {
    "@rollup/plugin-commonjs": "^28.0.2",
    "@rollup/plugin-json": "^6.1.0",
    "@rollup/plugin-node-resolve": "^16.0.0",
    "@rollup/plugin-terser": "^0.4.4",
    "@rollup/plugin-typescript": "^12.1.2",
    "@types/qs": "^6.9.17",
    "rimraf": "^6.0.1",
    "rollup": "^4.28.1",
    "tslib": "^2.8.1",
    "typescript": "^5.7.2"
  }
}

```
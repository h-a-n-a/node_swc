# node_swc
swc node binding use wasm

### Build

```shell
$ wasm-pack build # build wasm, make sure you switched rustup to the nightly version or you will get an error
$ yarn build # build node
```

### Usage

```js
import { parseSync, printSync } from 'node-swc'

const ast = parseSync(`const a: string = "hello world"`, {
  syntax: 'typescript'
})

const { code } = printSync(ast, {
  minify: true
})
```
### License

MIT

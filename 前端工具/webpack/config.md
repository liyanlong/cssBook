# How To Config ?
> 如何去配置 webpack.config.js

## DEMO
```javascript
{
  context: __dirname + "/app",
  entry: "./entry",
  output: {
      path: __dirname + "/dist",
      filename: "bundle.js"
  }
}
```


## 基本配置项

| name | description | type | default |
| -- | -- | -- | -- |
| `context` | 文件绝对路径 base path | string | process.cwd() |
| `entry` | 入口文件 | string &#124; array &#124; object | &nbsp;|
| `output` | 输出配置 | object | &nbsp; |
| `module` | 模块配置 | object | &nbsp; |
| `resolve` | 模块分解配置 | object | &nbsp; |
| `plugins` | 插件配置 | object | &nbsp; |
| `externals` | 外部扩展 | array | &nbsp; |
and so on ...

### `output`

| name | description | type | default |
| -- | -- | -- | -- |
| `output.filename` | 输出文件名 | string | &nbsp; |
| `output.path` | 输出路径(要求：absolute path)  | string | &nbsp; |
| `output.chunkFilename` | 没有在入口文件定义，但却需要打包的文件  | string | &nbsp; |
| `output.sourceMapFilename` | 根据入口文件生成的sourcemap文件  | string | &nbsp; |
| `output.library` | 如果配置libray, 输出 name 做为 library name  | string | &nbsp; |
| `output.libraryTarget` | 输出变量方式，"var", "this", "commonjs", "commonjs2", "umd", "cmd",   | string | "var" |

### `module`

| name | description | type | default |
| -- | -- | -- | -- |
| `module.loaders` | 加载器 | array | &nbsp; |
| `module.preLoaders` | 预加载器 | array | &nbsp; |
| `module.postLoaders` |  | array | &nbsp; |
| `module.noParse` |  | RegExp | &nbsp; |

### `resolve`
| name | description | type | default |
| -- | -- | -- | -- |
| `resolve.alias` | 模块别名 | object | &nbsp; |
| `module.root` | 根绝对路径 | string &#124; array | &nbsp; |
| `module.modulesDirectories` | 模块文件夹名称 | string | node_modules |
| `module.fallback` | 如果在root路径下寻找不到模块,则在该路径下寻找 | string &#124; array | &nbsp; |
| `module.extensions` | 默认模块扩展名称 | string &#124; array | [".webpack.js", ".web.js", ".js"] |

# taro-plugin-dynamic-import-weapp

> 基于 Taro 3.0 的小程序端动态加载逻辑

使用方式见 [taro-plugin-dynamic-import-weapp](./packages/taro-plugin-dynamic-import-weapp/README.md)

## 运行 demo

建议 node 版本 `12.x`

```bash
# 项目根目录安装依赖
yarn

# 编译项目
yarn run compile

# 打包 demo 项目, 默认开发端口是 5000
yarn run start
```

项目运行后:

- 打开小程序开发者工具, 可以看到动态请求的 js 代码
- 可以修改 `packages/demo/src/dynamic-import` 中的代码, 对比打包结果

> 注意, 如果没有提供 port 和 publicPath 的情况下, 会使用随机生成的端口, 每次打包都会更改 `runtime.js` 的 `publicPath` 端口, 正式环境指定 `publicPath` 即可

### 示例预览图

**静态页面示例图:**

![静态页面示例图](./assets/demo-static.jpg)

**动态页面示例图:**

![动态页面示例图](./assets/demo-dynamic.jpg)

## 缺点

- 不支持 `webpack 5.0+`
- 不支持动态加载样式文件 `wxss`, 建议使用原子性的 CSS 库 `tailwind CSS`

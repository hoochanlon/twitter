# twitter

* 源repo: [创建 Issue](https://github.com/SimonAKing/Gwitter) 

优化部分：在 rsbuild.config.mjs 文件中把 assetPrefix 改为 ./ 或删除该字段即可，这样生成的资源路径就是相对路径，适合本地或任意域名部署

安装

```
pnpm install
pnpm run build
pnpm run dev
```

参数：



`rsbuild.config.mjs` 修改成自己的URL

```
 output: {
    assetPrefix: isProd ? 'hoochanlon.github.io/twitter' : './',
  },
```
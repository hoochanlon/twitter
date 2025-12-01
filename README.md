# twitter

源repo: https://github.com/SimonAKing/Gwitter 

## 安装

npm 安装会报错，建议使用 pnpm 安装。

```
pnpm install
```

构建与本地预览

```
pnpm run build
pnpm run dev
```

## 参数

> 优化部分：在 rsbuild.config.mjs 文件中把 assetPrefix 改为 ./ 或删除该字段即可，这样生成的资源路径就是相对路径，适合本地或任意域名部署

`rsbuild.config.mjs` 修改成自己的域名url

```
 output: {
    assetPrefix: isProd ? 'hoochanlon.github.io/twitter' : './',
  }
```

`/src/config/index.ts`

* token：不用填，保持默认就好
* owner：你的github用户名
* repo：你的仓库

```
let config = {
  request: {
    token:
      'g?i?t?h?u?b?_?p?a?t?_?1?1?A?H?V?6?E?W?Q?0?M?f?C?S?r?0?4?K?A?j?1?F?_?3?7?n?4?U?y?u?S?m?d?z?i?t?D?s?w?i?s?i?u?a?g?N?b?a?k?V?n?L?I?7?U?W?s?s?h?n?K?p?s?H?S?D?S?4?D?K?O?Q?Q?J?S?S?x?q?z?Z?X?M',
    clientID: 'Ov23liGgrdAbsi8wF5eJ',
    clientSecret: 'fc423f948e99588015d46c7d76427db48a059f55',
    pageSize: 6,
    autoProxy:
      'https://cors-anywhere.azm.workers.dev/https://github.com/login/oauth/access_token',
    owner: 'hoochanlon',
    repo: 'twitter',
  },
```

## 配置设置

* 访问 https://github.com/settings/tokens 点击 "Generate new token (classic)"
  * 勾选 public repo、user 全部权限，永不过期。
* 访问 https://github.com/settings/developers > OAuth Apps > New OAuth App
  * Homepage URL，例如：hoochanlon.github.io/twitter
  * Authorization callback URL，例如：hoochanlon.github.io/twitter
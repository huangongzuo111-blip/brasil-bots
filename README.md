# 🇧🇷 Nossos Bots — Mini App 目录页

一个静态页，把全部 9 个 Telegram bot 列在一起。用户从任一 bot 点「🔗 Todos os bots」
就能看到全套，点击直达。

## 为什么用这个而不是合并 bot

合并 bot **不会带来用户**（Telegram 没有用户迁移机制，11500 个注册用户一个都带不走），
只会把 9 个没人用的产品变成一个更难解释的产品。

目录页解决的是**完全不同的一个问题**：让已经有兴趣的人**一次看到你全部的东西**，
从一个 bot 引流到其他 bot。**不牺牲定位，也不丢用户。**

## 部署（GitHub Pages，免费 HTTPS）

1. 在 GitHub 建 **public** 仓库 `brasil-bots`（Pages 免费版只支持 public；
   这里的内容全是公开的 bot 链接，没有敏感信息，public 没问题）
2. 推上去（见下方命令）
3. 仓库 **Settings → Pages → Source: Deploy from a branch → main / (root)** → Save
4. 等 1 分钟，得到 `https://huangongzuo111-blip.github.io/brasil-bots/`

## 接进 bot

把上面那个地址填进每个 bot 的 `.env`：

```
CATALOG_URL=https://huangongzuo111-blip.github.io/brasil-bots/
```

首页就会出现「🔗 Todos os bots」按钮。用 `url=` 而不是 `web_app=` ——
`web_app` 按钮需要每个 bot 先在 BotFather `/newapp` 注册，9 次；`url` 一次搞定，
而且点开也是 Telegram 内置浏览器，体验一样。

## 加新 bot

只改 `index.html` 里那个 `BOTS` 数组，`git push` 即可，不用碰任何 bot 代码。

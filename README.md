# widowmaker2025.github.io
Zola &amp; Ametrine 的个人博客仓库

# [daudix.one](https://daudix.one)

[![Netlify Status](https://api.netlify.com/api/v1/badges/ebae929e-5e6e-4b5f-855c-6942733fca41/deploy-status)](https://app.netlify.com/projects/daudix/deploys)

The source code of my personal website. It is powered by [Zola](https://www.getzola.org) and [Ametrine](https://ametrine.daudix.one).

![Screenshot](screenshot.png)

## Read Me, for Real

If you like how my website looks and want to make your own based on it: DON'T.

Seriously, just use the [Ametrine](https://ametrine.daudix.one) theme; I'm the author of it and it's literally the same thing minus all my content, custom elements, and the like. Save your nerves, I'm serious.

If you want to use some custom styles and stuff from here: go ahead! ...just don't make it *too similar,* I got to have some uniqueness x3

## Setup Local Repository

Mostly for myself.

- Clone the repository recursively:

```bash
git clone --recursive git@github.com:daudix/daudix.one.git
```

- Checkout `main` branch for Ametrine:

```bash
cd daudix.one/themes/ametrine/
git checkout main
```

- Set the remote URL to an SSH one:

```bash
git remote set-url origin git@codeberg.org/daudix/ametrine.git
```

</> with <3 by [daudix](https://daudix.one)

验证 主题 依赖的子模块是否安装成功 ; 


```
(base)  ~/00BlogZola/themes/ametrine/icons > git submodule status
 b571e7178156c2469fc5b342e79a0a3eedf2530b phosphor-icons (v2.0.8-25-gb571e717)
 50770347051fa06f46ad2555f050c2bfb94a7e96 simple-icons (50770347)
 ```


 ```
 Error: Failed to build the site
Error: Failed to render content of /Users/songhoujin/00BlogZola/content/nanolog/2024-11-23-content-duplication/index.md
Error: Reason: Failed to render emoji shortcode
Error: Reason: Failed to render 'shortcodes/emoji.html'
Error: Reason: Function call 'load_data' failed
Error: Reason: `load_data`: Failed to parse response from https://wetdry.world/api/v1/custom_emojis: reqwest::Error { kind: Decode, source: TimedOut }

```

报错原因分析: emojis 依赖的 网络不支持, 直接在配置文件中 关掉即可

no_emojis = false  改为 true

```

Error: Failed to build the site
Error: Failed to render page '/Users/songhoujin/00BlogZola/content/blog/2025-07-16-new-era/index.md'
Error: Reason: Failed to render 'article.html'
Error: Reason: Function call 'load_data' failed
Error: Reason: `load_data`: Could not get response status for url: https://api.qrserver.com/v1/create-qr-code/?data=https://wetdry.world/@daudix/114864922325514289&format=svg&size=116x116

```
报错原因分析: 同上, 配置文件中设置

show_comments_qr = true 改为 false



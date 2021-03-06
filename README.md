<!--
 * @describe: 描述文件
 * @Author: superDragon
 * @Date: 2019-09-02 09:48:18
 * @LastEditors: superDragon
 * @LastEditTime: 2019-09-03 09:58:36
 -->
<div align="center">
<h1>HEKR-UI</h1>
</div>
<div align="center">
<a href="https://hy.hekr.me/hk-ui/web/component/hk-button.html" target="_blank" rel="noopener noreferrer"><img width="200" src="./public/logo.png" alt="hekr logo"></a>
</div>
<div align="center">
  <a><img src="https://img.shields.io/circleci/project/github/vuejs/vue/dev.svg" alt="Build Status"></a>
  <a><img src="https://img.shields.io/badge/language-vue-42b983.svg" alt="Language"></a>
  <a ><img src="https://img.shields.io/badge/license-MIT-000000.svg" alt="Version"></a>
  <br>
    <a href="https://996.icu"><img src="https://img.shields.io/badge/link-996.icu-red.svg" alt="996.icu"></a>
  <a href="https://hy.hekr.me/hk-ui/web/index.html"><img src="https://img.shields.io/badge/hk_ui@V1.0-blue.svg" alt="hk-ui"></a>
</div>

## 构建命令

```bash
# 安装依赖
npm install

# 启动本地服务（默认test环境接口） localhost:8080
npm run dev

# 打包docs
npm run build

# 打包组件库
npm run lib
```

## 文档地址

- 地址： https://hy.hekr.me/hk-ui/web/index.html

## 项目目录

```bash
template
├─ docs
│    └─ .vuepress            # 配置、演示组件、静态资源
│    │    ├─ compnents        # 演示组件
│    │    |    └─ demo          # demo组件
│    │    ├─ public           # 静态资源
│    │    |    └─ images        # 图片文件
│    │    |    └─ scss          # 样式文件
│    │    ├─ config.js        # 配置文件
│    │    └─ enhanceApp       # 引入文件
|    ├─ compnent             # 组件md文件
|    └─ README              # 首页md
├─ packages
│    ├─ index.js             # 组件index.js
│    └─ hk-countup           # countup组件
├─ public
└─ package.json
```

## 源码地址

GitLab：[http://gitlab.hekr.me/front-end/hk-ui](http://gitlab.hekr.me/front-end/hk-ui)
GitHub：[https://github.com/xkloveme/hk-ui](https://github.com/xkloveme/hk-ui)

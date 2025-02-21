
### billd-live

- 安装依赖（建议使用 node 版本：v18.19.0）

```bash
pnpm i
```

> 更新 billd 相关依赖：

```bash
pnpm i billd-utils@latest billd-scss@latest billd-deploy@latest billd-html-webpack-plugin@latest
```

- 运行

```bash
npm run start
```

- 打包

```bash
npm run build
```

### billd-live-server

- 安装依赖（建议使用 node 版本：v18.19.0）

```bash
pnpm i
```

> 更新 billd 相关依赖：

```bash
pnpm i billd-utils@latest billd-scss@latest billd-html-webpack-plugin@latest
```

> 本地必须要有 docker、ffmpeg 环境！
>
> 项目启动后，会在项目的 src/secret/目录下生成 ssecret-dev、ecret-beta、secret-prod 文件，请填写里面的信息，MYSQL_CONFIG、REDIS_CONFIG、RABBITMQ_CONFIG、SRS_CONFIG 必填！

```bash
# 1.初始化docker容器
pnpm run docker:dev

# 2.初始化数据库（可选，只需要执行一次）
pnpm run mysql:dev

# 3.运行（4300端口）
pnpm run dev
```

## 兼容性

- [x] iphone 14
- [x] 三星 s10
- [x] ipad air 3

## 常见问题

[https://live.hsslive.cn/doc/faq](https://live.hsslive.cn/doc/faq)

## 技术支持

[https://live.hsslive.cn/support](https://live.hsslive.cn/support)

## 环境配置

### 本地开发环境

> 配置：MacBook Pro 2023 Apple M3 Max，14 核 CPU，36G 内存

- 操作系统：mac os 14.1
- ffmpeg 版本：6.1.1
- node 版本：v18.19.0
- pnpm 版本：8.6.3
- docker 版本：24.0.5, build ced0996
- mysql 版本：基于 docker，镜像：mysql:8.0
- redis 版本：基于 docker，镜像：redis:7.0
- rabbitmq 版本：基于 docker，镜像：rabbitmq:3.11-management
- srs 版本：基于 docker，镜像：registry.cn-hangzhou.aliyuncs.com/ossrs/srs:5.0.170

### 构建/托管服务器环境

> 配置：4 核 CPU，4G 内存，8M 带宽（广州）

- 操作系统：CentOS Linux release 8.2.2004
- nginx 版本：1.22.1
- node 版本：v18.19.0
- pnpm 版本：8.6.3
- docker 版本：23.0.1, build a5ee5b1
- mysql 版本：基于 docker，镜像：mysql:8.0
- redis 版本：基于 docker，镜像：redis:7.0
- rabbitmq 版本：基于 docker，镜像：rabbitmq:3.11-management

### 流媒体服务器环境

> ~~配置：2 核 CPU，2G 内存，带宽 30M（香港）~~，2G 内存也能跑，但偶尔会占满内存导致服务器卡死。
>
> 配置：2 核 CPU，4G 内存，带宽 30M（香港）

- 操作系统：Alibaba Cloud Linux release 3 (Soaring Falcon)
- ffmpeg 版本：6.0
- node 版本：v18.19.0
- pnpm 版本：8.6.3
- pm2 版本：5.3.0
- docker 版本：24.0.2, build cb74dfc
- srs 版本：基于 docker，镜像：registry.cn-hangzhou.aliyuncs.com/ossrs/srs:5.0.170

## 致敬开源

billd-live 自 2023 年 3 月开源以来，仅有作者（也就是我）一个人维护，深知做开源的难处。

如果你做过开源项目，并且单个仓库拿到 **`128+star`**，我个人认为这是非常不容易的，因为这代表了你的开源被很多人关注或认同，如果此时你正在了解直播相关方面的内容，我录制的 [**billd-live 付费课**](https://www.hsslive.cn/article/151) 或许会对你有一定帮助，它将对你进行**免费**，作为我认同你在开源方面做的贡献，以及我对你力所能及的回馈，希望你能不忘初心，砥砺前行~
# live-server

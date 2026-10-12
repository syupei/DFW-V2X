# 大富翁 · DFW-V2X

中国旅行主题浏览器竞速游戏的测试发行项目。支持本机 AI 游戏和 2–4 人好友房；联网模式由 Node.js 服务端通过 WebSocket 同步。

## 下载与运行

前往 [Releases](https://github.com/syupei/DFW-V2X/releases/tag/v2x-test-2026.10.12) 下载 4 个 `DFW-V2X-2026-10-12.zip.part-01` 至 `part-04` 分卷。把它们放在同一目录后合并并校验，再解压：

```sh
cat DFW-V2X-2026-10-12.zip.part-* > DFW-V2X-2026-10-12.zip
shasum -a 256 -c DFW-V2X-2026-10-12.zip.sha256
unzip DFW-V2X-2026-10-12.zip
```



```sh
npm ci
npm start
```

需要 Node.js 22 或更新版本。打开 <http://localhost:4173/full-game-06/> 开始游戏。手机及其他设备可通过运行服务电脑的局域网 IP 访问；跨互联网多人游戏需要将 Node.js 服务部署到支持 HTTPS 与 WebSocket 的主机。

GitHub Releases 保存可下载发行包，不托管实时游戏后端。该服务端使用单进程房间存档，当前没有为高并发或持续运营部署。

## 测试版资料

- 发布说明、运行步骤和 165 个离线资源的逐项校验值随压缩包提供。
- 本次工作树全量检查：生产资源构建成功，自动化测试 148/148 通过；下载包重装依赖后，165 个离线资源的哈希检查和两人 WebSocket 同房协议模拟通过。
- 这是测试发行版，不代表真机、弱网、高并发或持续运营验收。
- 仓库没有授予游戏原始素材的通用再许可。地图及数据来源和限制见 [DATA-SOURCES.md](DATA-SOURCES.md)；依赖和第三方说明见 [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md)。

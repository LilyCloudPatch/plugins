# TH15 skipgame 来源与分发说明

资源：Touhou Patch Center / skipgame contributors 的 “Skip gameplay sections”，
TH15 Stage 1–7 七个 ECL。上游与说明：

- https://srv.thpatch.net/skipgame/
- https://www.thpatch.net/wiki/Patch:Skipgame
- https://www.thpatch.net/wiki/Touhou_Patch_Center:Servers
- 许可：https://creativecommons.org/licenses/by-sa/4.0/

2026-10-14 的独立核查：官方 Servers 页面声明该站内容与服务器上的翻译/图片使用
CC BY-SA 4.0；官方 Skipgame 页面独立列出 TH15 七个替换 ECL。由站点内容许可及
文件来源作出适用同协议的判断，与 TH14 的许可解释一致，不声称取得了额外的个别作者
授权。当前 wiki HTML/API 直连返回 403；可检索的官方页面内容和资源服务器可读取。
七个 `https://srv.thpatch.net/skipgame/th15/st0N.ecl` 已直接从官方服务器读取到内存，
长度和 SHA-256 均逐项符合本目录 import-lock.json；没有使用第三方转贴作为依据。

LilyPatch 交付这些资源时保留上游内容字节，以独立 SQLite DB 封装，使用同一
CC BY-SA 4.0 许可、署名及上述来源链接。没有改写上游 ECL 文件；运行时中文符卡名
由 LilyPatch 的格式终端在资源载入后转换。没有声明上游认可或背书 LilyPatch。
资源许可证不要求使用 LilyPatch；签名仅用于本客户端的来源验证，不限制资源在
许可证允许的范围内提取、再利用或再分发。游戏原档案与第三方补丁可执行代码不交付。

公开插件仓的 README 须包含本说明。发布工具在输出树中交付署名文本；不能因
资源已经本地实测或已经签名而省略来源、许可或同协议说明。

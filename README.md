# LilyCloudPatch/plugins

这是集成发布仓，插件源仓保持独立。根 plugins.json / plugins.sig 提供已签名的
插件元信息与精确支持版本；插件名/游戏/files.json 提供下载路径、SHA-256 与长度。
该文件由根索引锁定哈希和长度。资源在插件名/游戏/files/ 下，规范内容 manifest
与其 Ed25519 proof 也位于同一游戏目录。main 是 release，dev 是 dev。
所有客户端使用插件仓根 URL，不读取旧的游戏名/插件名布局。
包保持原始语义清单、Blob 和 guard；基础汉化在各游戏翻译仓，私钥永不入仓。

## TH08 skipgame 署名与许可

# TH08 skipgame 来源与分发说明

资源：Touhou Patch Center / skipgame contributors 的 “Skip gameplay sections”，
TH08 18 个 ECL（九个关卡名各含普通与 sp 版本）。上游与说明：

- https://srv.thpatch.net/skipgame/
- https://www.thpatch.net/wiki/Patch:Skipgame
- https://www.thpatch.net/wiki/Touhou_Patch_Center:Servers
- 许可：https://creativecommons.org/licenses/by-sa/4.0/

2026-10-15 的独立核查：官方 Servers 页面声明该站内容与服务器上的翻译/图片使用
CC BY-SA 4.0；官方 Skipgame 页面独立列出 TH08 18 个替换 ECL。由站点内容许可及
文件来源作出适用同协议的判断，与 TH14 的许可解释一致，不声称取得了额外的个别作者
授权。当前 wiki HTML/API 直连返回 403；可检索的官方页面内容和资源服务器可读取。
18 个 `https://srv.thpatch.net/skipgame/th08/ecldata*.ecl` 已直接从官方服务器读取到内存，
长度和 SHA-256 均逐项符合本目录 import-lock.json；没有使用第三方转贴作为依据。

LilyPatch 交付这些资源时保留上游内容字节，以独立 SQLite DB 封装，使用同一
CC BY-SA 4.0 许可、署名及上述来源链接。没有改写上游 ECL 文件。没有声明上游认可或背书 LilyPatch。
资源许可证不要求使用 LilyPatch；签名仅用于本客户端的来源验证，不限制资源在
许可证允许的范围内提取、再利用或再分发。游戏原档案与第三方补丁可执行代码不交付。

公开插件仓的 README 须包含本说明。发布工具在输出树中交付署名文本；不能因
资源已经本地实测或已经签名而省略来源、许可或同协议说明。

TH08 包保留九份与原资源相同的 sp 文件，以对应上游完整清单。仅导入 ECL；上游
time_factor 二进制修改不在包或运行时中。

2026-10-16 用户确认包发现、启用与游戏内基本跳关通过；未提供具体关卡/路线，保留
独立回归范围。当时仍为本地测试签名产物，此反馈本身不自动授权公开发布。
2026-10-18用户另行明确授权推进TH08在线闭环，现已使用既有正式plugin锚签发，
以LilyCloudPatch/plugins中的thpatch-skipgame/th08变体发布；验收及版本见本作ONLINE/TESTING。

# LilyCloudPatch/plugins

这是集成发布仓，插件源仓保持独立。根 plugins.json / plugins.sig 提供已签名的
插件元信息与精确支持版本；插件名/游戏/files.json 提供下载路径、SHA-256 与长度。
该文件由根索引锁定哈希和长度。资源在插件名/游戏/files/ 下，规范内容 manifest
与其 Ed25519 proof 也位于同一游戏目录。main 是 release，dev 是 dev。
所有客户端使用插件仓根 URL，不读取旧的游戏名/插件名布局。
包保持原始语义清单、Blob 和 guard；基础汉化在各游戏翻译仓，私钥永不入仓。
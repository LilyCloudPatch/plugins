# LilyCloudPatch/plugins

跨游戏第三方插件发布仓（上游跟随型：alphes 类立绘包等）。设计定案见
`../LilyPatch/docs/CONTENT_CHANNEL.md` 的「插件仓库」章节与 `../LilyPatch/docs/SIGNING.md`
的密钥拓扑。

## 仓库角色

- 本仓是**纯发布目标**：只接受 `publish-channel.ps1`（`-Game` 作用域化后）写入的 staged
  内容，不接受手工提交的包、资源或工具。基础翻译在各自的游戏仓（`LilyCloudPatch/th14` …），
  不在本仓。
- 频道由分支表达：`main` = release，`dev` = dev。URL 一律用显式分支链接
  （`https://fastly.jsdelivr.net/gh/LilyCloudPatch/plugins@main`）。
- 由 **plugin 锚**（独立的 Ed25519 密钥，与各翻译仓的 base 锚严格分域）签名的
  `packages.json` / `packages.sig` 是唯一下载授权。

## 布局（每个游戏一棵子树）

```text
<game_id>/
├── packages.json / packages.sig          插件目录（schema v2，plugin 锚分离签名）
├── packages/<id>.<content-hash>.db       single 交付：整文件签名包
└── objects/<xx>/<sha256>                 objects 交付：内容寻址 Blob 池
```

## 纪律

- `.gitattributes` 固定 `* -text`：任何行尾规范化都会废掉分离签名（th14 仓首次上线事故）。
- 上游资产永远不直接入仓；入仓的是导入锁定清单放行、由我们的密钥签名的 DB 或其拆出的对象。
- 发布后必跑 `verify-published-channel.ps1`（按启动器的真实消费方式全量下载验证）。

当前状态：空仓。首个插件域包（alphes 类）接入时按阶段一初始化目录结构。

# 三国全战抗战 mod

以《全面战争：三国》为底的抗日战争（1937–1945）全面改造 mod。

- 设计文档：[三国全战抗战 mod 设计文档](https://claude.ai/artifact/X5bWAeM9dVEYmC7tQJaPkc)（Claude 文档，默认只有作者能打开，给合作者看之前要在页面的分享菜单里开启分享）
- 当前阶段：M0 · 熟悉工具链
- 路线图：M0 工具链 → M1 战斗原型 / M2 战役原型（并行）→ M3 首个可玩版本 → M4 公开测试与发布，详见设计文档

## 目录结构

| 目录 | 用途 |
| --- | --- |
| `packs/` | mod 源文件。每个子文件夹对应一个 .pack，内部结构和 pack 保持一致（`db/`、`text/db/`、`script/`、`ui/` 等），用 RPFM 打包 |
| `packs/kz_m1_rifle/` | M1 战斗原型：一个步枪兵单位 |
| `packs/kz_m2_campaign/` | M2 战役原型：城市改名、势力与开局 |
| `art/portraits/` | 人物立绘源文件 |
| `art/icons/` | 兵种卡、技能等图标源文件 |
| `art/models/` | 3D 模型源文件（Blender） |
| `art/textures/` | 贴图源文件 |
| `docs/research/` | 史料、地名核对、兵器资料 |
| `reference/` | 从原版导出的数据表和脚本，只在本地对照用，不提交、不发布 |
| `tools/` | 辅助脚本，例如批量生成数据表和本地化文本 |
| `build/` | 打包输出的 .pack，测试时复制到游戏的 `data` 目录 |

正式版的 pack 到 M3 阶段再建。

## 约定

- 路径和文件名只用英文小写字母、数字和下划线，不用中文和空格；部分 mod 工具处理中文路径会出错。
- 新增的数据库键名和脚本文件名统一加前缀 `kz_`，避免和原版或其他 mod 冲突。前缀等 mod 定名后可以再改。
- 只用自制或已获授权的素材，不从其他游戏移植模型、动画和音效。
- `reference/` 里的原版数据只在本地对照，不放进 pack，也不上传。

## 工具

- [RPFM（Rusted PackFile Manager）](https://github.com/Frodo45127/rpfm)：编辑 pack、数据表、本地化文本和 Lua 脚本
- 官方 Assembly Kit（Steam 的"工具"库）：修改开局设置（startpos）
- Blender：3D 模型

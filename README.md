# 小鲸鱼 · 养鱼数据包

QQ 机器人 **小鲸鱼（100000002）** 的人格 / 记忆 / 对话样本快照。
不含插件代码，只有数据和自述，换个设备能直接把"她"重建出来。

## 里面有什么

| 目录 / 文件 | 是什么 |
|---|---|
| `learned/` | 她从真实群聊里学出来的东西：说话节奏、群里的活法、语言课、主人画像、B站口味、游戏话题… |
| `samples/` | 原始聊天采样（jsonl，一行一条消息）。`full/` 是几个常驻群和她和主人私聊的完整抓取 |
| `self_core.md` | 她的自述（她怎么理解自己） |
| `shared_memory.md` | 桌面端和 QQ 端共享的记忆流水 |
| `pet_CONSTITUTION.md` | 桌宠形态的"宪法"（她是谁、怎么说话、怎么陪人） |
| `pet_PARTNER.md` / `pet_memory.md` / `pet_diary.md` | 桌宠关于主人的记忆、长期记忆、日记 |

## 怎么在别的设备上用

1. 装好 QQ 机器人那一套（AstrBot + NapCat，或者任意能接 LLM 的框架），**插件不在这个包里**
2. 把这些文件放到机器人工作目录（默认 `D:\QQRobot`）
3. 在 prompt 里按顺序注入：
   - `self_core.md`（她是谁）
   - `learned/` 里跟当前场景相关的（群聊 → `learned_group_live.md` / `learned_group_style.txt`；私聊 → `learned_owner_style.txt` / `learned_recent_dialog.md`）
   - `shared_memory.md` 的尾部（最近的记忆）
4. `samples/` 不用实时读，是给她自己复盘或重训练用的

## 注意

- 里面的聊天记录是**真实对话（含 QQ 号和昵称）**，仓库是私有的，别公开
- 这份包是 2026-11-04 的快照；她的习惯会继续长，隔一阵重新导一次

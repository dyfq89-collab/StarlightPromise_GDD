# 🌌 Starlight Promise

# Technical Architecture Document

版本：1.0


# 1. 项目技术概述


项目名称：

Starlight Promise


游戏类型：

2D剧情探索RPG


开发语言：

Python 3.12


游戏框架：

Kivy


目标平台：

Android


打包工具：

Buildozer



---

# 2. 项目结构


最终代码结构：


StarlightPromise/


├── main.py


├── game/


│   ├── game_manager.py


│   ├── player.py


│   ├── map_manager.py


│   ├── npc_manager.py


│   ├── quest_manager.py


│   ├── item_manager.py


│   ├── save_manager.py


│   └── dialog_manager.py



├── screens/


│   ├── menu_screen.py


│   ├── game_screen.py


│   ├── inventory_screen.py


│   ├── dialog_screen.py


│   └── ending_screen.py



├── data/


│   ├── quests.json


│   ├── items.json


│   ├── npc.json


│   ├── dialogs.json


│   └── maps.json



├── assets/


│   ├── images/


│   ├── sounds/


│   ├── music/


│   └── fonts/


├── saves/


└── requirements.txt



---

# 3. 核心模块设计



# GameManager


作用：

游戏总控制器。


负责：

- 初始化游戏
- 管理状态
- 控制场景切换



---

# Player


玩家系统。


负责：

- 玩家位置
- 移动
- 状态
- 背包



---

# MapManager


地图管理。


负责：

- 加载地图
- 场景切换
- 碰撞检测



---

# NPCManager


NPC管理。


负责：

- NPC生成
- NPC互动
- 对话触发



---

# DialogManager


对话系统。


负责：

- 显示文本
- 角色头像
- 剧情推进



---

# QuestManager


任务系统。


负责：

- 创建任务
- 更新任务状态
- 判断完成条件



---

# ItemManager


物品系统。


负责：

- 添加物品
- 删除物品
- 查询物品



---

# SaveManager


存档系统。


负责：

保存：

- 玩家位置
- 任务进度
- 物品
- 剧情状态



---

# 4. 游戏运行流程



启动：

main.py


↓

加载资源


↓

初始化GameManager


↓

进入MainMenu


↓

开始游戏


↓

加载地图


↓

玩家探索


↓

触发剧情


↓

保存进度



---

# 5. 数据驱动设计


所有剧情数据：

JSON管理。


禁止：

直接写死剧情。



例如：

dialogs.json


{
"id":"luma_001",

"speaker":"Luma",

"text":"欢迎来到星光世界"
}



---

# 6. 场景管理


使用：

Kivy ScreenManager



页面：


MainMenuScreen


GameScreen


DialogScreen


InventoryScreen


QuestScreen


EndingScreen



---

# 7. 安卓适配要求



必须支持：

- 触摸操作
- 横屏
- 不同分辨率
- 性能优化



目标：

稳定运行60FPS。



---

# 8. 开发原则



1.

模块独立。


2.

代码必须注释。


3.

禁止单文件超过500行。


4.

功能完成必须测试。


5.

保持后期可扩展。



---

# 9. 最终功能目标



游戏必须包含：


✅ 玩家移动


✅ 地图探索


✅ NPC互动


✅ 对话系统


✅ 任务系统


✅ 背包系统


✅ 存档系统


✅ 最终生日动画



---

版本：

v1.0

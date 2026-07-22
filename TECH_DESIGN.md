# 技术设计


## 技术栈


Python

Kivy


---

# 架构


main.py

↓

GameController


↓

----------------

Player

MapManager

EventManager

StoryManager

ItemManager


----------------


↓

Views


MapView

GameScreen

Dialog


---


# 模块职责


## Player

负责：

- 玩家坐标
- 移动


---

## MapManager

负责：

- 地图数据
- Tile


---

## EventManager

负责：

- 事件触发


---

## StoryManager

负责：

- 剧情


# Don't Drop — Unity WebGL

《Don't Drop》是一款轻松有趣的本地多人派对对战游戏。玩家在悬浮平台上移动、跳跃和攻击，利用随机掉落的道具把对手击落；每位玩家初始拥有 3 条生命，最后存活的玩家获胜。

本仓库包含项目展示页、Unity WebGL 可玩构建、游戏截图和策划展示文档。

## 在线内容

- 项目主页：打开根目录的 `index.html`
- 开始游戏：进入 `game/index.html`
- 游戏策划展示：`docs/game-pitch.pdf`
- 演示视频：[哔哩哔哩](https://www.bilibili.com/video/BV1xsQMBfEtf/)

## 游戏特色

- 2–4 人本地同屏对战
- 移动、二段跳、下平台与攻击操作
- 鞋子、红心、剑等随机道具
- 快节奏、易上手的聚会玩法

## 操作说明

| 玩家 | 移动 | 跳跃 | 下平台 | 攻击 |
| --- | --- | --- | --- | --- |
| 玩家一 | `A` / `D` | `W`（二段跳） | `S` | `F` |
| 玩家二 | `←` / `→` | `↑`（二段跳） | `↓` | 右 `Ctrl` |
| 玩家三、四 | 手柄摇杆 | 手柄按键 | 手柄按键 | South 键（Xbox 手柄为 `A`） |

- 按 `R` 重新开始游戏。
- 在选人界面按攻击键加入，再次按攻击键确认；所有玩家确认后进入选图。

## 本地运行

Unity WebGL 构建不能直接通过 `file://` 协议正常加载，请在仓库根目录启动一个本地 HTTP 服务：

```bash
python -m http.server 8000
```

然后访问 <http://localhost:8000/>。也可以使用任意静态文件服务器，例如 VS Code Live Server。

## 项目结构

```text
.
├── index.html                  # 项目展示主页
├── assets/
│   └── images/                 # Logo 与游戏截图
├── docs/
│   └── game-pitch.pdf          # 游戏策划展示
└── game/
    ├── index.html              # Unity WebGL 入口
    ├── Build/                  # Unity WebGL 构建产物
    ├── StreamingAssets/        # Unity StreamingAssets
    └── TemplateData/           # Unity WebGL 页面资源
```

## 开发团队

- 张健源（Zhang Jianyuan），西安交通大学
- 王议甲（Wang Yijia），西安交通大学
- 刘远浩（Liu Yuanhao），西安交通大学
- 李欣泽（Li Xinze），西安交通大学

## 技术栈

- Unity WebGL
- HTML / CSS / JavaScript

## 说明

`game/Build/` 中包含体积较大的 Unity WebGL 二进制文件。克隆和首次加载可能需要一些时间。


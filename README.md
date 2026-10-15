---
AIGC:
    Label: "1"
    ContentProducer: 001191440300708461136T1XGW3
    ProduceID: 834947731de00f8150b35d33817278ca_7ffc8f38c7d711f1b5a6525400393706
    ReservedCode1: YUlbSlw5ZMfPS9ZKrcgoqGopumc0cBmLsimwwLdeEOMqregs+SPyq7qgDnkhp7l79VY+/bnFwNasrumhaLgr/pN7/xfzCgoVMaWgDoWZtjYU0wMRRtovB/3lOCkZygBjK6k59CYB2TGTp1Mi2AF9+zB16YBxwzTdk3e6IpSgApeYkvsw+Z9+bPU5ayo=
    ContentPropagator: 001191440300708461136T1XGW3
    PropagateID: 834947731de00f8150b35d33817278ca_7ffc8f38c7d711f1b5a6525400393706
    ReservedCode2: YUlbSlw5ZMfPS9ZKrcgoqGopumc0cBmLsimwwLdeEOMqregs+SPyq7qgDnkhp7l79VY+/bnFwNasrumhaLgr/pN7/xfzCgoVMaWgDoWZtjYU0wMRRtovB/3lOCkZygBjK6k59CYB2TGTp1Mi2AF9+zB16YBxwzTdk3e6IpSgApeYkvsw+Z9+bPU5ayo=
---

# 计算器（Calculator）

<p align="center">
  <a href="#中文文档"><b>中文</b></a> ·
  <a href="#english-documentation"><b>English</b></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/platform-macOS%2015.7%2B-lightgrey" alt="Platform: macOS 15.7+">
  <img src="https://img.shields.io/badge/UI-SwiftUI%20%2B%20AppKit-blue" alt="SwiftUI + AppKit">
  <img src="https://img.shields.io/badge/language-%E4%B8%AD%E6%96%87%20%2F%20English-green" alt="中文 / English">
  <img src="https://img.shields.io/github/v/release/f8r4ksv7v4-hub/Calculator?label=release&color=orange" alt="Release">
  <img src="https://img.shields.io/badge/license-MIT-brightgreen" alt="License: MIT">
</p>

<a id="中文文档"></a>

## 中文文档

计算器是一款 macOS 桌面计算器应用，基于 SwiftUI + AppKit 开发。它把日常计算、汇率换算、单位换算、进制转换、实验数据绘图（二维 / 极坐标 / 三维）与番茄钟收进一个「圆盘 + 计算窗口」的两级悬浮界面，所有计算都在本地完成，仅在汇率换算与检查更新时访问网络。

> 本项目由 **f8r4ksv7v4-hub** 原创开发与维护，界面与全部功能均为原创实现。仓库仅提供说明文档与官方安装包，不提供源码。

- **English documentation**: [English Documentation](#english-documentation)

### 界面预览

<p align="center">
  <img src="docs/screenshots/01-app-icon.jpg" width="110" alt="App 图标">
</p>

<table align="center">
  <tr>
    <td align="center"><img src="docs/screenshots/02-wheel-menu.jpg" width="320" alt="圆盘主菜单"><br><sub>圆盘主菜单</sub></td>
    <td align="center"><img src="docs/screenshots/03-scientific-exchange.jpg" width="320" alt="科学计算与汇率换算"><br><sub>科学计算与汇率换算</sub></td>
    <td align="center"><img src="docs/screenshots/04-pomodoro-base.jpg" width="320" alt="番茄钟与进制转换"><br><sub>番茄钟与进制转换</sub></td>
  </tr>
  <tr>
    <td align="center"><img src="docs/screenshots/05-polar-fit.jpg" width="320" alt="极坐标绘图与数据拟合"><br><sub>极坐标绘图与数据拟合</sub></td>
    <td align="center"><img src="docs/screenshots/06-3d-spiral.jpg" width="320" alt="三维空间螺旋曲线"><br><sub>三维空间螺旋曲线</sub></td>
    <td align="center"><img src="docs/screenshots/01-app-icon.jpg" width="320" alt="App 图标"><br><sub>App 图标</sub></td>
  </tr>
</table>

### 版本说明

| 版本 | 圆盘项数 | 主要差异 |
| --- | --- | --- |
| **2.3**（当前开发版本） | 12 | 在 2.0 之上新增：绘图的**多图线**（同一张图内多条曲线，逐线数据 / 颜色 / 拟合）、**导出 CSV**（多线分列并汇总逐线拟合结果）、三维**导出 OBJ**，以及各二级窗口右上角的 **i 使用说明** 面板 |
| 2.0 | 12 | 在 1.0 全部功能之上新增「番茄钟」：独立窗口、左下角剩余时间胶囊、到时提醒 |
| 1.0 | 11 | 普通 / 科学 / 汇率 / 重量 / 温度 / 面积 / 速度 / 时间 / 存储 / 进制 / 绘图 |

> 说明：当前 [Releases](https://github.com/f8r4ksv7v4-hub/Calculator/releases) 页面提供的官方安装包为 **2.0** 与 **1.0**；2.3 的安装包随后续 Release 提供。应用内的「检查更新」只会下载 Release 中名称含 `macOS` 的 zip 资产。

### 功能特性

- **圆盘两级交互**：第一级为悬浮圆盘（2.0 起为 12 项模式），第二级为计算窗口；圆盘中心按钮可让圆盘收缩消失并隐藏窗口
- **普通计算**：四则运算、百分号、多层括号嵌套
- **科学计算**：sin / cos / tan、log、ln、√、x²、x!、π、e，角度与弧度可切换
- **汇率换算**：以人民币为基准在线获取实时汇率，离线时使用本地缓存
- **单位换算**：重量、温度、面积、速度、时间、存储六类
- **进制转换**：二进制 / 八进制 / 十进制 / 十六进制，输入即时换算
- **实验数据绘图**：
  - 二维图像：手动录入或表格导入数据点，折线 / 光滑曲线，线性、二次、三次、四次、五次、指数、对数、幂律、正弦等拟合并给出 R² / RMSE；支持数据变换（ln x、ln y、log10 x、log10 y、1/x、1/y、y 归一化）、对数轴、范围锁定、平滑强度、双游标、切线、误差棒、波峰 / 波谷标注、均值线、面积、坐标标签、自定义图表标题与坐标轴名称单位
  - 极坐标图：输入关于角度 t 的半径表达式，设定角度范围与采样数，附带同心圆网格、角度线与角度标签
  - 三维图像：表达式曲面 z = f(x, y) 或三维数据点（曲面网格 / 空间线）；拖动旋转、缩放；拟合平面、外推、切平面、两点测量；x / y / z 轴名称、点坐标标签、均值面、误差棒、范围锁定
  - **多图线（2.3）**：同一张图内可添加多条图线，逐线独立的数据、颜色、显示与拟合配置，图例与逐线拟合结果一并绘制与导出
  - 曲线数字化（从图片提取数据点）、绘图历史（可恢复数据与设置重新生成）
  - 导出 PNG（屏幕所见即导出所见）、导出 CSV（数据点与拟合结果）、三维导出 OBJ
- **番茄钟（2.0）**：工作 / 休息时长可自定义（默认 25 / 5 分钟自动循环）；工作结束与休息结束的提醒方式各自独立配置（静音 / 震动 / 响铃 / 响铃 + 震动，响铃与震动强度可调），到时有屏幕边缘光晕呼吸提示；收起后左下角小角常驻显示剩余时间胶囊，可直接开始 / 暂停
- **使用说明面板（2.3）**：各二级窗口右上角的 **i** 按钮可打开中英双语使用说明，覆盖圆盘交互、快捷键、二维 / 极坐标 / 三维绘图、多图线、番茄钟、自动更新与设置
- **历史记录**：普通与科学模式保留最近 20 条计算历史，重启后仍在
- **中英双语**：界面一键切换中文 / English，即时生效
- **外观与触发**：跟随系统深浅色或手动固定；可隐藏 Dock 图标，仅保留屏幕左下角触发展开
- **自动更新**：基于 GitHub Releases 自动检查、下载并原位安装新版本

### 环境要求

- macOS 15.7 或更高版本
- Apple Silicon（arm64）Mac

### 下载

| 版本 | 安装包 | 大小 | 下载直链 |
| --- | --- | --- | --- |
| **2.0**（推荐） | `Calculator-2.0-macOS.zip` | 约 2.0 MB | [下载](https://github.com/f8r4ksv7v4-hub/Calculator/releases/download/v2.0/Calculator-2.0-macOS.zip) |
| 1.0 | `Calculator-1.0-macOS.zip` | 约 1.9 MB | [下载](https://github.com/f8r4ksv7v4-hub/Calculator/releases/download/v1.0/Calculator-1.0-macOS.zip) |

全部版本与更新日志见 [Releases](https://github.com/f8r4ksv7v4-hub/Calculator/releases) 页面。

### 安装与首次启动

1. 打开本仓库的 [Releases](https://github.com/f8r4ksv7v4-hub/Calculator/releases) 页面，下载对应版本的安装包（`Calculator-2.0-macOS.zip` 或 `Calculator-1.0-macOS.zip`）
2. 双击解压得到「计算器.app」，拖入「应用程序」文件夹
3. **首次启动会被 Gatekeeper 拦截**：安装包为开发者签名、未经 Apple 公证，系统会提示「无法验证开发者」或「Apple 无法检查其是否包含恶意软件」。按以下任一方式放行即可：
   - 在「访达」中 **按住 Control 点击（或右键）**「计算器.app」→ 选择「打开」→ 在弹窗中再次点击「打开」
   - 若仍被阻止：打开 **系统设置 → 隐私与安全性**，在「安全性」一栏中点击 **「仍要打开」**，然后重新打开应用
   - 若上述方式仍无效，打开「终端」执行以下命令后再启动（移除下载隔离标记）：
     ```bash
     xattr -dr com.apple.quarantine /Applications/计算器.app
     ```
4. 首次运行会请求网络访问权限（用于获取汇率与检查更新），允许即可；拒绝不影响计算与绘图功能

### 使用方法

#### 第一级：圆盘

启动应用后显示第一级悬浮圆盘，圆盘上按顺时针依次排列各功能模式（2.0 起依次为：普通、科学、汇率、重量、温度、面积、速度、时间、存储、进制、绘图、番茄钟）。

- 点击任意模式图标 → 圆盘收缩，进入第二级对应页面
- 点击圆盘中心按钮 → 圆盘向中心收缩消失，并隐藏窗口

#### 第二级：计算窗口

- 顶部左侧「返回」→ 回到第一级圆盘
- 顶部右侧分别为「收起」与「设置」；2.3 起「设置」左侧另有 **i** 使用说明入口
- 点击「收起」（或按 ⌘W / ↓）→ 窗口缩为屏幕左下角的小角
- 恢复窗口：把鼠标移到**屏幕最左下角**停留片刻露出小角，点击即可展开

#### 绘图

1. 圆盘选择「绘图」，窗口会自动加宽
2. 顶部切换「二维图像 / 极坐标图 / 三维图像」
3. 二维与三维在「数据 / 图表 / 工具」功能区中录入数据（手动添加或导入表格）、设置图表样式与拟合、显示元素与标注
4. 极坐标图输入半径表达式，并设定角度范围与采样数
5. 完成后可导出 PNG（二维另有 CSV，三维另有 OBJ）；导出记录进入绘图历史，可恢复数据与设置重新生成

#### 番茄钟（2.0）

1. 圆盘选择「番茄钟」，打开独立窗口
2. 在窗口内设定工作 / 休息时长与到时提醒方式，点击开始即可计时
3. 点击「收起」→ 番茄钟窗口隐藏，左下角小角**常驻显示剩余时间胶囊**：胶囊上的按钮可直接开始 / 暂停，点击胶囊其它区域恢复番茄钟窗口
4. 点击「返回圆盘」→ 回到第一级圆盘

### 绘图功能按钮位置与功能

> 以下按「顶部切换 → 二维（数据 / 图表 / 工具）→ 极坐标 → 三维（数据 / 图表 / 工具）→ 多图线 → 导出 → 图像标定取点」逐项说明每个按钮、输入框与开关在界面中的位置与作用（对应 2.3 版界面）。

#### 顶部：绘图模式切换

| 位置 | 控件 | 作用 |
| --- | --- | --- |
| 绘图面板第一行左侧 | 三档分段控件「二维图像 / 极坐标图 / 三维图像」 | 切换绘图类型；切换后下方的功能区与图表整体替换 |
| 同一行右侧 | 灰色提示文字 | 提示当前模式可用能力：「支持拟合/外推/测量/切线/误差棒/对数轴/变换」（二维）、「用 t（或 θ）表示角度，支持 sin/cos/exp/sqrt 等」（极坐标）、「等距投影曲面；数据点可画面或空间线，可导出 PNG」（三维） |
| 第二行 | 页签「数据 / 图表 / 工具」（二维与三维） | 功能区分组标签，选中项以强调色加粗并带底部指示条 |

#### 二维图像 · 数据页

| 位置 | 控件 | 作用 |
| --- | --- | --- |
| 第一行 | 「横轴」+ 输入框（提示「如 时间/s」） | 设置 X 轴名称 / 单位，显示在坐标轴旁，导出 PNG 同样使用 |
| 第一行 | 「纵轴」+ 输入框（提示「如 电压/V」） | 设置 Y 轴名称 / 单位 |
| 第二行左起 | `x` 输入框 | 待添加数据点的 x 值 |
| 第二行 | `y` 输入框 | 待添加数据点的 y 值 |
| 第二行 | `±` 输入框（提示「误差(可选)」） | 该点的 y 方向误差，用于误差棒；留空则该点无误差 |
| 第二行 | 圆形 **+** 按钮 | 把 x / y / 误差写入当前图线的数据点列表 |
| 第二行 | 圆形垃圾桶按钮 | 清空当前图线的全部数据点 |
| 第二行 | 圆形下载图标（弹出菜单） | 数据导入入口，三个选项：**导入到当前图线（表格）**（按 `x,y[,err]` 解析，写入当前图线）、**一次导入为多条图线（整表）**（首列为 x，其余每个数值列各生成一条图线）、**导入图像并标定取点** |
| 第二行右侧 | 胶囊按钮「**增加图线**」（+） | 2.3 新增：在当前图中新增一条图线，新线拥有独立的数据、颜色与拟合配置 |
| 数据点下方（仅当图线 **≥2** 条时出现） | 「图线」管理栏 + 图线胶囊 | 点击胶囊切换当前图线；胶囊显示线色、线名与显隐状态（单图线时该栏不出现，界面与 2.0 一致） |
| 图线管理栏 | 「图例」开关 | 显示 / 隐藏图表图例；图例逐线列出线名、颜色与拟合表达式 |
| 图线管理栏「当前」行 | 「图线名称」输入框 | 重命名当前图线，留空恢复「图线 N」自动命名 |
| 「当前」行 | 「颜色」菜单 | 修改当前图线的颜色（同一张图内多线不同色） |
| 「当前」行 | 「显示」按钮 | 单独显示 / 隐藏该图线（仅不绘制，数据保留） |
| 「当前」行 | 「拟合」按钮 | 勾选后该线的拟合结果绘制到图上并显示在图例中 |
| 「当前」行最右 | 删除按钮 | 删除当前图线（至少保留一条） |
| 图线管理栏下方 | 数据点列表 | 逐行编辑 x / y / 误差；眼睛按钮排除或恢复该点（排除点不绘制、不参与拟合 / 统计 / 面积）；行末按钮删除该点 |
| 列表为空时 | 提示文字 | 「暂无数据点，请在上方输入 x、y 后点击 + 添加」 |

#### 二维图像 · 图表页

| 位置 | 控件 | 作用 |
| --- | --- | --- |
| 第一行 | 「图表名称」输入框（提示「留空则不显示标题」） | 设置显示在图表顶部的标题；屏幕与导出 PNG 同源，输入即时生效 |
| 第二行 | 绘图类型胶囊「折线 / 光滑曲线」 | 选择曲线的绘制方式 |
| 第二行 | 「外推」按钮 | 显示拟合曲线在数据范围之外的延伸（浅虚线）；关闭时只画数据范围内的拟合曲线 |
| 第二行 | 拟合类型菜单 | 选择拟合函数形式（线性、二次、三次、四次、五次、指数、对数、幂律、正弦等） |
| 第三行 | 「显示元素」折叠按钮 | 展开 / 收起下方开关组 |
| 折叠面板内 | 「特征点 / 拟合结果 / 均值线 / 面积 / 误差棒 / 点坐标」六个眼睛按钮 | 逐项显示或隐藏对应元素；2.3 起这些开关**逐线独立**（写回当前图线） |
| 特征点开启且有峰谷时 | 特征点按钮列表 | 每个波峰 / 波谷一个按钮，可单独显示或隐藏该特征点 |
| 图表页工具行 | 「x 轴 / y 轴」对数按钮 | 坐标轴刻度在线性 / 对数之间切换（对数仅对对应方向 > 0 的数据有效） |
| 图表页工具行 | 「平滑」三档 | 设置光滑曲线的平滑强度 |
| 图表页工具行 | 「变换」菜单 | 对数据应用 ln x、ln y、log10 x、log10 y、1/x、1/y、y 归一化 0-1；仅影响显示与拟合，原始数据保留、可随时撤销 |
| 面板下方（只读） | 数据统计面板 | 显示点数 N、最小、最大、均值、标准差 σ（总体，÷N） |
| 面板下方（只读） | 拟合结果摘要 | 显示拟合表达式、R²、RMSE |

#### 二维图像 · 工具页

| 位置 | 控件 | 作用 |
| --- | --- | --- |
| 第一行 | 「测量」按钮 | 开启双游标测量：拖动图上 A / B 游标吸附数据点，实时显示坐标与 Δx / Δy |
| 第一行 | 「切线」按钮 | 开启切线：点击图上数据点显示该点切线斜率，再次点击取消 |
| 第一行 | 「绘图历史」按钮 | 展开历史列表；每条含日期、点数、线型与拟合类型，可「重新生成」或删除该条 |
| 测量展开行 | 「A 游标」「B 游标」输入框（`x / x,y / ,y`）+「定位」按钮 + 恢复吸附按钮 | 用坐标直接定位游标；恢复按钮让游标回到吸附模式 |
| 切线展开行 | 「切点 x」输入框 +「添加」按钮 + 已添加切点标签 | 添加多条切线，标签上的按钮可删除单条切线；也可直接点击图上数据点添加 / 取消 |
| 第二行 | 「范围锁定」按钮 | 展开坐标范围输入行；已锁定时按钮显示「范围已锁定」 |
| 第二行 | 「等比缩放」按钮 | 让 x / y 轴上「1 个单位」的屏幕长度相等（与范围锁定互斥） |
| 范围锁定展开行 | 「x 范围」「y 范围」的最小 / 最大输入框 +「锁定当前范围」+「恢复自动」 | 手动输入坐标范围并锁定，或一键把当前自动范围写入并锁定；「恢复自动」清除锁定 |

#### 极坐标图

| 位置 | 控件 | 作用 |
| --- | --- | --- |
| 顶部 | 表达式输入框（提示「如 5*cos(2*t)、1+sin(t)」） | 输入半径关于角度的表达式 r = f(θ)，变量写作 t；支持 sin / cos / exp / sqrt 等函数 |
| 第二行 | 「θ 范围」起点 / 至 / 终点 | 设置角度范围 |
| 第二行 | 「步数」 | 设置采样点数，决定曲线平滑程度 |
| 第三行 | 「图表名称」输入框 | 设置极坐标图顶部标题，留空不显示 |
| 面板底部 | 「导出极坐标图」按钮 | 把当前极坐标曲线导出为 PNG（可选保存位置与文件名） |

#### 三维图像

三维数据源由面板顶部的胶囊按钮组切换：**表达式曲面** 与 **导入数据点**。

| 位置 | 控件 | 作用 |
| --- | --- | --- |
| 顶部 | 数据源胶囊「表达式曲面 / 导入数据点」 | 切换三维数据来源 |
| 表达式模式 | 表达式输入框（提示「如 sin(sqrt(x^2+y^2))、x*y/4」） | 输入曲面表达式 z = f(x, y) |
| 表达式模式 | x / y 范围输入框 +「采样」 | 设置自变量范围与网格采样数 |
| 表达式模式 | 「图表名称」输入框 | 设置曲面图标题 |
| 数据点模式 | 页签「数据 / 图表 / 工具」 | 与二维一致的功能区分组 |
| 数据点模式 | 右侧实时 3D 预览 | 三个页签共用同一交互式视图：拖动旋转、滚轮缩放，随拟合 / 切面 / 测量等开关联动刷新 |
| 数据 ● 第一行 | 「X 轴」「Y 轴」「Z 轴」输入框（提示「如 时间/s、距离/m、温度/℃」） | 设置三条坐标轴的名称 / 单位 |
| 数据 ● 第二行 | `x`、`y`、`z` 输入框 + `±` 误差输入框 | 待添加三维数据点的三个坐标与 z 方向误差（用于误差棒） |
| 数据 ● 第二行 | 圆形 **+** 按钮 / 圆形垃圾桶按钮 | 添加三维数据点 / 清空全部数据点 |
| 数据 ● 第二行 | 圆形下载图标（弹出菜单） | 「导入表格（CSV/TSV/TXT）」（需带 x、y、z 表头，大小写均可）与「导入图像并标定取点」 |
| 数据 ● 列表 | 数据点列表 | 逐行编辑 x / y / z / 误差（z 缺失显示 –）、排除或恢复、删除单点；无 z 值时面板给出提示 |
| 图表 ● 第一行 | 「图表名称」输入框 | 设置三维图标题 |
| 图表 ● 第二行 | 绘制方式胶囊「面 / 空间线」 | 数据点画成曲面网格或空间折线 |
| 图表 ● 第二行 | 「拟合平面」按钮 | 最小二乘平面拟合 z = a + b·x + c·y |
| 图表 ● 第二行 | 「外推」按钮 | 把拟合平面向数据范围外扩展 25%（虚线标出边界，需先开启拟合） |
| 图表 ● 第三行 | 「显示元素」折叠按钮 | 展开 / 收起「拟合平面 / 均值面 / 点坐标 / 误差棒」四个开关 |
| 图表 ● 第四行 | 「锁定范围」按钮 | 锁定当前 x / y / z 显示范围；展开后可填最小 / 最大值，或用「恢复自动」清空 |
| 工具 ● 第一行 | 「切平面」按钮 + (x, y) 输入 | 在指定 (x, y) 处绘制切平面（开启拟合时取拟合平面，否则用最近点局部拟合） |
| 工具 ● 第一行 | 「测量」按钮 + A / B 输入 | 输入两点坐标 (x, y, z)，显示两点间的三维距离 |
| 工具 ● 第一行 | 「绘图历史」按钮 | 展开三维绘图历史，可恢复数据与设置重新生成图片 |
| 面板底部 | 「导出图片」按钮 | 导出三维图 PNG |
| 面板底部 | 「导出 OBJ」按钮 | 导出 OBJ 网格模型，可在 Blender / MeshLab / Origin 等软件中打开 |

#### 多图线（2.3 新增）

- **入口**：数据页第二行右侧的「**增加图线**」胶囊按钮；每点击一次新增一条图线，新线自动分配颜色并成为当前图线
- **管理栏**：图中存在 **两条以上** 图线时，数据页出现「图线」管理栏（只有一条线时界面与 2.0 完全一致）
- **切换**：点击图线胶囊切换当前图线，各线的数据、颜色、变换与拟合互不影响
- **图例开关**：显示 / 隐藏图表图例，图例逐线列出线名、颜色与拟合表达式
- **当前图线行**：可重命名、改色、单独显隐（仅不绘制、数据保留）、勾选是否绘制该线的拟合曲线，或删除该图线（至少保留一条）
- **两种表格导入模式**：
  1. 「导入到当前图线（表格）」—— 单线模式，按 `x,y[,err]` 解析并写入当前图线
  2. 「一次导入为多条图线（整表）」—— 整表模式，第一列作为公共 x，其余每个数值列各生成一条图线，自动识别误差列
- **导出联动**：PNG 含图例与逐线拟合；CSV 多线时按线分列（`x1,y1,x2,y2…`，带误差的线追加 `errN`），并在文件末尾逐线汇总拟合表达式、R² 与 RMSE

#### 导出

| 位置 | 按钮 | 输出与说明 |
| --- | --- | --- |
| 二维面板底部 | 「导出图片」 | PNG，屏幕所见即导出所见（含图例与逐线拟合曲线），可选择保存位置与文件名 |
| 二维面板底部 | 「导出 CSV」 | 导出数据点与拟合结果为 CSV（可用 Excel 打开）；多图线时分列输出并附逐线拟合摘要 |
| 极坐标面板底部 | 「导出极坐标图」 | PNG |
| 三维面板底部 | 「导出图片」 | PNG |
| 三维面板底部 | 「导出 OBJ」 | OBJ 网格模型文件 |

导出完成后记录进入「绘图历史」，可一键调回当时的全部数据与配置重新生成图片。

#### 图像标定取点

从「导入」菜单选择「导入图像并标定取点」后打开标定窗口，操作提示为「双指捏合缩放 · 双指/鼠标拖拽平移 · 单击取点」，按四步完成：

1. 第 1 步：点击图像坐标原点 (0,0)
2. 第 2 步：点击 x 轴上一个刻度点，并填写它的刻度值
3. 第 3 步：点击 y 轴上一个刻度点，并填写它的刻度值
4. 第 4 步：依次点击曲线上的数据点（左侧列表可删除）

窗口内还有「重新标定」「清空取点」「完成导入」按钮与「已取 N 点」计数；窗口右上角即为 **i 使用说明** 入口。

### 使用说明面板（Information，2.3 新增）

2.3 起，三个二级窗口的**右上角「设置」按钮旁**（图像标定窗口在标题栏右侧）新增圆形的 **i** 按钮，点击打开中英双语「使用说明」面板，内容对应工程实际实现，共 11 个分区：

| 入口位置 | 说明 |
| --- | --- |
| 主计算窗口右上角 | 「设置」左侧的 **i** 按钮 |
| 番茄钟窗口右上角 | 「设置」旁的 **i** 按钮 |
| 图像标定取点窗口标题栏右侧 | **i** 按钮 |

面板分区：**圆盘与窗口**、**快捷键**、**绘图 · 总览**、**绘图 · 二维 · 数据页**、**绘图 · 多图线（2.3 新增）**、**绘图 · 二维 · 图表页**、**绘图 · 二维 · 工具页**、**极坐标图**、**三维图像**、**番茄钟**、**自动更新与设置**。面板标题栏右侧显示当前版本号，右下角「完成」关闭面板。

### 快捷键

| 快捷键 | 作用 |
| --- | --- |
| ⌘ , | 打开「设置」 |
| ⌘ W | 收起当前窗口为左下角小角 |
| ↓（向下方向键） | 收起当前窗口为左下角小角 |
| 0–9 / . , · 。 | 输入数字与小数点 |
| + - * / | 加、减、乘、除（键盘 × ÷ 同样识别） |
| = 或 Enter | 计算结果 |
| ( ) | 左、右括号（支持多层嵌套，中英文括号均可） |
| % | 百分号 |
| C | 清除当前输入 |
| Delete / Backspace | 退格（在括号末尾时智能删除括号） |
| 0–9、A–F（进制模式） | 按当前进制输入数字 |
| 0–9、.（汇率 / 单位换算模式） | 输入待换算数值 |

说明：第二级计算窗口内可直接用键盘输入；第一级圆盘下仅保留 ⌘W 收起。绘图模式下键盘数字与运算符不参与计算，输入由各输入框自行处理。

### 设置

**打开方式**（任一即可）：

- 第二级计算窗口顶栏右侧的「设置」按钮
- 菜单栏「计算器」→「设置…」（快捷键 ⌘,）

**设置内容**：

- 语言：中文 / English，切换后全界面立即生效，无需重启
- 通用：隐藏 Dock 图标（开启后应用从 Dock 消失，仅保留屏幕左下角触发）
- 外观模式：跟随系统 / 手动固定深浅色
- 关于：作者、版本、打赏作者、检查更新、问题反馈

### 自动更新

- 应用启动时自动检查一次 GitHub Releases 上的最新版本：发现新版本弹出「下载更新 / 稍后」，已是最新则静默不打扰
- 也可在「设置 → 关于 → 检查更新」中手动检查，失败时会区分网络错误、暂无发布版本、接口限流等原因
- 更新流程：下载名称含 `macOS` 的 zip 资产 → ditto 解压 → 校验包内版本与代码签名 → 备份旧版本后原位替换并自动重新打开；替换失败自动回滚原版本

### 常见问题（FAQ）

**Q1：首次打开提示「无法验证开发者」或「Apple 无法检查其是否包含恶意软件」，怎么办？**
安装包为开发者签名、未经 Apple 公证，属正常提示。按住 Control 点击（或右键）应用 → 选择「打开」→ 弹窗中再次点击「打开」；若仍被阻止，前往 **系统设置 → 隐私与安全性** 点击「仍要打开」；或用终端执行 `xattr -dr com.apple.quarantine /Applications/计算器.app` 后再启动。

**Q2：为什么仓库里没有源代码？**
本仓库仅提供说明文档与官方安装包，不提供源码。

**Q3：应用需要联网吗？**
只有「汇率换算」获取实时汇率与「检查更新」访问 GitHub 时会联网；换算失败时使用本地缓存汇率，拒绝网络权限不影响计算与绘图功能。

**Q4：支持哪些系统？**
macOS 15.7 或更高版本，Apple Silicon（arm64）Mac。

**Q5：圆盘不见了 / 窗口被收起了，怎么找回？**
点击「收起」、按 ⌘W 或 ↓ 后，窗口会缩为屏幕左下角的小角。把鼠标移到**屏幕最左下角**停留片刻露出小角，点击即可展开。若开启了「隐藏 Dock 图标」，左下角小角是唯一入口。

**Q6：2.0 与 1.0 有什么区别？**
2.0 在 1.0 的 11 项功能之上新增「番茄钟」，圆盘为 12 项；两个版本的安装包都可在 Releases 中下载。

**Q7：怎么在一张图里画多条曲线？**
在绘图 → 二维图像的「数据」页点击「**增加图线**」；图线超过一条后会出现图线管理栏，可切换、重命名、改色、显隐、勾选拟合或删除。表格数据也可用「一次导入为多条图线（整表）」一次性生成多条图线。

**Q8：绘图数据能导出成什么格式？**
二维可导出 PNG 与 CSV（多图线时分列并附逐线拟合结果），极坐标可导出 PNG，三维可导出 PNG 与 OBJ 模型文件。

**Q9：数据点画错了怎么办？**
可在数据点列表中直接修改 x / y（三维另有 z）与误差；暂时不想参与绘图与拟合的点可用眼睛按钮「排除」（数据仍保留、可恢复）；也可以删除单点或清空全部。

**Q10：绘图的历史记录在哪？**
导出后自动记录在「工具」页的「绘图历史」中，点击「重新生成」可恢复该次的数据与设置。

**Q11：怎么切换成英文界面？**
「设置 → 语言」选择 English，全界面立即生效，无需重启。

**Q12：怎么更新到新版本？**
应用启动时会自动检查 GitHub Releases，也可在「设置 → 关于 → 检查更新」手动检查；更新过程会自动备份旧版本，替换失败会自动回滚。

**Q13：在哪里看使用说明？**
2.3 起，主计算窗口、番茄钟窗口、图像标定取点窗口的右上角都有 **i** 按钮，打开即为中英双语使用说明面板。

### 支持与反馈

- 问题反馈：请在 [Issues](https://github.com/f8r4ksv7v4-hub/Calculator/issues) 提交
- 如果你喜欢这个应用，可以通过 [爱发电](https://afdian.com/a/xzy_projects) 或 [GitHub Sponsors](https://github.com/sponsors/f8r4ksv7v4-hub) 支持作者 f8r4ksv7v4-hub

### 致谢

感谢每一位下载、使用并反馈问题的用户，你们的建议让这个应用持续变得更好。

### License

MIT

---

<a id="english-documentation"></a>
## English Documentation

<p align="center">
  <a href="#中文文档"><b>中文</b></a> ·
  <a href="#english-documentation"><b>English</b></a>
</p>

Calculator is a desktop calculator app for macOS built with SwiftUI + AppKit. It packs everyday arithmetic, currency exchange, unit conversion, base conversion, experimental-data plotting (2D / polar / 3D) and a Pomodoro timer into a two-level floating UI made of a "wheel + calculator window". Everything is computed locally; the app only goes online for currency rates and update checks.

> This project is originally designed, developed and maintained by **f8r4ksv7v4-hub**. The UI and all features are original implementations. This repository only ships documentation and the official installers — no source code is provided.

- **中文文档**: [中文文档](#中文文档)

### Screenshots

<p align="center">
  <img src="docs/screenshots/01-app-icon.jpg" width="110" alt="App icon">
</p>

<table align="center">
  <tr>
    <td align="center"><img src="docs/screenshots/02-wheel-menu.jpg" width="320" alt="Wheel menu"><br><sub>Wheel menu</sub></td>
    <td align="center"><img src="docs/screenshots/03-scientific-exchange.jpg" width="320" alt="Scientific calculator and currency exchange"><br><sub>Scientific calculator &amp; currency exchange</sub></td>
    <td align="center"><img src="docs/screenshots/04-pomodoro-base.jpg" width="320" alt="Pomodoro timer and base conversion"><br><sub>Pomodoro timer &amp; base conversion</sub></td>
  </tr>
  <tr>
    <td align="center"><img src="docs/screenshots/05-polar-fit.jpg" width="320" alt="Polar plot with data fitting"><br><sub>Polar plot with data fitting</sub></td>
    <td align="center"><img src="docs/screenshots/06-3d-spiral.jpg" width="320" alt="3D space spiral curve"><br><sub>3D space spiral curve</sub></td>
    <td align="center"><img src="docs/screenshots/01-app-icon.jpg" width="320" alt="App icon"><br><sub>App icon</sub></td>
  </tr>
</table>

### Version History

| Version | Wheel items | Key differences |
| --- | --- | --- |
| **2.3** (current development version) | 12 | Adds over 2.0: **multiple lines** in a single plot (per-line data / colour / fit), **CSV export** (columns split per line plus a per-line fit summary), **OBJ export** for 3D, and the **i Information** panel in the top-right corner of every secondary window |
| 2.0 | 12 | Adds the "Pomodoro" mode on top of everything in 1.0: its own window, a remaining-time pill in the bottom-left corner, and end-of-phase alerts |
| 1.0 | 11 | Basic / Scientific / Exchange / Weight / Temperature / Area / Speed / Time / Data / Base / Plot |

> Note: the official installers currently available on the [Releases](https://github.com/f8r4ksv7v4-hub/Calculator/releases) page are **2.0** and **1.0**; the 2.3 installer will follow in a later Release. The in-app "Check for Updates" only downloads zip assets whose name contains `macOS`.

### Features

- **Two-level wheel interaction**: level 1 is a floating wheel (12 modes since 2.0), level 2 is the calculator window; the centre button shrinks the wheel away and hides the window
- **Basic arithmetic**: the four operators, percent, deeply nested parentheses
- **Scientific**: sin / cos / tan, log, ln, √, x², x!, π, e, with degree/radian switching
- **Currency exchange**: live rates with CNY as the base; falls back to a local cache when offline
- **Unit conversion**: weight, temperature, area, speed, time and data storage
- **Base conversion**: binary / octal / decimal / hexadecimal, converted as you type
- **Experimental data plotting**:
  - 2D chart: enter points manually or import a table, draw polylines or smooth curves, fit linear, quadratic, cubic, quartic, quintic, exponential, logarithmic, power-law or sinusoidal models with R² / RMSE; data transforms (ln x, ln y, log10 x, log10 y, 1/x, 1/y, y normalised to 0-1), log axes, range lock, smoothing level, dual cursors, tangents, error bars, peak / valley labels, mean line, area, point labels, custom chart title and axis names/units
  - Polar chart: enter a radius expression in the angle, set the angle range and sample count, with concentric grid, angle lines and angle labels
  - 3D chart: an expression surface z = f(x, y) or 3D data points (surface mesh / 3D line); drag to rotate and scroll to zoom; fitted plane, extrapolation, tangent plane, two-point measurement; x / y / z axis names, point labels, mean plane, error bars, range lock
  - **Multiple lines (2.3)**: add several lines to one chart, each with independent data, colour, visibility and fit settings; the legend and per-line fit results are drawn and exported together
  - Curve digitising (extract data points from an image) and plot history (restore the data and settings and regenerate)
  - Export PNG (exactly what you see), export CSV (data points and fit results), and OBJ for 3D
- **Pomodoro (2.0)**: customisable work / break durations (defaults to 25 / 5 minutes, cycling automatically); independent alert styles for "work ends" and "break ends" (Mute / Vibrate / Ring / Ring + Vibrate, with adjustable intensity) and a breathing glow around the screen edge; when collapsed, the bottom-left corner keeps a remaining-time pill with start / pause
- **Information panel (2.3)**: the **i** button in the top-right corner of each secondary window opens a bilingual usage guide covering the wheel, shortcuts, 2D / polar / 3D plotting, multiple lines, the Pomodoro timer, updates and settings
- **History**: basic and scientific modes keep the last 20 calculations across launches
- **Bilingual UI**: switch between 中文 / English instantly
- **Appearance & trigger**: follow the system light/dark appearance or pin your own; hide the Dock icon and keep only the bottom-left corner trigger
- **Auto update**: checks, downloads and installs new versions in place from GitHub Releases

### Requirements

- macOS 15.7 or later
- Apple Silicon (arm64) Mac

### Download

| Version | Installer | Size | Direct link |
| --- | --- | --- | --- |
| **2.0** (recommended) | `Calculator-2.0-macOS.zip` | ~2.0 MB | [Download](https://github.com/f8r4ksv7v4-hub/Calculator/releases/download/v2.0/Calculator-2.0-macOS.zip) |
| 1.0 | `Calculator-1.0-macOS.zip` | ~1.9 MB | [Download](https://github.com/f8r4ksv7v4-hub/Calculator/releases/download/v1.0/Calculator-1.0-macOS.zip) |

All versions and release notes live on the [Releases](https://github.com/f8r4ksv7v4-hub/Calculator/releases) page.

### Installation & First Launch

1. Open this repository's [Releases](https://github.com/f8r4ksv7v4-hub/Calculator/releases) page and download the installer you need (`Calculator-2.0-macOS.zip` or `Calculator-1.0-macOS.zip`)
2. Double-click to unzip "计算器.app" and drag it into your Applications folder
3. **Gatekeeper will block the first launch**: the installer is developer-signed but not notarised by Apple, so macOS reports "cannot verify the developer" or "Apple cannot check it for malicious software". Let it through using any of these:
   - In Finder, **Control-click (or right-click)** "计算器.app" → choose "Open" → click "Open" again in the dialog
   - If it is still blocked: open **System Settings → Privacy & Security**, click **"Open Anyway"** in the Security section, then launch the app again
   - If neither works, run the following in Terminal and launch again (strips the quarantine flag):
     ```bash
     xattr -dr com.apple.quarantine /Applications/计算器.app
     ```
4. On first run the app asks for network access (for currency rates and update checks). Allowing it is optional — declining does not affect calculations or plotting

### Usage

#### Level 1: the wheel

Launching the app shows the level-1 floating wheel, with the modes arranged clockwise (since 2.0: Basic, Scientific, Exchange, Weight, Temperature, Area, Speed, Time, Data, Base, Plot, Pomodoro).

- Click any mode icon → the wheel shrinks and the matching level-2 window opens
- Click the centre button → the wheel shrinks away and the window is hidden

#### Level 2: the calculator window

- Top-left "Back" → return to the level-1 wheel
- Top-right holds "Collapse" and "Settings"; since 2.3 the **i** Information entry sits next to "Settings"
- Clicking "Collapse" (or pressing ⌘W / ↓) shrinks the window into the bottom-left corner of the screen
- To restore it, move the pointer to the **very bottom-left corner** of the screen and dwell for a moment, then click the corner

#### Plotting

1. Choose "Plot" on the wheel; the window widens automatically
2. Switch between "2D Image / Polar / 3D Image" at the top
3. For 2D and 3D, enter data (manually or by importing a table), set chart style and fit, display elements and labels in the "Data / Chart / Tools" ribbon
4. For polar charts, enter the radius expression and set the angle range and sample count
5. When done, export PNG (plus CSV for 2D, OBJ for 3D); every export is recorded in the plot history and can be restored and regenerated

#### Pomodoro (2.0)

1. Choose "Pomodoro" on the wheel to open its own window
2. Set the work / break durations and alert styles, then press start
3. Clicking "Collapse" hides the window and leaves a **remaining-time pill pinned in the bottom-left corner**: the button on the pill starts / pauses, and clicking the rest of the pill restores the window
4. Clicking "Back to wheel" returns to the level-1 wheel

### Plot UI Reference: Button Positions and Functions

> The following walks through "top mode switch → 2D (Data / Chart / Tools) → Polar → 3D (Data / Chart / Tools) → multiple lines → exports → image digitising" and explains where every button, field and switch lives and what it does (matching the 2.3 UI).

#### Top: plot mode switch

| Position | Control | Function |
| --- | --- | --- |
| First row of the plot panel, left | Three-way segmented control "2D Image / Polar / 3D Image" | Switches the chart type; the ribbon and chart below are replaced accordingly |
| Same row, right | Grey hint text | Shows what the current mode supports: "Fit / extrapolate / measure / tangent / error bars / log / transform" (2D), "Use t (or θ) for the angle; supports sin / cos / exp / sqrt" (polar), "Isometric surface; data points can draw surface or 3D line; export PNG" (3D) |
| Second row | Tabs "Data / Chart / Tools" (2D and 3D) | Ribbon groups; the selected tab is bold in the accent colour with an underline |

#### 2D chart · Data tab

| Position | Control | Function |
| --- | --- | --- |
| Row 1 | "X Axis" + field (placeholder "e.g. time/s") | Sets the X axis name / unit, drawn next to the axis and used in exported PNGs |
| Row 1 | "Y Axis" + field (placeholder "e.g. voltage/V") | Sets the Y axis name / unit |
| Row 2, from the left | `x` field | x value of the point to add |
| Row 2 | `y` field | y value of the point to add |
| Row 2 | `±` field (placeholder "Error (optional)") | y-direction error of that point, used for error bars; leave empty for no error |
| Row 2 | Round **+** button | Adds the x / y / error values to the current line's point list |
| Row 2 | Round trash button | Clears every data point of the current line |
| Row 2 | Round download icon (menu) | Import entry with three items: **Import into Current Line (Table)** (parses `x,y[,err]` into the current line), **Import Whole Table as Multiple Lines** (column 1 is x, every other numeric column becomes a line), **Import Image & Calibrate Points** |
| Row 2, right | Capsule button "**Add Line**" (+) | New in 2.3: adds a line to the current chart, with its own data, colour and fit settings |
| Below the data row (appears only with **2 or more** lines) | "Lines" management bar + line chips | Click a chip to switch the active line; each chip shows colour, name and visibility (with a single line the bar is hidden and the UI matches 2.0) |
| Management bar | "Legend" switch | Shows / hides the chart legend; the legend lists each line's name, colour and fit expression |
| Management bar, "Active" row | "Line name" field | Renames the active line; leave empty to fall back to the automatic "Line N" name |
| "Active" row | "Colour" menu | Changes the active line's colour (lines in one chart are drawn in different colours) |
| "Active" row | "Show" button | Shows / hides the active line only (drawing only, data kept) |
| "Active" row | "Fit" button | When checked, this line's fit is drawn on the chart and listed in the legend |
| "Active" row, far right | Delete button | Deletes the active line (at least one line always remains) |
| Below the management bar | Point list | Edit x / y / error per row; the eye button excludes or restores a point (excluded points are not drawn and are ignored by fitting / statistics / area); the button at the end of the row deletes that point |
| When the list is empty | Hint text | "No data points yet. Enter x, y above and tap + to add" |

#### 2D chart · Chart tab

| Position | Control | Function |
| --- | --- | --- |
| Row 1 | "Chart Title" field (placeholder "Leave empty to hide the title") | Sets the title drawn at the top of the chart; the screen and the exported PNG share the same title and update as you type |
| Row 2 | Line style capsules "Polyline / Smooth" | Chooses how the curve is drawn |
| Row 2 | "Extrapolate" button | Draws the fitted curve beyond the data range as light dashes; when off, only the in-range fit is drawn |
| Row 2 | Fit type menu | Chooses the fit model (linear, quadratic, cubic, quartic, quintic, exponential, logarithmic, power law, sinusoidal, …) |
| Row 3 | "Display Elements" collapse button | Expands / collapses the switch group below |
| Inside the panel | Six eye buttons: "Extrema / Fit Result / Average / Area / Error Bars / Point Labels" | Shows or hides each element; since 2.3 these switches are **per line** (they write back to the active line) |
| When extrema are on and peaks/valleys exist | Extrema button list | One button per peak / valley to show or hide that single extremum |
| Chart-tab tool row | "x axis / y axis" log buttons | Switches each axis between linear and logarithmic (log needs positive values on that axis) |
| Chart-tab tool row | "Smooth" (three levels) | Sets the smoothing strength of smooth curves |
| Chart-tab tool row | "Transform" menu | Applies ln x, ln y, log10 x, log10 y, 1/x, 1/y or y normalised to 0-1 to the data; affects display and fitting only — the raw data is kept and the transform can be undone |
| Below the panel (read-only) | Statistics panel | Shows point count N, Min, Max, Mean and standard deviation σ (population, ÷N) |
| Below the panel (read-only) | Fit summary | Shows the fit expression, R² and RMSE |

#### 2D chart · Tools tab

| Position | Control | Function |
| --- | --- | --- |
| Row 1 | "Measure" button | Turns on cursor measurement: drag cursors A / B on the chart to snap to data points and read their coordinates and Δx / Δy live |
| Row 1 | "Tangent" button | Turns on tangents: click a data point to show the tangent slope at that point; click again to cancel |
| Row 1 | "History" button | Expands the history list; each entry shows its date, point count, line style and fit type, and offers "Regenerate" or delete |
| Measure row (expanded) | "Cursor A" / "Cursor B" fields (`x / x,y / ,y`) + "Set" button + reset-to-snap button | Positions a cursor by coordinate; the reset button returns it to snap mode |
| Tangent row (expanded) | "Tangent x" field + "Add" button + tangent chips | Adds several tangents; the button on a chip removes that tangent; tangents can also be added / removed by clicking data points |
| Row 2 | "Lock Range" button | Expands the axis-range fields; once locked the button reads "Range Locked" |
| Row 2 | "Equal Scale" button | Makes one unit on x and y occupy the same on-screen length (mutually exclusive with range lock) |
| Range-lock row (expanded) | "X Range" / "Y Range" Min & Max fields + "Lock Range" + "Auto" | Type the ranges and lock them, or write the current auto range into the fields in one click; "Auto" clears the lock |

#### Polar chart

| Position | Control | Function |
| --- | --- | --- |
| Top | Expression field (placeholder "e.g. 5*cos(2*t), 1+sin(t)") | The radius expression r = f(θ); the variable is written as t and functions such as sin / cos / exp / sqrt are supported |
| Row 2 | "θ range" Start / to / End | Sets the angle range |
| Row 2 | "Steps" | Sets the sample count, which controls how smooth the curve is |
| Row 3 | "Chart Title" field | Sets the title at the top of the polar chart; leave empty to hide it |
| Bottom of the panel | "Export Polar" button | Saves the current polar curve as a PNG (you choose the location and file name) |

#### 3D chart

The data source is chosen by the capsule group at the top of the panel: **Expression Surface** and **Import Points**.

| Position | Control | Function |
| --- | --- | --- |
| Top | Data-source capsules "Expression Surface / Import Points" | Switches the 3D data source |
| Expression mode | Expression field (placeholder "e.g. sin(sqrt(x^2+y^2)), x*y/4") | The surface expression z = f(x, y) |
| Expression mode | x / y range fields + "Samples" | Sets the variable ranges and the mesh sample count |
| Expression mode | "Chart Title" field | Sets the surface chart title |
| Points mode | Tabs "Data / Chart / Tools" | Same ribbon grouping as 2D |
| Points mode | Interactive 3D preview on the right | Shared by all three tabs: drag to rotate, scroll to zoom; it refreshes with the fit / tangent / measure switches |
| Data ● Row 1 | "X Axis" / "Y Axis" / "Z Axis" fields (placeholders "e.g. time/s", "distance/m", "temp/℃") | Set the names / units of the three axes |
| Data ● Row 2 | `x`, `y`, `z` fields + `±` error field | Coordinates of the 3D point to add and its z-direction error (for error bars) |
| Data ● Row 2 | Round **+** / round trash buttons | Adds a 3D point / clears every point |
| Data ● Row 2 | Round download icon (menu) | "Import Table (CSV/TSV/TXT)" (needs x, y and z headers, case-insensitive) and "Import Image & Calibrate Points" |
| Data ● list | Point list | Edit x / y / z / error per row (a missing z shows as –), exclude or restore, delete a single point; when no point carries a z value the panel shows a hint |
| Chart ● Row 1 | "Chart Title" field | Sets the 3D chart title |
| Chart ● Row 2 | Draw-style capsules "Surface / 3D Line" | Draws the points as a mesh surface or as a 3D polyline |
| Chart ● Row 2 | "Fit Plane" button | Least-squares plane fit z = a + b·x + c·y |
| Chart ● Row 2 | "Extrapolate" button | Extends the fitted plane 25% beyond the data range with a dashed boundary (enable Fit first) |
| Chart ● Row 3 | "Display Elements" collapse button | Expands / collapses the four switches "Fit Plane / Average / Labels / Error Bars" |
| Chart ● Row 4 | "Lock Range" button | Locks the current x / y / z display range; when expanded you can type min / max or use "Auto" to clear it |
| Tools ● Row 1 | "Tangent" button + (x, y) fields | Draws the tangent plane at a given (x, y) — it uses the fit plane when Fit is on, otherwise a local least-squares plane over the nearest points |
| Tools ● Row 1 | "Measure" button + A / B fields | Enter two points (x, y, z) to read the 3D distance between them |
| Tools ● Row 1 | "History" button | Expands the 3D plot history to restore data and settings and regenerate the image |
| Bottom of the panel | "Export Image" button | Exports the 3D chart as PNG |
| Bottom of the panel | "Export OBJ" button | Exports an OBJ mesh, openable in Blender / MeshLab / Origin and similar tools |

#### Multiple lines (new in 2.3)

- **Entry**: the "**Add Line**" capsule button on the right of the Data tab's second row; each click adds a line, which gets its own colour and becomes active
- **Management bar**: once the chart holds **two or more** lines, a "Lines" bar appears on the Data tab (with a single line the UI matches 2.0 exactly)
- **Switching**: click a line chip to activate it; data, colour, transform and fit are kept per line
- **Legend switch**: shows / hides the chart legend, which lists each line's name, colour and fit expression
- **Active-line row**: rename, recolour, show / hide that line only (drawing only, data kept), toggle whether its fit is drawn, or delete the line (at least one always remains)
- **Two table-import modes**:
  1. "Import into Current Line (Table)" — single-line mode: parses `x,y[,err]` into the current line
  2. "Import Whole Table as Multiple Lines" — whole-table mode: column 1 is the shared x and every other numeric column becomes a line, with error columns detected automatically
- **Export coupling**: PNG includes the legend and per-line fits; multi-line CSV splits columns per line (`x1,y1,x2,y2…`, plus `errN` for lines that carry errors) and appends a per-line summary of the fit expression, R² and RMSE

#### Exports

| Position | Button | Output and notes |
| --- | --- | --- |
| Bottom of the 2D panel | "Export Image" | PNG, exactly what you see (legend and per-line fits included); you choose the location and file name |
| Bottom of the 2D panel | "Export CSV" | Data points and fit results as CSV (openable in Excel); with multiple lines the columns are split per line and a per-line fit summary is appended |
| Bottom of the polar panel | "Export Polar" | PNG |
| Bottom of the 3D panel | "Export Image" | PNG |
| Bottom of the 3D panel | "Export OBJ" | OBJ mesh file |

Every export is recorded in "History", where you can restore the full data and settings of that run and regenerate the image.

#### Image digitising

Choosing "Import Image & Calibrate Points" from the import menu opens the calibration window. The hint reads "Pinch to zoom · drag to pan · click to pick", and the four steps are:

1. Step 1: click the image origin (0,0)
2. Step 2: click a tick on the x axis and type its value
3. Step 3: click a tick on the y axis and type its value
4. Step 4: click the data points along the curve one by one (the list on the left lets you delete them)

The window also offers "Recalibrate", "Clear Picks" and "Finish Import" buttons plus a "N points picked" counter, and the **i** Information entry sits in its top-right corner.

### Information Panel (new in 2.3)

Since 2.3 the **round i button next to "Settings" in the top-right corner** of three secondary windows (for the calibration window, in the title row) opens a bilingual "Information" panel that mirrors the real implementation, with 11 sections:

| Entry point | Notes |
| --- | --- |
| Main calculator window, top-right | The **i** button left of "Settings" |
| Pomodoro window, top-right | The **i** button next to "Settings" |
| Image calibration window, right of the title | The **i** button |

Sections: **Wheel & Windows**, **Keyboard Shortcuts**, **Plot · Overview**, **2D Plot · Data tab**, **Multiple Lines (new in 2.3)**, **2D Plot · Chart tab**, **2D Plot · Tools tab**, **Polar Chart**, **3D Chart**, **Pomodoro**, **Updates & Settings**. The panel shows the current version in its header and closes with the "Done" button.

### Keyboard Shortcuts

| Shortcut | Action |
| --- | --- |
| ⌘ , | Open Settings |
| ⌘ W | Collapse the current window into the bottom-left corner |
| ↓ (Down arrow) | Collapse the current window into the bottom-left corner |
| 0–9 / . , · 。 | Digits and decimal point |
| + - * / | Add, subtract, multiply, divide (the keyboard × ÷ keys are also recognised) |
| = or Enter | Evaluate |
| ( ) | Left / right brackets (nesting supported; half- and full-width brackets both work) |
| % | Percent |
| C | Clear the current input |
| Delete / Backspace | Backspace (removes brackets intelligently at the end of a bracket group) |
| 0–9, A–F (Base mode) | Digits valid for the current base |
| 0–9, . (Exchange / unit conversion) | The value to convert |

Notes: in the level-2 window you can type directly with the keyboard; on the level-1 wheel only ⌘W is active. In plot mode keyboard digits and operators never trigger a calculation — each field handles its own input.

### Settings

**How to open** (either way):

- The "Settings" button in the top-right of the level-2 window
- Menu bar "计算器" → "设置…" (⌘,)

**What it contains**:

- Language: 中文 / English, applied across the whole UI immediately without a restart
- General: hide the Dock icon (the app disappears from the Dock and only the bottom-left corner trigger remains)
- Appearance: follow the system or pin light / dark manually
- About: author, version, tip the author, check for updates, send feedback

### Auto Update

- On launch the app checks GitHub Releases once: when a newer version exists it offers "Download Update / Later"; when it is up to date it stays silent
- You can also check manually in "Settings → About → Check for Updates"; failures distinguish network errors, no releases yet and API rate limiting
- Update flow: download the zip asset whose name contains `macOS` → unzip with ditto → verify the bundled version and code signature → back up the old version, replace it in place and relaunch; a failed replacement rolls back to the previous version

### FAQ

**Q1: On first launch macOS says "cannot verify the developer" or "Apple cannot check it for malicious software". What should I do?**
That is expected — the installer is developer-signed but not notarised by Apple. Control-click (or right-click) the app → "Open" → click "Open" again in the dialog. If it is still blocked, go to **System Settings → Privacy & Security** and click "Open Anyway", or run `xattr -dr com.apple.quarantine /Applications/计算器.app` in Terminal and launch again.

**Q2: Why is there no source code in this repository?**
This repository only ships documentation and the official installers — no source code is provided.

**Q3: Does the app need a network connection?**
Only "Currency Exchange" (live rates) and "Check for Updates" (GitHub) go online. When fetching rates fails the app falls back to its local cache, and declining network access does not affect calculations or plotting.

**Q4: Which systems are supported?**
macOS 15.7 or later on Apple Silicon (arm64) Macs.

**Q5: The wheel is gone, or the window was collapsed — how do I get it back?**
After using the collapse button, ⌘W or ↓, the window shrinks into the bottom-left corner of the screen. Move the pointer to the **very bottom-left corner** and dwell for a moment, then click the corner to expand it. If "Hide Dock Icon" is on, that corner is the only entry point.

**Q6: What is the difference between 2.0 and 1.0?**
2.0 adds the "Pomodoro" mode on top of the 11 modes in 1.0, giving a 12-item wheel. Both installers are available on the Releases page.

**Q7: How do I draw several curves in one chart?**
In Plot → 2D Image → "Data", click "**Add Line**". Once there is more than one line a management bar appears where you can switch, rename, recolour, show / hide, toggle the fit or delete lines. Tabular data can also be turned into several lines at once with "Import Whole Table as Multiple Lines".

**Q8: What export formats are available for plots?**
2D exports PNG and CSV (with per-line columns and a per-line fit summary for multiple lines), polar charts export PNG, and 3D charts export PNG and OBJ model files.

**Q9: What if I entered a data point incorrectly?**
Edit x / y (and z for 3D) or the error directly in the point list; a point you do not want in the plot or the fit can be "excluded" with the eye button (the data is kept and can be restored), or you can delete a single point or clear them all.

**Q10: Where are the plot history records?**
Every export is recorded under "History" on the "Tools" tab; click "Regenerate" to restore that run's data and settings.

**Q11: How do I switch the interface to English?**
Settings → Language → English. The whole UI updates immediately without a restart.

**Q12: How do I update to a newer version?**
The app checks GitHub Releases on launch, or you can check manually in "Settings → About → Check for Updates". The updater backs up the old version automatically and rolls back if the replacement fails.

**Q13: Where can I find the usage guide?**
Since 2.3, the main calculator window, the Pomodoro window and the image calibration window all have an **i** button in their top-right corner that opens the bilingual Information panel.

### Support & Feedback

- Feedback: please open an [Issue](https://github.com/f8r4ksv7v4-hub/Calculator/issues)
- If you find the app useful, you can support the author f8r4ksv7v4-hub via [爱发电 (Afdian)](https://afdian.com/a/xzy_projects) or [GitHub Sponsors](https://github.com/sponsors/f8r4ksv7v4-hub)

### Acknowledgements

Thanks to everyone who downloads, uses and reports issues — your suggestions keep making this app better.

### License

MIT

*（内容由AI生成，仅供参考）*

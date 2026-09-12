![Banner](https://raw.githubusercontent.com/ClaralightDesign/.github/main/docs/Cover.png)

# ClaraLight Design

ClaraLight Design 是 AstralSight Studios 维护的设计系统，覆盖 App、Web 与图标资产三条主线。本仓库作为设计系统的总览入口，汇总各子仓库的职责与快速链接。

## 设计哲学
### 引言

Claralight 之名，源于小行星 642 Clara（克拉拉星）。

这颗星体的名字来自拉丁语 clarus，意为「清澈、明亮、明晰」——正是英文 clear 与 clarity 的古老词根。它像一块悬浮在宇宙中的透明方晶，表面覆盖着洁净的冰与硅酸盐，在黑暗中反射出冷冽而通透的光。不喧哗，只是清晰地存在着。

Claralight 的设计哲学便由此而来。我们将界面视为 Clara 星那样的存在——明确、简洁，在需要温度、需要纵深的地方，在方圆之间，寻找结构秩序与柔和体验的平衡点，让光自然流淌，让每一处设计都如星光般，营造出清澈而明亮的局部氛围。 不喧哗，但足够指引方向。

### 核心价值观

#### 1·明晰 Clarity
> 「直接到达，不绕弯路。」

在素朴的基底之上，信息的传递必须更加直接。Claralight 的布局设计以明确符合直觉为目标，让用户与内容之间没有任何视觉中介。

#### 2· 平衡 Balance
> 「方立其骨，圆润其气。」

Claralight 在几何语言上追求一种克制的辩证：适当以圆的柔和消解冰冷，又不时以方的秩序建立信赖。这不是风格选择，而是功能与情绪的平衡策略。

#### 3·氛围 Atmosphere
> 「光不在每一处，但在该在处，它便是一方天地。」

在 Claralight 中，光不是强调符号，而是空间氛围的营造者。我们在需要情绪表达、需要品牌温度、需要打破单调的地方，用光与影共同构建局部的「氛围场」。

## 仓库地图

```
ClaralightDesign
├── App 组件库 ............... ClaralightDesign-Flutter
├── Web 组件库
│   ├── React 平滑胶囊 ...... claralight-design-smooth-capsule
│   └── React 组件集合 ...... claralight-design-react-components
└── Symbol Kit
    ├── 主仓 ................. claralight-design-symbol-kit
    ├── Flutter 适配包 ...... claralight-design_symbol-kit-flutter
    ├── Figma 适配包 ........ claralight-design_symbol-kit-figma
    ├── Vue 适配包 .......... claralight-design_symbol-kit-vue
    ├── Unplugin 适配包 ..... claralight-design_symbol-kit-unplugin
    ├── React 适配包 ........ claralight-design_symbol-kit-react
    └── Figma 插件 .......... claralight_symbol-kit_figma_plugin
```

### 第一部分：App 组件库

#### [ClaralightDesign-Flutter](https://github.com/AstralSightStudios/ClaralightDesign-Flutter)

设计语言 ClaraLight Design 的 Flutter 实现，包含完整组件库与 Gallery 演示工程。

- 技术栈：Flutter / Dart

### 第二部分：Web 组件库

#### [claralight-design-smooth-capsule](https://github.com/AstralSightStudios/claralight-design-smooth-capsule)

React 平滑胶囊遮罩组件，基于 SVG mask 与 CSS `backdrop-filter` 实现玻璃质感胶囊。

#### [claralight-design-react-components](https://github.com/AstralSightStudios/claralight-design-react-components)

ClaraLight Design 的 React 通用组件集合仓库，用于沉淀跨项目复用的 Web 组件。

### 第三部分：Symbol Kit

#### [claralight-design-symbol-kit](https://github.com/AstralSightStudios/claralight-design-symbol-kit)

Symbol Kit 主仓，负责把 Figma 导出的 SVG 源文件与 Design Token JSON 编译为多字重、多样式的 SVG 图标集。

- 已发布 npm 包：
  - `@claralight-design/symbol-kit-core`：Symbol IR、字重定义、SVG 渲染与已编译图标数据
  - `@claralight-design/symbol-kit-compiler`：SVG 解析、语义分类、几何处理与图标生成
  - `@claralight-design/symbol-kit-cli`：可安装的 SVG 与 Design Token 构建命令
- 默认生成样式：`Normal` / `outline` 为必需；`Fill` 与 `Duotone` 可选生成
- 框架子仓库通过 `modules.config.json` 与 `scripts/modules.mjs` 统一管理，并非 Git submodule

#### 框架适配包

| 仓库 | 用途 |
|------|------|
| [claralight-design_symbol-kit-flutter](https://github.com/AstralSightStudios/claralight-design_symbol-kit-flutter) | 读取 `.symbol.json` 预编译产物，使用 Flutter `Path` / `CustomPainter` 绘制图标 |
| [claralight-design_symbol-kit-figma](https://github.com/AstralSightStudios/claralight-design_symbol-kit-figma) | 统一 Figma 插件：构建、命名与设置三合一 |
| [claralight-design_symbol-kit-vue](https://github.com/AstralSightStudios/claralight-design_symbol-kit-vue) | Vue 图标组件适配包 |
| [claralight-design_symbol-kit-unplugin](https://github.com/AstralSightStudios/claralight-design_symbol-kit-unplugin) | 构建工具插件（Unplugin）适配包 |
| [claralight-design_symbol-kit-react](https://github.com/AstralSightStudios/claralight-design_symbol-kit-react) | React 图标组件包，每个图标为独立命名组件 |

#### Figma 插件

| 仓库 | 用途 |
|------|------|
| [claralight_symbol-kit_figma_plugin](https://github.com/AstralSightStudios/claralight_symbol-kit_figma_plugin) | 通过 Figma Variables 识别图标语义，生成 Symbol Kit 可读取的 Build Source SVG |
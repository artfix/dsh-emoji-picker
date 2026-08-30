# dsh-emoji-picker

DeepSeek Harness 插件：在聊天输入栏工具栏（模型选择器这一排）加一个 emoji 快捷按钮。点击 **😊**，从 8 个分类（约 1870 个基础 emoji）中挑选，点选即插入草稿末尾；点击面板外任意区域自动收起。

data 来源：[`@emoji-mart/data`](https://github.com/missive/emoji-mart)（MIT，Unicode 全量），已按官方分类内嵌进插件本体，运行时不依赖任何磁盘文件、也无网络请求。

## 功能

- 输入栏**左端**（附件控件旁）出现 😊 按钮
- 面板为**文字分类标签**切换：表情与人物 / 动物与自然 / 食物与饮品 / 活动与节庆 / 旅行与地点 / 物品 / 符号 / 旗帜
- 点击某分类，下方网格显示该分类全部 emoji；点击插入草稿末尾
- **点击面板外任意区域**自动关闭（也可点 × 或再按按钮）

## 安装

```bash
dsh plugin --profile web add github:Arthu77/dsh-emoji-picker
```

重启 `dsh web` 后生效。若你的 profile 名不是 `web`，把 `--profile web` 换成你的 profile 名。

> ⚠️ 本机（Windows）若遇到 pnpm 安装 git 仓库报 `EPERM`，可手动安装：把仓库 `tar.gz` 解压后，将整个文件夹复制到 `<profile>/node_modules/dsh-emoji-picker`，再在 `<profile>/cordis.patch.yml` 加入 `- insert: { - id: emoji-quick, name: 'dsh-emoji-picker' }`，然后重启。

## 截图

![面板 Demo](ScreenShot.png)

## License

MIT

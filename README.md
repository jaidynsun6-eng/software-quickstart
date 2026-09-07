# AI 做好了，教我自己改。

**AI 作品接手指南 · software-quickstart**

## 先看案例

[直接打开 Photoshop 案例：把「牛来了」改成自己的标题](examples/photoshop-title/index.html)

这是一份已经生成好的 HTML 接手指南，包含真实界面截图、练习 PSD、完成示范、撤销和保存步骤。也可以通过仓库的 [GitHub Pages 入口](https://jaidynsun6-eng.github.io/software-quickstart/)直接阅读。

跟着案例让 AI 做出一张海报、一个房间或一个网页之后，你可能还是不知道怎么自己改标题、挪家具、换图片。

这个 Skill 接在作品生成之后：检查实际工程，让你选择想亲手修改的部分，再用真实界面截图和必要原理，生成一份简短的接手指南。每次学一项，包含结果检查、撤销和保存。

![真实案例：在 Photoshop 中接手修改牛来了海报](examples/photoshop-title/assets/01-open.png)

## 案例

AI 在 Photoshop 中完成了「牛来了」海报。用户选择先学修改标题，随后得到一份针对这张海报的指南：

**找到文字图层 → 双击 T → 替换标题 → 点勾确认 → 撤销 → 保存新 PSD。**

![修改后：好牛啊](examples/photoshop-title/assets/04-commit.png)

案例包含实际界面截图、图中定位标注、练习 PSD、完成示范、错误提示和独立练习。

- [阅读案例说明](examples/photoshop-title/README.md)
- [下载练习 PSD](examples/photoshop-title/practice.psd) · [下载完成示范](examples/photoshop-title/finished.psd)
- [查看 HTML 指南文件](examples/photoshop-title/index.html)：下载仓库后，用浏览器打开这个文件即可阅读；GitHub 文件页显示源码。

本例于 2026-09-07 在 macOS、Photoshop 2024 中文界面中演示。牛与背景是一张 AI 生成的插画，中英文是独立文字图层。案例验证了标题修改流程，不代表已经测试所有软件，也没有测量新手学习效率。

## 安装与开始

这是给 Agent 使用的 Skill，不是 Photoshop 插件，也不包含软件操控工具。

下载 [Skill 安装包](dist/software-quickstart.zip)，解压得到 `software-quickstart` 文件夹。Codex 默认安装位置是 `~/.codex/skills/software-quickstart/`；设置了 `CODEX_HOME` 时使用其 `skills/` 目录。已有同名文件夹时先备份，避免覆盖个人修改。

也可以把本仓库链接交给 Codex，让它使用 skill-installer 安装仓库中的 `software-quickstart` 子目录。安装后在下一轮对话使用；若未识别，可直接要求 Agent 读取安装目录下的 `SKILL.md`。

在已经完成作品的对话中发送：

```text
使用 $software-quickstart，这个作品已经做好了，教我自己修改。
```

目标明确时直接说：

```text
使用 $software-quickstart，教我修改这张海报的标题。
请检查当前 PSD，用副本演示，生成带真实截图的指南。
```

如果换了对话，需要提供工程文件或其位置。仅输入软件名时，Skill 会先给出具体任务路径供选择。

## 它会怎样教

1. **看实际工程。** 确认可编辑源文件、当前软件和目标内容，区分 PSD 与 PNG、源码与浏览器预览。
2. **选一次修改。** 围绕作品提出少量可行选项；你已经说明目标时跳过选择。
3. **演示并截图。** 在副本或可恢复环境中验证，标出对象、模式、入口与操作结果。
4. **给你一份接手指南。** 默认生成可离线阅读的 HTML，带目录、图解、必要原理与排错提示。
5. **让你自己试一次。** 换一个标题或参数，检查结果，练习恢复与保存。后续再补充你想学的修改。

例如，改字时解释文字图层，移动物品时解释选择与方向。概念随着实际问题出现，无需先读完整软件课程。

## 使用条件与边界

- Agent 需要访问相关工程。真实截图与操作验证还需要可用的电脑或浏览器工具、相应授权，以及目标软件。
- Skill 本身不会安装 Photoshop、赋予控制权限，也不依赖某个特定模型名称。
- 没有界面工具时可以生成文档依据的指南，但必须标明未实际验证，不能伪造截图。
- 只有扁平图片时，不会假装存在独立图层；复杂改动可能仍适合交给 Agent。
- 默认保护原工程；教学不包含擅自重组作品或发布线上修改。
- 这是一套可跨软件应用的方法，目前随仓库公开的实操案例是 Photoshop 标题修改。

## 反馈

试用后欢迎提交 Issue：软件与版本、你想改什么、卡在哪一步、实际看到什么。分享截图前移除账号、客户资料等无关信息。具体卡点比“好不好用”更有助于改进教学。

## 文件

```text
software-quickstart/       安装到 Agent 的 Skill
examples/photoshop-title/ 实际案例、截图及练习工程
dist/                     仅包含 Skill 的下载包
```

本仓库为独立项目，与 OpenAI 或 Adobe 无官方隶属关系。软件界面和商标属于相应权利人；案例没有附带软件或字体文件。公开展示不等于已授予所有素材任意再分发权，素材情况见 [来源说明](examples/photoshop-title/README.md#素材与公开范围)。

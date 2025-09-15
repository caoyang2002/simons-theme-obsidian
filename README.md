# 教程

[教程](https://publish.obsidian.md/chinesehelp/01+2021%E6%96%B0%E6%95%99%E7%A8%8B/obsidian%E4%B8%BB%E9%A2%98%E8%AE%BE%E7%BD%AE)

# 调试

win 使用 `Ctrl` +  `Shift` + `I` 进入

mac 使用 `Command` + `Option` + `I` 进入

#

这是一个 Obsidian ([https://obsidian.md](https://obsidian.md/)) 的示例主题。

## 第一次发布主题？

### 快速开始

<img width="244" alt="Pasted image 20220822135601" src="https://user-images.githubusercontent.com/693981/186000386-4f4da987-fcaf-4aa5-aed4-e34b5901255d.png">

首先，选择 **Use this template**（使用此模板）。这将在你的 Github 个人资料下创建此存储库（repo）的副本。然后，你需要将新的存储库 _克隆_ 到你的计算机上。

一旦你在本地计算机上拥有了存储库，有几个占位符字段需要填写。

1. 在 `manifest.json` 文件中，将 "name" 字段更改为你希望主题名称的任何内容。例如：

  ```json
  {
    "name": "Moonstone",
    "version": "0.0.0",
    "minAppVersion": "1.0.0"
  }
  ```

2. 同样在 manifest.json 文件中，你可以在 "author" 字段旁边包含你的姓名。

配置完这些字段后，剩下的就是添加你的样式！你的所有 CSS 都需要放在位于存储库根目录的 `theme.css` 文件中。

## 将你的主题添加到主题画廊

### 添加截图缩略图

在存储库中，包含你主题的截图缩略图。你可以给文件起任何名字，例如 `screenshot.png`。此图片将用于主题列表中的小预览。

你的截图文件应该是 `16:9` 的宽高比。
推荐尺寸为 512x288。

### 提交你的主题进行审查

要将你的主题包含在主题画廊中，你需要向 [`obsidianmd/obsidian-releases`](https://github.com/obsidianmd/obsidian-releases#community-theme) 提交一个 Pull Request。

## 发布版本 _（可选）_

如果你的主题变得越来越复杂，你可能需要开始考虑你的主题如何与 Obsidian 的不同版本保持兼容。在 Obsidian v0.16 中引入，主题支持 [Github Releases](https://docs.github.com/en/repositories/releasing-projects-on-github/managing-releases-in-a-repository)。这意味着你可以指定主题的哪些版本与 Obsidian 的哪些版本兼容。

### 发布主题初始版本 (1.0.0) 的步骤

1. 从你的主题存储库中，点击 "Releases"。

<img width="235" alt="Pasted image 20220822145001" src="https://user-images.githubusercontent.com/693981/186000441-287a1a97-65f6-4b5f-ba66-810ceae91cd3.png">

2. 在 Releases 页面上，应该有一个 **Draft a new Release**（起草新版本）按钮。点击它。

<img width="202" alt="Pasted image 20220822145048" src="https://user-images.githubusercontent.com/693981/186000664-6c63ae14-f685-4d39-bfe6-324f95cd9669.png">

3. 填写发布信息表单。
	- **Choose a Tag**（选择标签）：在这里输入版本号的名称。在下拉菜单底部应该有一个按钮来创建一个包含你最新主题更改的新标签。选择此选项。
		<img width="340" alt="Pasted image 20220822145648" src="https://user-images.githubusercontent.com/693981/186000848-bd1c2619-ea09-4e70-a886-40769cda6921.png">
	- **Release Title**（发布标题）：这可以是版本号。
	- **Description**（描述）_可选_：任何更改的内容
	- **Files**（文件）：此表单最重要的部分是上传文件。你可以通过拖放 `manifest.json` 文件和主题的 `theme.css` 文件到文件上传字段来完成此操作。

<img width="946" alt="Pasted image 20220822145356" src="https://user-images.githubusercontent.com/693981/186000772-e689ecea-c3b7-4e9d-9204-7ad62c0123aa.png">

4. 点击 "Publish Release"（发布版本）。
5. 确保 `versions.json` 设置正确。这个文件是一个映射。
  ```json
  {
    "1.0.0": "0.16.0"
  }
  ```

  这意味着你的主题版本 1.0.0 与 Obsidian 版本 0.16.0 兼容。对于主题的初始发布，你不需要对此文件进行任何更改。

### 发布新版本的步骤

发布主题的新版本与发布初始版本相同。

1. 从你的主题存储库中，点击 "Releases"。
2. 在 Releases 页面上，应该有一个 **Draft a new Release**（起草新版本）按钮。点击它。
3. 填写发布信息表单。
	- **Choose a Tag**（选择标签）：在这里输入版本号的名称。在下拉菜单底部应该有一个按钮来创建一个包含你最新主题更改的新标签。选择此选项。
		<img width="333" alt="Pasted image 20220822145812" src="https://user-images.githubusercontent.com/693981/186000912-f494def9-0f67-4662-92bf-bd278082455f.png">
	- **Release Title**（发布标题）：这可以是版本号。
	- **Description**（描述）_可选_：任何更改的内容
	- **Files**（文件）：此表单最重要的部分是上传文件。你可以通过拖放 `manifest.json` 文件和主题的 `theme.css` 文件到文件上传字段来完成此操作。

4. 点击 "Publish Release"（发布版本）。
5. 更新存储库中的 `versions.json` 文件。对于主题的初始发布，你可能不需要对 `versions.json` 文件进行任何更改。但是，当你发布主题的后续版本时，最佳实践是将新版本作为条目包含在 versions.json 文件中。所以这可能看起来像：
  ```json
  {
		"1.0.0": "0.16.0",
		"1.0.1": "0.16.0"
  }
  ```

  这里需要注意的重要一点是：新版本作为"键"包含，"值"是你的主题兼容的 Obsidian 的最低版本。因此，如果你的主题新版本仅与 Obsidian 的 Insider 版本兼容，重要的是相应地设置此值。这将防止使用较旧版本 Obsidian 的用户更新到你主题的较新版本。

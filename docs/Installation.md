# 安装
###### 在开始使用RavenScript你需要做以下准备:

- Ravenfield
- Ravenfield Tools Pack
- Visual Studio Code

## Ravenfield
从[Steam](https://store.steampowered.com/app/636480/Ravenfield)或[Humble Store](https://www.humblebundle.com/store/ravenfield)购买Ravenfield最新版本。更多细节可以在[Ravenfield网站](http://ravenfieldgame.com/)上找到。

## Ravenfield 工具包
Ravenfield工具包包含了构建和发布mod所需的基本资源和脚本。应按照[ instructions on the Ravenfield website](http://ravenfieldgame.com/modding.html)上的说明去使用。

## Visual Studio Code
Visual Studio Code是一个来自微软的代码编辑器。
推荐使用Visual Studio Code有以下几点原因:
- 支持在Unity内构建使用
- 支持Lua脚本的Debug调试
- 支持带.txt扩展名的Lua脚本的语法高亮。

您可以使用任何代码编辑器. Vim, Sublime Text, Notepad++, 任何你喜欢的都可以，但本文档内使用的编辑器全部是Visual Studio Code.
本文档将Visual Studio Code简写为VSCode.

## Unity ❤ Visual Studio Code
Unity默认的代码编辑器是MonoEdit或Visual Studio（注意是臃肿的VS）。但是我们可以配置Unity来使用VSCode:

1. 在Unity中启用Ravenfield Tools Pack.

2. 打开Unity偏好 (Edit > Preferences)

3. 找到  `External Tools`

4. 从下拉框里找到你喜欢的代码编辑器<img src="http://ravenfieldgame.com/ravenscript/_images/unity-external-tools-vs17.png" />

5. 找到  `%localappdata%/Programs/Microsoft VS Code/`  并选中 `Code.exe`

6. `Visual Studio Code` 会立刻成为被选中成为你的默认代码编辑器.

7. 关闭偏好窗口。

8. 打开一个新的VSCode窗口(不需要创建新项目)

9. 打开 `Ravenfield Tools Pack` 文件夹 (File > Open Folder)<img src="http://ravenfieldgame.com/ravenscript/_images/vscode-open-folder.png" />

10. 完成

## 安装扩展
VSCode可以通过扩展进行高度定制。这里有Lua、c#和用于调试的扩展。

1. 打开VScode
2. 打开扩展栏 (View > Extensions)<img src="http://ravenfieldgame.com/ravenscript/_images/vscode-open-extensions.png" />

3. 在顶上的搜索框里搜索 `VScode-lua`

4. 选第一个扩展

5. 点那个绿色的安装按钮<img src="http://ravenfieldgame.com/ravenscript/_images/vscode-install-lua.png" />

6. 再安装一个  `C#`  的扩展 (除非你已经安装了)

7. 再安装一个  `EditorConfig for VS Code`

8. 完成

## 语法高亮

> Note： 如果您遵循了上面的操作，那么在最新的`Ravenfield Tools Pack`中，语法高亮应该是开箱即用的。

Ravenscript文件使用.txt文件扩展名。它们作为文本资产被捆绑到 `Ravenfield Tools Pack` 中，因此需要文件扩展名。

VSCode应该将 `Ravenfield Tools Pack` 中的所有.txt文件都视为Lua代码。如果您遵循了上述步骤，那么它应该已经按预期工作了。如果没有，请继续阅读

VSCode不直接对.txt文件使用语法高亮。我们必须让VSCode将Lua语法高亮应用到Ravenfield Tools Pack文件夹中的所有.txt文件。

1. 打开`Ravenfield Tools Pack`文件夹
2. 打开.vscode目录(它可能是隐藏的)
3. 打开`settings.json`文件
4. 确认是否有以下代码:
```lua
{
    "files.associations": {
        "*.txt": "lua",
    }
}
```
> By [EldersJavas](https://github.com/EldersJavas/ravenscript_doc_zh_tr/)

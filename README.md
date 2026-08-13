# 中文

一个适用于vscode的CSS样式，该样式能让vscode具有whitesur-gtk风格的标题栏按钮。修改自[FengZhongShaoNian/whitesur-gtk-style-titlebuttons-for-vscode](https://github.com/FengZhongShaoNian/whitesur-gtk-style-titlebuttons-for-vscode),调整了按钮的间距，与 whitesur 主题一致

whitesur-gtk-vscode.css文件需要搭配vscode插件[Custom CSS and JS Loader](https://marketplace.visualstudio.com/items?itemName=be5invis.vscode-custom-css)使用。

效果：

![截图](./pic.png)

## 安装步骤

1. **安装插件**

   在VSCode扩展商店中搜索并安装 `Custom CSS and JS Loader` 插件。

2. **下载CSS文件**

   下载本仓库中的 `whitesur-gtk-vscode.css` 文件，保存到一个固定位置（例如 `~/.config/Code/` 或其他你喜欢的位置）。

3. **重启VSCode**

   安装插件后需要重启VSCode使其生效。

## 配置步骤

1. 打开VSCode设置文件 `settings.json`：
   - Windows/Linux: 按 `Ctrl+Shift+P`，输入 `Open User Settings (JSON)`
   - macOS: 按 `Cmd+Shift+P`，输入 `Open User Settings (JSON)`

2. 添加以下配置项：

   ```json
   {
     "vscode_custom_css.imports": [
       "file:///home/你的用户名/.config/Code/whitesur-gtk-vscode.css"
     ]
   }
   ```

   将路径替换为你实际存放CSS文件的位置。

3. 保存设置文件。

4. 再次打开命令面板（`Ctrl+Shift+P` 或 `Cmd+Shift+P`），执行 `Custom CSS: Enable Custom CSS and JS`。

5. 重启VSCode，使样式生效。

## 卸载方法

1. 打开 `settings.json`，删除 `vscode_custom_css.imports` 中的相关配置项。

2. 删除已下载的 `whitesur-gtk-vscode.css` 文件。

3. 打开命令面板，执行 `Custom CSS: Disable Custom CSS and JS`。

4. 重启VSCode。

## 注意事项

- 启用自定义CSS后，VSCode可能会显示"你的安装已损坏"的警告，这是正常现象，可以忽略。
- VSCode更新后可能需要重新执行 `Enable Custom CSS and JS` 命令。
- 某些系统上可能需要以管理员身份运行VSCode才能加载自定义CSS。
- 在Linux系统下如果遇到权限问题，需要获取VSCode安装目录的所有权，运行以下命令：
  ```bash
  sudo chown -R $(whoami) "$(which code)"
  sudo chown -R $(whoami) /usr/share/code
  ```
- 建议保留原始的 `settings.json` 备份，以便出现问题时恢复。


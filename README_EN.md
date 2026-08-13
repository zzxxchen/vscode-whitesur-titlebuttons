# English

A CSS style for VSCode that gives it whitesur-gtk style title bar buttons. Modified from [FengZhongShaoNian/whitesur-gtk-style-titlebuttons-for-vscode](https://github.com/FengZhongShaoNian/whitesur-gtk-style-titlebuttons-for-vscode), adjusted button spacing to match the whitesur theme.

The `whitesur-gtk-vscode.css` file requires the VSCode extension [Custom CSS and JS Loader](https://marketplace.visualstudio.com/items?itemName=be5invis.vscode-custom-css) to work.

Effect:

![Screenshot](./pic.png)

## Installation

1. **Install the extension**

   Search and install the `Custom CSS and JS Loader` extension in the VSCode extension marketplace.

2. **Download the CSS file**

   Download the `whitesur-gtk-vscode.css` file from this repository and save it to a permanent location (e.g., `~/.config/Code/` or any location you prefer).

3. **Restart VSCode**

   Restart VSCode after installing the extension.

## Configuration

1. Open the VSCode settings file `settings.json`:
   - Windows/Linux: Press `Ctrl+Shift+P` and type `Open User Settings (JSON)`
   - macOS: Press `Cmd+Shift+P` and type `Open User Settings (JSON)`

2. Add the following configuration:

   ```json
   {
     "vscode_custom_css.imports": [
       "file:///home/your_username/.config/Code/whitesur-gtk-vscode.css"
     ]
   }
   ```

   Replace the path with the actual location where you stored the CSS file.

3. Save the settings file.

4. Open the command palette again (`Ctrl+Shift+P` or `Cmd+Shift+P`) and run `Custom CSS: Enable Custom CSS and JS`.

5. Restart VSCode to apply the styles.

## Uninstallation

1. Open `settings.json` and remove the related entry from `vscode_custom_css.imports`.

2. Delete the downloaded `whitesur-gtk-vscode.css` file.

3. Open the command palette and run `Custom CSS: Disable Custom CSS and JS`.

4. Restart VSCode.

## Notes

- After enabling custom CSS, VSCode may display a "your installation is corrupt" warning. This is normal and can be ignored.
- After updating VSCode, you may need to re-run the `Enable Custom CSS and JS` command.
- Some systems may require running VSCode as administrator to load custom CSS.
- On Linux, if you encounter permission issues, you need to claim ownership of the VSCode installation directory by running the following commands:
  ```bash
  sudo chown -R $(whoami) "$(which code)"
  sudo chown -R $(whoami) /usr/share/code
  ```
- It is recommended to keep a backup of your original `settings.json` in case you need to restore it.

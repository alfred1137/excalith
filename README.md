<div align="center">
	<h1 align="center">Excalith Start Page (Customized Fork)</h1>
	<img src=".github/startpage.gif" />

This is a customized fork of the [original Excalith Start Page project](https://github.com/excalith/excalith-start-page) for personal use. For comprehensive documentation, built-in commands, key bindings, and detailed usage instructions, please refer to the [original repository](https://github.com/excalith/excalith-start-page).

### Built-In Commands

- Show usage with `help` command (shows basic usage and your configured search shortcuts)
- Show info with `fetch` command (time, date, system and browser data)
- Update your configuration with `config` command
  - `config help` - Displays config command usage
  - `config import <url>` - Imports a configuration from URL
  - `config theme` - Lists all [available themes](./data/themes/)
  - `config theme <theme-name>` - Switches between themes and sets your local configuration
  - `config edit` - Edit local configuration within editor
  - `config reset` - Reset your configuration to default

### Key Bindings

- Use <kbd>→</kbd> to auto-complete the suggestion
- Search without auto-complete with <kbd>CTRL</kbd> + <kbd>ENTER</kbd>
- Cycle through filtered links using <kbd>TAB</kbd> and <kbd>SHIFT</kbd> + <kbd>TAB</kbd>
- Clear the prompt quickly with <kbd>CTRL</kbd> + <kbd>C</kbd>
- Close windows with <kbd>ESC</kbd>

## Using

This fork is primarily intended for personal customization. For detailed information on how to use the original application, including methods like Docker or the online version, please visit the [original project's Getting Started Wiki Page](https://github.com/excalith/excalith-start-page/wiki/Getting-Started).

To customise the page, modify [settings.json](data\settings.json).

## Upgrading the Fork

To keep the customized fork up-to-date with the latest changes from the original Excalith Start Page project, follow these steps:

1.  **Add the Upstream Remote:**
    Add the original Excalith repository as an upstream remote to my local fork:
    ```bash
    git remote add upstream https://github.com/excalith/excalith-start-page.git
    ```

2.  **Fetch Upstream Changes:**
    Fetch the latest changes from the upstream repository:
    ```bash
    git fetch upstream
    ```

3.  **Merge Changes:**
    To incorporate the upstream changes into my local `main` branch (or my primary branch), use a squash merge to keep my fork's history clean. Replace `vX.Y.Z` with the specific tag or branch you want to merge (e.g., `v3.1.5` as in the example below):
    ```bash
    git merge upstream/vX.Y.Z --squash --allow-unrelated-histories
    ```

    **Handling Merge Conflicts:**
    If there are conflicts (e.g., `CONFLICT (content): Merge conflict in data/settings.json`), I will need to resolve them manually.
    *   Open the conflicted files in my editor (e.g., `data/settings.json`).
    *   Look for conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`).
    *   Edit the file to combine the changes as desired, choosing which parts to keep from my fork and which from the upstream.
    *   After resolving conflicts, stage the changes:
        ```bash
        git add <conflicted-file-path>
        ```
    *   Then, commit the merged changes:
        ```bash
        git commit -m "Merge upstream vX.Y.Z into customized fork"
        ```

## License

The code is available under the [MIT license](LICENSE). Feel free to copy, modify, and distribute the code as you wish, but please keep the original license in the files. Attribution is appreciated and will definitely help improving this project.

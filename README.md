# vscode-personal-theme

1. open file `extensions/theme-defaults/package.json`
    - mac 
      ``` bash
      code "/Applications/Visual Studio Code.app/Contents/Resources/app/extensions/theme-defaults/package.json"
      ```
    - linux 
      ```
      code /usr/share/code/resources/app/extensions/theme-defaults/package.json
      ```
 2. add personal theme property
    ``` diff
    {
    ...
        "contributes": {
            "themes": [
                {
                    "id": "Default High Contrast Light",
                    "label": "%lightHcColorThemeLabel%",
                    "uiTheme": "hc-light",
                    "path": "./themes/hc_light.json"
    -           }
    +           },
    +           {
    +               "id": "Custom",
    +               "label": "Personal Theme",
    +               "uiTheme": "vs-dark",
    +               "path": "./themes/custom.json"
    +           }
            ]
        }
    ...
    }
    ```
3. open vscode command with `ctrl` + `shift` + `p` hotkey in and select `Generate Color Theme From Current Settings`, it will generate theme with json format, then copy paste it to `custom.json` file from step 4
4. create/add [custom.json](custom.json) to 
    - mac : `/Applications/Visual Studio Code.app/Contents/Resources/app/extensions/theme-defaults/themes`
    - linux : `/usr/share/code/resources/app/extensions/theme-defaults/themes`

5. close and reopen vscode
6. open vscode theme settings and find `Personal Theme`

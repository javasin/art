<!-- Plugin description -->
---
#  AEM Repository Tools - ART


ART plugin works with one plugin without installing external tools
and quickly manages JCR content.
This tool is more useful in environments with many developers and many servers.

---
 `Put With..`: Transfers content to multiple selected servers.

 `Put`: Transfers content selected in the Project file tree or Editor to the server.

 `Get`: Retrieves from the server to the location selected in the Project file tree or Editor (overwrite).

 `Diff`: Compares the selected file (single) with the server.
<!-- Plugin description end -->
## Settings


  <kbd>File</kbd> > <kbd>⚙️Settings...</kbd> > <kbd>Tools</kbd> > <kbd>AEM Repository Tools</kbd>

![Use this template][file:setting.png]

> #### You can set the functions (put, get, diff, put with) to not be displayed in the menu for each registered AEM server.


- [x] Separate menus by actions

  If you select this function,
  Menu separation by function will be created and menus by server will be registered under it. (3depth)
  If you do not select it,

- [x] Availability

  Set to hide unused features in the right-click menu.
- [x] Show overwrite Confirm

  Show a warning window when overwritten.
- [x] Console autofocus
      
  When an event occurs after selection, the focus moves to the console.




## Add Server
#### Click `+` or `Add AEM Server..` to register an <kbd> AEM server</kbd> .
![Use this template][file:new_server.png]
>  Check the checkbox in the first column of the registered server list to quickly modify whether to use it.

| Property name        | Required   | Description                                                                                                                                                           |
|----------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `Name`               | `true`     | Displayed server name and Key                                                                                                                                         |
| `Description`        | `false`    | Description                                                                                                                                                           |
| `Adding to actions`  | `false`    | Select the function to be used on the registered server                                                                                                               |
| `Proxy`              | `false`    | Enter if it must go through a proxy server                                                                                                                            |
| `URL`                | `true`     | Enter the AEM server address.<br/>If there are multiple servers with the same login information, you can enter additional information by separating them with spaces. |
| `ID`                 | `true`     | Enter an ID that can access crx/de                                                                                                                                    |
| `PW`                 | `true`     | Enter a password that can access crx/de                                                                                                                               |



## Run


<kbd>right-click</kbd> > <kbd>Select action</kbd>

![Use this template][file:right_click.png]

> Right-click a file or folder in the Editor window or Project window and select a function.

- ### Put With : Select the server you want to send to and send it
  ![Use this template][file:select_server.png]
- ### Put : Send to the selected server.
- ### Get : Get the content of the selected server.
- ### Diff : Compare and send to the server or save to My Project.
  ![Use this template][file:diff_window.png]
  > Diff and put<br>
  > A comparison window is created when diff is completed. <br>
  > Can only be used for a single file.

    - <kbd>Put to Remote : "name"</kbd>`Left`
        1. Puts the left (Remote) source code to the server.
        2. If modified, the button is activated.
        3. The window remains even after transmission.

    - <kbd>Put to Remote : "name"</kbd>`right`
        1. Sends the right (Local) window's source code to the server.
        2. If modified, the button is activated.
        3. The window remains even after transmission.

    - <kbd>Apply to Local</kbd>`right-bootom`
        1. Save the source code in the right window as My Code.
        2. The button becomes active when modified.>
        3. The window closes after saving.

## Console

<kbd>Run ToolWindow</kbd> > <kbd>ART Console</kbd>

![Use this template][file:console.png]
> Show the log file.


[file:setting.png]: ./.github/readme/setting_v2.png
[file:new_server.png]: ./.github/readme/new_server.png
[file:right_click.png]: ./.github/readme/right_click.png
[file:confirm.png]: ./.github/readme/confirm.png
[file:console.png]: ./.github/readme/console.png
[file:select_server.png]: ./.github/readme/select_server.png
[file:diff_window.png]: ./.github/readme/diff_window.png





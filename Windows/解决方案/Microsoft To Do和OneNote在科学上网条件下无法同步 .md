1. 使用 ```win+R``` 命令打开命令运行窗口，输入 ```regedit``` 打开注册表
2. 进入目录 ```计算机\HKEY_CURRENT_USER\Software\Classes\Local Settings\Software\Microsoft\Windows\CurrentVersion\AppContainer\Mappings```
3. 通过 DisplayName 找到To Do，```S-1-15-2-2537...```即为SID

    ![](https://github.com/YonlinZ/notebook/blob/main/%E5%9B%BE%E7%89%87%E5%BA%93/image-20210224152232459.png?raw=true)

4. 以管理员身份运行Windows PowerShell
5. 执行命令：

    ```
    CheckNetIsolation.exe loopbackexempt -a -p=S-1-15-2-2537927067-2140208811-1083047336-3825492100-1188134376-3459723148-3131426163
    ```
    -p=后跟的是To Do的SID
6. 验证是否更改成功

    ```
    CheckNetIsolation.exe LoopbackExempt -s
    ```
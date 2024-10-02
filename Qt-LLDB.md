# Qt6 LLDB 应用

作者： nmpassthf@gmail.com 



- CodeLLDB Pulgin
- `>LLDB: Command Promat` run

```bash
pip install --user pygdbmi
```

- setting.json add

``````json
"lldb.launch.initCommands": ["command script import C:\\ENV\\qt\\Tools\\QtCreator\\share\\qtcreator\\debugger\\lldbbridge.py"],
``````

- xmake.lua append

```lua
-- 执行windeployqt
after_build(function (target)

  os.exec("windeployqt.exe " .. target:targetfile())

end)
```

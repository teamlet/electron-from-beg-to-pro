* 在主线程中无法运行 require 的解决方法：

```
mainWindow = new BrowserWindow({
   webPreferences: {
     nodeIntegration: true, // 增加 nodeIntegration： true
  },
});
```

* 在 render 线程出现的安全提示，解决方法：在主线程中，增加下面一句

```
  process.env['ELECTRON_DISABLE_SECURITY_WARNINGS'] = 'true';
```

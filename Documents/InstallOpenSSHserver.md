# 於 Windows 10 安裝 OpenSSH server

1. 在 [github](https://github.com/PowerShell/Win32-OpenSSH/releases) 下載最新版 OpenSSH（OpenSSH-Win64.zip）

![](https://i.imgur.com/LfR9XSQ.png)

2. 以管理員權限，將 OpenSSH-Win64.zip 解壓縮至 C:\Program Files\OpenSSH-Win64

![](https://i.imgur.com/IdF7I0e.jpg)

3. 以系統管理員身分執行命令提示字元

![](https://i.imgur.com/0hVzRkw.png)

4. 使用命令列切換目前所在目錄至 C:\Program Files\OpenSSH-Win64

```
> cd C:\Program Files\OpenSSH-Win64
```

5. 安裝 sshd 與 ssh-agent 服務

```
> powershell powershell.exe -ExecutionPolicy Bypass -File install-sshd.ps1
```

![](https://i.imgur.com/U5pvs7z.jpg)

6. 完成後會以系統服務的方式執行 sshd。而設定檔 sshd_config 與 host keys 在 sshd 服務第一次啟動時，會安裝至 %ProgramData%\ssh

[回到目錄](https://github.com/Roderick-github/cloud-classroom)

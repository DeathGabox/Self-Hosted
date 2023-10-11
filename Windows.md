>> Bueno, vamos a hacer lo mejor posible para que esto se haga bn en un solo script

>> Se usara todo en el Disco `D:` para que se mantenga la instalacion 
---
> Crear Carpetas
```
mkdir -p "D:/Archivos de programa\Instaladores"
```

Instalar Powershell
> Intentar via Winget o Via [MSI](https://github.com/PowerShell/PowerShell/releases/latest)
```
winget install --id Microsoft.Powershell --source winget
```

---
> Instalar Choco
```
Set-ExecutionPolicy Bypass -Scope Process
```
```
$InstallDir='D:/Archivos de programa/Choco/'
```
```
$env:ChocolateyInstall="$InstallDir"
```
```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```
> Instalar programas con Choco
```
choco install aria2 micro
```


> Instalar Firefox
```
aria2c -s16 -x16 "https://download.mozilla.org/?product=firefox-esr-msi-latest-ssl&os=win64&lang=es-CL" --dir="D:/Archivos de programa\Instaladores" --out=Firefox-esr.msi
```
```
msiexec.exe /i "D:\Archivos de programa\Instaladores\Firefox-esr.msi" RunInstallDirPath=`"D:\Archivos de programa\Mozilla Firefox\`" INSTALL_DIRECTORY_PATH=`"D:\Archivos de programa\Mozilla Firefox\`" TASKBAR_SHORTCUT=false DESKTOP_SHORTCUT=false INSTALL_MAINTENANCE_SERVICE=false /quiet
```

---
> Intalar Windows Terminal
```
choco install microsoft-windows-terminal --pre --params='"/install=D:\Program Files\'"
```

> Activar WSL
```
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```
> Activar el Funcionamiento
```
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```
```
wsl --set-default-version 2
wsl --install
```

> Instalar Docker

> Intalar Fuentes | [Mas Info](https://msfn.org/board/topic/28300-installing-fonts-temporarly/#comment-194037)
```
copy "FontName.ttf" "%WINDIR%\Fonts"
reg add "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Fonts" /v "FontName (TrueType)" /t REG_SZ /d FontName.ttf /f
```

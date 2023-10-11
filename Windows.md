>> Bueno, vamos a hacer lo mejor posible para que esto se haga bn en un solo script

>> Se usara todo en el Disco `D:` para que se mantenga la instalacion 
---
> Crear Carpetas
```
cd D:/
mkdir "Archivos de programa"
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
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
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

Instalar Docker


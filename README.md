# 🟦 powershell

### Install
```bash
# Install scoop
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
Invoke-RestMethod -Uri https://get.scoop.sh | Invoke-Expression

# Update PSReadLine
Install-Module PSReadLine -AllowPrerelease -Force

# Install module `Terminal-Icons`
Install-Module -Name Terminal-Icons -Repository PSGallery

# Install module `Oh My Posh`
scoop install https://github.com/JanDeDobbeleer/oh-my-posh/releases/latest/download/oh-my-posh.json

# Install font using `Oh My Posh`
oh-my-posh font install meslo
```

### Profile
```bash
notepad $PROFILE
```

```plain
oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\zash.omp.json" | Invoke-Expression
Import-Module -Name Terminal-Icons
Set-PSReadLineOption -PredictionViewStyle ListView
```

### Fonts
#### Windows Terminal
```json
 "profiles": 
    {
        "defaults": 
        {
            "font": 
            {
                "face": "MesloLGM Nerd Font"
            }
        }
   }
```

#### VSCode
```json
"terminal.integrated.fontFamily": "MesloLGS NF, Consolas, 'Courier New', monospace"
```

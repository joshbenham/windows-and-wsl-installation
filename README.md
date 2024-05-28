# BIOS

 - Make sure that you have Virtualization enabled
 - Make sure that you have TPM enabled

# Windows applications

 - Firefox
 - Laravel Herd
 - TablePlus
 - VMWare Workstation Player
 - Windows Terminal Preview
 - Steam
 - Ubisoft Connect
 - QBittorrent

# Nerd font

Go to https://github.com/ryanoasis/nerd-fonts/releases and download CascadiaCode.zip 

# winget applications

```bash
winget install BurntSushi.ripgrep.MSVC \
cURL.cURL \
Discord.Discord \
Git.Git \
junegunn.fzf \ 
Microsoft.Powershell \
Microsoft.PowerToys \ 
Microsoft.Skype \ 
Microsoft.VisualStudioCode \
Neovim.Neovim \ 
PeterPawlowski.foobar2000 \
Starship.Starship
Zoom.Zoom
```

# PowerShell customizations

```bash
Install-Module -Name Terminal-Icons -Force
Install-Module -Name z -Force
Install-Module -Name PSReadline -Force
Install-Module -Name PSFzf -Force
```

# Powershell config

Open up $PROFILE and add below

```bash
# Powershell
Invoke-Expression (&starship init powershell)

# Icons
Import-Module -Name Terminal-Icons

# PSReadline
Set-PSReadLineOption -PredictionSource History
Set-PSReadLineOption -PredictionViewStyle ListView

# Fzf
Import-Module PSFzf
Set-PsFzfOption -PSReadlineChordProvider 'Ctrl+f' -PSReadlineChordReverseHistory 'Ctrl+r'

# Alias
Set-Alias vim nvim
Set-Alias ll ls
Set-Alias grep findstr
```

# WSL

Not used anymore. check `WSL.md` on the old setup.

# Windows Terminal
Make sure you are using Powershell 7+
My Powershell theme setup

## Enable Acrylic Tab Row
- Go to Appearance Section and set to on the use acrylic material in the tab row

## Changing Color scheme
## For Catppuccin Theme
- Go to [Catpuccin Windows Terminal](https://github.com/catppuccin/windows-terminal)
- Follow the instructions in their wiki


## For Dracula Theme
- Go to: [Windows Terminal Themes](https://windowsterminalthemes.dev/)
- Choose Dracula
- or go to: [Dracula](https://draculatheme.com/windows-terminal)
- Open **``settings.json``** file
- Add the colorscheme in the schemes list
- You should be able to see the theme in Color schemes list

## Changing Fonts
- Go to: [Nerd Fonts](https://github.com/ryanoasis/nerd-fonts/)
- Go to releases and choose the font you want to download
- In this case I'll choose **FiraCode Nerd Font**
- Extract them all to a folder, select all, right click, and click install
- You have to reopen the terminal to refresh the changes
- Go to Windows Terminal > Settings > Profiles section > Defaults > Appearance
- change the colorscheme and font face

## Install Oh My Posh
- Go to: [Oh My Posh](https://ohmyposh.dev/)
- Make sure you have access to **``winget``** command
- Click Get Started > Installation > Windows
- **``winget install JanDeDobbeleer.OhMyPosh -s winget``** paste this in Windows Terminal
- restart your terminal
- type: **``oh-my-posh``**
- enable the default setup: **``oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\jandedobbeleer.omp.json"``**
- Copy the output and paste it.
- To select themes type: **``Get-PoshThemes``**
- Once you selected a theme remember the name of the theme and follow the instructions at the bottom of your terminal to apply the changes.
- Go to the Prompt section of the website to persist your changes in your prompt
- Then to type: **``oh-my-posh get shell``** to find out what shell you're in
- And then you can type: **``notepad $PROFILE``** to modify your profile
- If you can't open your **``$PROFILE type this one: New-Item -Path $PROFILE -Type File -Force``**
- Then try opening it again
- Type this inside your notepad: **``oh-my-posh init pwsh | Invoke-Expression``** . Save and close it.
- If the changes doesn't persist you need to paste into notepad the command you type after you selected a theme.
- For example:
**``oh-my-posh init pwsh --config 'C:\Users\carlsebolino\AppData\Local\Programs\oh-my-posh\themes\hotstick.minimal.omp.json' | Invoke-Expression``**

## Powershell Modules
- [z](https://www.hanselman.com/blog/spend-less-time-cding-around-directories-with-the-powershell-z-shortcut)
- Install the module with this command: `Install-Module z -AllowClobber`
- [Terminal Icons](https://www.powershellgallery.com/packages/Terminal-Icons/0.11.0)
- [PSReadlineHistory](https://www.powershellgallery.com/packages/PSReadlineHistory/)

- Import your modules: `Import-Module -Name <module_name>`
- [Show history while typing ](https://stackoverflow.com/questions/77015369/how-to-enable-history-picklist-while-typing)
    - `Set-PSReadLineOption -PredictionViewStyle ListView`
    - Add to profile
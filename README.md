<h1>Configurações e Etapas para estilizar PowerShell

<br>

1 - Baixar e instalar extensão PowerShell (Microsoft Store) e Gow 0.8.0 (Comandos) E Fire Code

<br>

2 - Abrir terminal como _admin_

<br>

3 - Ativar scripts de fora do

    Set-ExecutionPolicy -ExecutionPolicy RemoteSigned

<br>

4 - Instalar modulos _Oh My Posh_

    Install-Module oh-my-posh -Scope CurrentUser

<br>

    Install-Module posh-git -Scope CurrentUser

<br>

    Install-Module -Name PowerShellGet -Force

_Reiniciar como admin_

<br>

    Install-Module -Name PSReadline -AllowPrerelease -Scope CurrentUser -Force SkipPublisherCheck

<br>

    New-item -type file -Force $profile

<br>

    notepad $profile

<br>

_Colar_

    # Importações Padrões

    Import-Module oh-my-posh
    Import-Module posh-git
    Set-poshPrompt -Theme atomic

    #Autocomplete e histórico de uso

    Set-PSReadlineKeyHandler -Key Tab -Function MenuComplete
    Set-PSReadLineKeyHandler -Key UpArrow -Function HistorySearchBackward
    Set-PSReadLineKeyHandler -Key DownArrow -Function HistorySearchForward
    Set-PSReadlineOption -HistorySearchCursorMovesToEnd

    # Autosugestões do PsReadline

    Set-PSReadlineOption -ShowToolTips
    Set-PSReadlineOption -PredictionSource History

    clear

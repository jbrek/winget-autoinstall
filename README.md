# winget-autoinstall
#one line install for use in unattend.xml
<FirstLogonCommands>
                <SynchronousCommand wcm:action="add">
                    <CommandLine>cmd /c powershell iex ((New-Object System.Net.WebClient).DownloadString('https://raw.githubusercontent.com/jbrek/winget-autoinstall/main/install-winget.ps1'))</CommandLine>
                    <Order>1</Order>
                    <CommandLine>cmd /c winget install Microsoft.VisualStudioCode --silent --accept-package-agreements  --accept-source-agreements </CommandLine>
                    <Order>2</Order>
                    
                </SynchronousCommand>
            </FirstLogonCommands>

iex ((New-Object System.Net.WebClient).DownloadString('https://raw.githubusercontent.com/jbrek/winget-autoinstall/main/install-winget.ps1'))

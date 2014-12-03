Powershell
==========

#Session
Vanop een ene computer verbinding maken met de andere computer via Powershell

Client-PC ``` Enable-PSSessionConfiguration``` 
Als alles goed is verlopen, kan je dan inloggen via het volgende 
Client-PC  ``` Enter-PSSession <naam server>``` 

#Nieuwe shares aanmaken
```New-SMBShare -Name Naam -Path Lokaalpad```

#Shares
```Get-WmiObject Win32_share```

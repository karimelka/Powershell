##Chapter 1

* Get-NetAdapter
* Get-NetConnectionProfile
* Get-Culture
* Get-UICulture
* Get-Date
* Get-Random

Chapter 2
----------
4 main commando's
- Get-Help
- Get-Command (Finding Commandlets)
- Get-Member
- Show-Command
Hulpcommando's
- Verbose (detailed information about the process)
- Debug
- WarningAction
- WarningVariable
- ErrorAction
- ErrorVariable
- OutVariable
- OutBuffer
- WhatIf
- Confirm

! No error message -ErrorAction SilentlyContinue

Transcript : uitvoer van alles wat je hebt gedaan
Start-Transscript
Stop-Transcript

Get-WinEvent

Execution Policies
- Restricted : Laadt geen scripts (Default)
- AllSigned : Alle scripts moeten zijn van Trusted publisher, ook die van lokaal
- RemoteSigned : Moet gesigneerd zijn voor Trusted publisher van internet
- Unrestricted : Alles mag erdoor maar met waarschuwingen
- Bypass : alles mag erdoor zonder waarschuwingen
- Undefined : Verwijderd de huidige policy

Scopes
- Process : alleen voor huidig powershell process
- CurrentUser : alleen voor gebruiker
- LocalMachine : alle gebruikers van de computer

Set-ExecutionPolicy

Chapter 3
----------
Pipeline : Takes the output from one command and sets it as input to another command

* sort --> through the pipeline

* Get-Service | sort name,status -Descending --> by property
* Get-Service | sort name,status --> by value
* Group-Object : Get-Sort-Group

* Where-Object

Chapter 4
----------
* Format-Table
* Format-List
* Format-Wide -AutoSize -Column (Get-Help ...)
* Out-GridView

Chapter 5
----------
>> : into file
> : redirect and overwrite
Export-CSV
Export-CliXML

Chapter 6
----------
* Get-PSProvider : get all providers
 - Alias
 - Environemnt
 - FileSystem
 - Function
 - Registry
 - Variable

* Create new alias
	Set-Location alias:
	New-Item -Name Processes -Value Get-Process

Chapter 7
----------
* DCOM = Distributed Component Object Model
* RPC : Remote Procedure Call

* Enable-PSRemoting
* Enter-PSSession -computername DC

Chapter 8
----------
* WMI = WIndows Management Instrumentation

* Get-WmiObject : connection into WMI
* Get-WmiObject -list "*bios*"

Chapter 9 
----------
* Get-CimClass : wildcards for the classname parameter to enable you to quickly identify potential WMI classes

Chapter 10
-----------

Chapter 11
-----------
* foreach
foreach($element in $dc){}

* while
While($i -lt 5)
	{}

* DoWhile
Do
{}
While($i lt -5)

* Casting [String]A

* DoUntil
Do
{}
Until(vwd)

* For
for($i=5;*i<=5;$i++)

* If
If(vwd)
Else
EndIf

* Switch
Switch($a)
{
	1{'$a=1'}
	2{'$a=2'}
	3{'$a=3'}
	Default {'tekst'}
}

Chapter 12
----------
* Standaard Functie
Function Verb-Noun
{
	#Code
}

* Variabele
Function Verb-Noun()
{
	#Code
}
* Meederen Variabelen
Function Verb-Noun()
{
	Param([int]$p1,[string]$p2,$p3)	
#Code
}


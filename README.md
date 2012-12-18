poweralto
========

Welcome to the **poweralto** wiki!  **Poweralto** is a PowerShell module that provides tools for discovering, configuring, and troubleshooting **Palo Alto Next-Gen Firewalls** through their XML API.

So far, this module adds 18 new cmdlets as follows:

* **Find-PaAddressObject**: Search Address Objects and Address Groups for a given IP, FQDN, or string.
* **Find-PaUnusedObjects**: Find unused Address Objects and Address Groups.
* **Get-PaConnectionString**: Connects to a Palo Alto firewall and returns an connection string with API key. adds value to global:PaConnectionArray for other functions to access
* **Get-PaNatRule**: Returns NAT Ruleset from Palo Alto firewall.
* **Get-PaObjectUsage**: Returns Security, Nat, Address and Address Group usge of specific search string.
* **Get-PaSecurityRule**: Returns Security Ruleset from Palo Alto firewall.
* **Get-PaSystemInfo**: Returns general information about the desired PA.
* **Invoke-PaCommit**: Commits candidate config to Palo Alto firewall
* **Restart-PaSystem**: Restarts PA and watches initial autocommit job for completion.
* **Restore-PaPreviousVersion**: Reverts to previous configuration version
* **Send-PaApiQuery**: Query Palo Alto for custom data.
* **Set-PaSecurityRule**: Edits settings on a Palo Alto Security Rule
* **Set-PaUpdateSchedule**: Defines schedule for content updates.
* **Test-PaConnection**: 
* **Update-PaContent**: Updates Pa Content files.
* **Update-PaSoftware**: **IN PROGRESS** Updates PanOS software to desired version.
* **Watch-PaJob**: Watch a given Jobs progress.

To install poweralto, download [poweralto.psm1](https://github.com/brianaddicks/poweralto/blob/master/poweralto.psm1) and place it it in a directory named "poweralto" within your PowerShell module path.


Place it inside a it's own directory (named poweralto) inside your Powershell Module path.  You can get your PSModule path from `$env:PSModulePath`. For example:
* Current User scope: `C:\Users\jds\Documents\WindowsPowerShell\Modules\poweralto\poweralto.psm1`
* Local Machine scope: `C:\Windows\system32\WindowsPowerShell\v1.0\Modules\poweralto\poweralto.psm1`

After the file is in place, you can then import it into your PowerShell session:

`Import-Module poweralto`
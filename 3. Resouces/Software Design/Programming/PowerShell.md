# Powershell Notes

[PowerShell Documentation - PowerShell](https://docs.microsoft.com/en-us/powershell/)

## Searching and Replacing 
[Select-Stringl](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/select-string?view=powershell-7.1)

[Use PowerShell to Replace Text in Strings  Scripting Blog](https://devblogs.microsoft.com/scripting/use-powershell-to-replace-text-in-strings/)

The replace and search cmdlets make use of REGEX - standard patterns are listed in  [[Regular Expression Quick Reference]]  

PowerShell allows for replacemnt text to make use of the string being replaced. This is done by defining REGEX groups, these groups can then be referenced in the REGEX

## Creating functions and commands

Powershell uses s standard method for naming cmdlets, typicall a verb-noun combination 
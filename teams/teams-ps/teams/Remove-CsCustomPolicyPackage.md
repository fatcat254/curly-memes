---
external help file: Microsoft.TeamsCmdlets.PowerShell.Custom.dll-Help.xml
Module Name: MicrosoftTeams
title: Remove-CsCustomPolicyPackage
author: sunguchuan
ms.author: gucsun
manager: amitar
online version: https://docs.microsoft.com/powershell/module/teams/remove-CsCustomPolicyPackage
schema: 2.0.0
---

# Remove-CsCustomPolicyPackage

## SYNOPSIS
This cmdlet submits an operation that deletes a custom policy package with the given package name.

## SYNTAX

```
Remove-CsCustomPolicyPackage -Identity <String>
```

## DESCRIPTION

This cmdlet submits an operation that deletes a custom policy package. It allows the admin user to delete a custom package. The available package names can be found by running Get-CsPolicyPackage.

## EXAMPLES

### Example 1
```powershell
PS C:\> Remove-CsCustomPolicyPackage -Identity myCustomPackage
```

Deletes a custom package named "myCustomPackage".

## PARAMETERS

### -Identity

The name of the custom package.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Microsoft Teams
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES
The user is not allowed to delete a default package created by Microsoft.

## RELATED LINKS

[Get-CsPolicyPackage](Get-CsPolicyPackage.md)

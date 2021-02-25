---
external help file: Microsoft.TeamsCmdlets.PowerShell.Custom.dll-Help.xml
Module Name: MicrosoftTeams
title: New-CsCustomPolicyPackage
author: sunguchuan
ms.author: gucsun
manager: amitar
online version: https://docs.microsoft.com/powershell/module/teams/new-CsCustomPolicyPackage
schema: 2.0.0
---

# New-CsCustomPolicyPackage

## SYNOPSIS
This cmdlet submits an operation that creates a custom policy package with custom package name, description and a list of policies.

## SYNTAX

```
New-CsCustomPolicyPackage -Identity <String> -PolicyList <String[]> [-Description <String>] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet submits an operation that creates a custom policy package. It allows the user to create their own policy package. For more information on policy packages and the policy types available, please review https://docs.microsoft.com/MicrosoftTeams/manage-policy-packages.

## EXAMPLES

### Example 1
```powershell
PS C:\> New-CsCustomPolicyPackage -Identity myCustomPackage -PolicyList "TeamsMeetingPolicy, Education_Teacher" , "TeamsMessagingPolicy, Firstline_Manager" -Description "My first custom package"
```

Creates a custom package named "myCustomPackage" with description "My first custom package" and two policies included: TeamsMeeting policy named "Education_Teacher" and TeamsMessaging policy named "Firstline_Manager". 

### Example 2
```powershell
PS C:\> New-CsCustomPolicyPackage -Identity myCustomPackage -PolicyList "TeamsMeetingPolicy, Education_Teacher" , "TeamsMessagingPolicy, Firstline_Manager"
```

Creates a custom package named "myCustomPackage" with two policies included: TeamsMeeting policy named "Education_Teacher" and TeamsMessaging policy named "Firstline_Manager". 

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

### -PolicyList

A list of one or more policies included in the package. For each policy in the list, the form is "\<PolicyType\>, \<PolicyName\>". Delimiters of ' ', '.', ':', '\t' are also acceptable. Supported policy types are listed in this [link](https://docs.microsoft.com/en-us/MicrosoftTeams/manage-policy-packages#supported-policy-types). To get the full list of available policy names, please refer to cmdlets such as [Get-CsTeamsMeetingPolicy](https://github.com/MicrosoftDocs/office-docs-powershell/blob/master/skype/skype-ps/skype/Get-CsTeamsMeetingPolicy.md) and [Get-CsTeamsMessagingPolicy](https://github.com/MicrosoftDocs/office-docs-powershell/blob/master/skype/skype-ps/skype/Get-CsTeamsMessagingPolicy.md)

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Applicable: Microsoft Teams
Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description

The description of the custom package.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Microsoft Teams
Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CsPolicyPackage](Get-CsPolicyPackage.md)

[Get-CsTeamsMeetingPolicy](https://github.com/MicrosoftDocs/office-docs-powershell/blob/master/skype/skype-ps/skype/Get-CsTeamsMeetingPolicy.md)

[Get-CsTeamsMessagingPolicy](https://github.com/MicrosoftDocs/office-docs-powershell/blob/master/skype/skype-ps/skype/Get-CsTeamsMessagingPolicy.md)

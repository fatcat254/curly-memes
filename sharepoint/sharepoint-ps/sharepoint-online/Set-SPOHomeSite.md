---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://docs.microsoft.com/powershell/module/sharepoint-online/set-spohomesite
applicable: SharePoint Online
title: Set-SPOHomeSite
schema: 2.0.0
author:
ms.author:
ms.reviewer:
---

# Set-SPOHomeSite

## SYNOPSIS

Sets a SharePoint Site as a Home Site.

## SYNTAX

```powershell
Set-SPOHomeSite [-HomeSiteUrl] <String> [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to set a SharePoint Site as a Home Site. A home site is a communication site that you create and set as the top landing page for all users in your intranet. For more information, see [Set up a home site for your organization](https://docs.microsoft.com/SharePoint/home-site)

## EXAMPLES

### Example 1

```powershell
Set-SPOHomeSite -HomeSiteUrl "https://contoso.sharepoint.com/sites/homesite"
```

This example set the site collection at *<https://contoso.sharepoint.com/sites/homesite>* as SharePoint Online Home Site.

## PARAMETERS

### -HomeSiteUrl

The Url of the site collection to be the home site.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

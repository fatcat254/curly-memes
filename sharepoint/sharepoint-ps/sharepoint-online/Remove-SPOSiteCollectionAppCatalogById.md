---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://docs.microsoft.com/powershell/module/sharepoint-online/remove-spositecollectionappcatalogbyid
applicable: SharePoint Online
title: Remove-SPOSiteCollectionAppCatalogById
schema: 2.0.0
author:
ms.author:
ms.reviewer:
---

# Remove-SPOSiteCollectionAppCatalogById

## SYNOPSIS

Removes the site collection app catalog by the id of the site collection.

## SYNTAX

```powershell
Remove-SPOSiteCollectionAppCatalogById -SiteId <guid> [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to remove the site collection app catalog by the id of the site collection.

## EXAMPLES

### Example 1

```powershell
Remove-SPOSiteCollectionAppCatalogById -SiteId bdbd7458-8199-4e99-87ca-15fe9dc17a86
```

This example removes the site collection app catalog from the site with the id 'bdbd7458-8199-4e99-87ca-15fe9dc17a86'.

## PARAMETERS

### -SiteId

Guid of the site collection.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:
Applicable: SharePoint Online
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/p/?LinkID=113216).

## NOTES

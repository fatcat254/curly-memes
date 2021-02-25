---
external help file:
online version: https://docs.microsoft.com/powershell/module/sharepoint-pnp/get-pnpsiteclassification
applicable: SharePoint Online
schema: 2.0.0
title: Get-PnPSiteClassification
---

# Get-PnPSiteClassification

## SYNOPSIS
Returns the defined Site Classifications for the tenant. Requires a connection to the Microsoft Graph.

## EXAMPLES

### ------------------EXAMPLE 1------------------
```powershell
Connect-PnPOnline -Scopes "Directory.ReadWrite.All"
Get-PnPSiteClassification
```

Returns the currently set site classifications for the tenant.

## RELATED LINKS

[SharePoint Developer Patterns and Practices](https://aka.ms/sppnp)
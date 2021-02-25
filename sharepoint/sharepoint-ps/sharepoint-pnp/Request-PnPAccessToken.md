---
external help file:
online version: https://docs.microsoft.com/powershell/module/sharepoint-pnp/request-pnpaccesstoken
applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019, SharePoint Online
schema: 2.0.0
title: Request-PnPAccessToken
---

# Request-PnPAccessToken

## SYNOPSIS
Requests an OAuth Access token

## SYNTAX 

```powershell
Request-PnPAccessToken [-ClientId <String>]
                       [-Resource <String>]
                       [-Scopes <String>]
                       [-Decoded [<SwitchParameter>]]
                       [-SetAsCurrent [<SwitchParameter>]]
                       [-Credentials <PSCredential>]
                       [-TenantUrl <String>]
```

## DESCRIPTION
Returns an access token using the password grant, using the PnP O365 Management Shell client id by default and the AllSites.FullControl scope by default.

## EXAMPLES

### ------------------EXAMPLE 1------------------
```powershell
Request-PnPAccessToken
```

Returns the access token using the default client id and scope

### ------------------EXAMPLE 2------------------
```powershell
Request-PnPAccessToken -ClientId 26e29fec-aa10-4f99-8381-d96cddc650c2
```

Returns the access token using the specified client id and the default scope of AllSites.FullControl

### ------------------EXAMPLE 3------------------
```powershell
Request-PnPAccessToken -ClientId 26e29fec-aa10-4f99-8381-d96cddc650c2 -Scopes Group.ReadWrite.All
```

Returns the access token using the specified client id and the specified scope

### ------------------EXAMPLE 4------------------
```powershell
Request-PnPAccessToken -ClientId 26e29fec-aa10-4f99-8381-d96cddc650c2 -Scopes Group.ReadWrite.All, AllSites.FullControl
```

Returns the access token using the specified client id and the specified scopes

### ------------------EXAMPLE 5------------------
```powershell
$token = Request-PnPAccessToken -ClientId 26e29fec-aa10-4f99-8381-d96cddc650c2 -Resource https://contoso.sharepoint.com -Credentials (Get-Credential) -TenantUrl https://contoso.sharepoint.com
    Connect-PnPOnline -AccessToken $token
```

Returns the access token using the specified client id and the specified scopes while using the credentials and tenanturl specified to authentication against Azure AD

## PARAMETERS

### -ClientId
The Azure Application Client Id to use to retrieve the token. Defaults to the PnP Office 365 Management Shell

Only applicable to: SharePoint Online

```yaml
Type: String
Parameter Sets: (All)

Required: False
Position: Named
Accept pipeline input: False
```

### -Credentials
Optional credentials to use when retrieving the access token. If not present you need to connect first with Connect-PnPOnline.

Only applicable to: SharePoint Online

```yaml
Type: PSCredential
Parameter Sets: (All)

Required: False
Position: Named
Accept pipeline input: False
```

### -Decoded
Returns the token in a decoded / human readible manner

Only applicable to: SharePoint Online

```yaml
Type: SwitchParameter
Parameter Sets: (All)

Required: False
Position: Named
Accept pipeline input: False
```

### -Resource
The scopes to retrieve the token for. Defaults to AllSites.FullControl

Only applicable to: SharePoint Online

```yaml
Type: String
Parameter Sets: (All)

Required: False
Position: Named
Accept pipeline input: False
```

### -Scopes
The scopes to retrieve the token for. Defaults to AllSites.FullControl

Only applicable to: SharePoint Online

```yaml
Type: String
Parameter Sets: (All)

Required: False
Position: Named
Accept pipeline input: False
```

### -SetAsCurrent
Set this token as the current token to use when performing Azure AD based authentication requests with PnP PowerShell

Only applicable to: SharePoint Online

```yaml
Type: SwitchParameter
Parameter Sets: (All)

Required: False
Position: Named
Accept pipeline input: False
```

### -TenantUrl
Optional tenant URL to use when retrieving the access token. The Url should be in the shape of https://yourtenant.sharepoint.com. See examples for more info.

Only applicable to: SharePoint Online

```yaml
Type: String
Parameter Sets: (All)

Required: False
Position: Named
Accept pipeline input: False
```

## RELATED LINKS

[SharePoint Developer Patterns and Practices](https://aka.ms/sppnp)
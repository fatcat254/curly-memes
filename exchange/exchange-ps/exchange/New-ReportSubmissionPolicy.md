---
external help file: Microsoft.Exchange.TransportMailflow-Help.xml
online version: https://docs.microsoft.com/powershell/module/exchange/new-reportsubmissionpolicy
applicable: Exchange Online
title: New-ReportSubmissionPolicy
schema: 2.0.0
author: chrisda
ms.author: chrisda
ms.reviewer:
---

# New-ReportSubmissionPolicy

## SYNOPSIS
This cmdlet is available only in the cloud-based service.

Use the New-ReportSubmissionPolicy cmdlet to create the user submission configuration in your cloud-based organization. If you've already done this, the cmdlet returns an error.

> [!NOTE]
> We recommend that you use the Exchange Online PowerShell V2 module to connect to Exchange Online PowerShell. For instructions, see [Use the Exchange Online PowerShell V2 module](https://docs.microsoft.com/powershell/exchange/exchange-online-powershell-v2).

For information about the parameter sets in the Syntax section below, see [Exchange cmdlet syntax](https://docs.microsoft.com/powershell/exchange/exchange-cmdlet-syntax).

## SYNTAX

```
New-ReportSubmissionPolicy
 [-EnableCustomizedMsg <Boolean>]
 [-EnableReportToMicrosoft <Boolean>]
 [-EnableThirdPartyAddress <Boolean>]
 [-PostSubmitMessage <String>]
 [-PostSubmitMessageTitle <String>]
 [-PreSubmitMessage <String>]
 [-PreSubmitMessageTitle <String>]
 [-ReportJunkAddresses <MultiValuedProperty>]
 [-ReportJunkToCustomizedAddress <Boolean>]
 [-ReportNotJunkAddresses <MultiValuedProperty>]
 [-ReportNotJunkToCustomizedAddress <Boolean>]
 [-ReportPhishAddresses <MultiValuedProperty>]
 [-ReportPhishToCustomizedAddress <Boolean>]
 [-ThirdPartyReportAddresses <MultiValuedProperty>]
 [<CommonParameters>]
```

## DESCRIPTION
You need to be assigned permissions before you can run this cmdlet. Although this topic lists all parameters for the cmdlet, you may not have access to some parameters if they're not included in the permissions assigned to you. To find the permissions required to run any cmdlet or parameter in your organization, see [Find the permissions required to run any Exchange cmdlet](https://docs.microsoft.com/powershell/exchange/find-exchange-cmdlet-permissions).

## EXAMPLES

### Example 1
```powershell
{{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -EnableCustomizedMsg
The  parameter enables or disables the customized message that's presented to users in the Report Message add-in. Valid values are:

- $true: The customized message is presented to users in the Report Message add-in. You specify the text in the PreSubmitMessage, PreSubmitMessageTitle, PostSubmitMessage, and PostSubmitMessageTitle parameters.
- $false: A customized message is not presented to users. This is the default value.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableReportToMicrosoft
The  parameter enables or disables sending the reported message to Microsoft. Valid values are:

- $true: Reported messages are sent to Microsoft. This is the default value.
- $false: Reported message are not sent to Microsoft.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableThirdPartyAddress
The EnableThirdPartyAddres parameter enables or disables using third-party reporting tools for user submissions. Valid values are:

- $true: Users use third-party tools to report messages to the recipients specified by the ThirdPartyAddresses.
- $false: Users use the Report Message add-in to report messages. This is the default value.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PostSubmitMessage
The PostSubmitMessage parameter specifies the main text to use in the custom message that's shown to users in the Report Message add-in after they submit the message. You can use the variable %type% as a placeholder for the type of submission (spam, phish, etc.). If the value contains spaces, enclose the value in quotation marks (").

You need to use this parameter with the PostSubmitMessageTitle parameter.

This parameter is meaningful only when the EnableCustomizedMsg parameter value is $true.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PostSubmitMessageTitle
The PostSubmitMessageTitle parameter specifies the title text to use in the custom message that's shown to users in the Report Message add-in after they submit the message. You can use the variable %type% as a placeholder for the type of submission (spam, phish, etc.). If the value contains spaces, enclose the value in quotation marks (").

You need to use this parameter with the PostSubmitMessage parameter.

This parameter is meaningful only when the EnableCustomizedMsg parameter value is $true.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreSubmitMessage
The PreSubmitMessage parameter specifies the main text to use in the custom message that's shown to users in the Report Message add-in before they submit the message. You can use the variable %type% as a placeholder for the type of submission (spam, phish, etc.). If the value contains spaces, enclose the value in quotation marks (").

You need to use this parameter with the PreSubmitMessageTitle parameter.

This parameter is meaningful only when the EnableCustomizedMsg parameter value is $true.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreSubmitMessageTitle
The PreSubmitMessageTitle parameter specifies the title text to use in the custom message that's shown to users in the Report Message add-in before they submit the message. You can use the variable %type% as a placeholder for the type of submission (spam, phish, etc.). If the value contains spaces, enclose the value in quotation marks (").

You need to use this parameter with the PreSubmitMessage parameter.

This parameter is meaningful only when the EnableCustomizedMsg parameter value is $true.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportJunkAddresses
The ReportJunkAddresses parameter specifies the recipients who receive messages that are reported as junk by users. A valid value is an internal email address. You can specify multiple email addresses separated by commas.

```yaml
Type: MultiValuedProperty
Parameter Sets: (All)
Aliases:
Applicable: Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportJunkToCustomizedAddress
The ReportJunkToCustomizedAddress parameter enables or disables sending messages reported as junk to custom recipients. Valid values are:

- $true: Messages reported as junk are sent to the recipients specified by the ReportJunkAddresses parameter.
- $false: Messages reported as junk are not sent to custom recipients. This is the default value.

 Whether or not the messages are also sent to Microsoft is controlled by the EnableReportToMicrosoft parameter (the default value is $true).

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportNotJunkAddresses
The ReportNoJunkAddresses parameter specifies the recipients who receive messages that are reported as no junk by users. A valid value is an internal email address. You can specify multiple email addresses separated by commas.

```yaml
Type: MultiValuedProperty
Parameter Sets: (All)
Aliases:
Applicable: Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportNotJunkToCustomizedAddress
The ReportNotJunkToCustomizedAddress parameter enables or disables sending messages reported as not junk to custom recipients. Valid values are:

- $true: Messages reported as not junk are sent to the recipients specified by the ReportNotJunkAddresses parameter.
- $false: Messages reported as not junk are not sent to custom recipients. This is the default value.

 Whether or not the messages are also sent to Microsoft is controlled by the EnableReportToMicrosoft parameter (the default value is $true).

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportPhishAddresses
The ReportPhishAddresses parameter specifies the recipients who receive messages that are reported as phishing by users. A valid value is an internal email address. You can specify multiple email addresses separated by commas.

```yaml
Type: MultiValuedProperty
Parameter Sets: (All)
Aliases:
Applicable: Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportPhishToCustomizedAddress
The ReportPhishToCustomizedAddress parameter enables or disables sending messages reported as phishing to custom recipients. Valid values are:

- $true: Messages reported as phishing are sent to the recipients specified by the ReportPhishAddresses parameter.
- $false: Messages reported as not junk are not sent to custom recipients. This is the default value.

 Whether or not the messages are also sent to Microsoft is controlled by the EnableReportToMicrosoft parameter (the default value is $true).

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Applicable: Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThirdPartyReportAddresses
The ThirdPartyReportAddresses parameter specifies where to send user-reported messages if you're using third-party tools instead of the Report Message add-in. You can specify multiple email addresses separated by commas.

This parameter is meaningful only when the EnableThirdPartyAddress parameter value is $true.

```yaml
Type: MultiValuedProperty
Parameter Sets: (All)
Aliases:
Applicable: Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

###  

## OUTPUTS

###  

## NOTES

## RELATED LINKS

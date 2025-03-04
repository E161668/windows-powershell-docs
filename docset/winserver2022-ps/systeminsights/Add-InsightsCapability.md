---
ms.mktglfcycl: manage
ms.sitesec: library
ms.author: v-kaunu
Module Name: systeminsights
Download Help Link: http://go.microsoft.com
Locale: en-US
title: Add-InsightsCapability
ms.reviewer:
description: Use this topic to help manage Windows and Windows Server technologies with Windows PowerShell.
external help file:
keywords: powershell, cmdlet
author: Kateyanne
manager: lizapo
ms.date: 06/18/2018
ms.topic: reference
ms.prod: w10
ms.technology: 
ms.assetid: 38DCC777-40BB-4E35-943F-5AC57EEB53A7
schema: 2.0.0
---

# Add-InsightsCapability

## SYNOPSIS
Adds new predictive capabilities to System Insights. 

## SYNTAX

```
Add-InsightsCapability [-Name] <String> [-Library] <String> [[-ComputerName] <String>]
 [-Credential <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Add-InsightsCapability** cmdlet dynamically adds a new capability using the specified capability name and capability library.

>[!IMPORTANT]
>Some information relates to prereleased product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.

## EXAMPLES

### Example 1
```powershell
PS C:\> Add-InsightsCapability -Name "Custom performance analysis" -Library "D:\perfAnalysis.dll"
```

Adds a new capability with name **Custom performance analysis**, which uses "D:\perfAnalysis.dll" as the capability library.

## PARAMETERS

### -ComputerName
Specifies a fully qualified domain name (FQDN). If not specified, uses the local computer.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CN

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
Specifies the credential for accessing the computer specified by the -ComputerName parameter.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Library
Specifies the path to a .NET library (.dll), which contains the predictive model and defines additional capability metadata, such as the capability description, data sources, and default schedule.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of the capability to be added.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.
For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.SystemInsights.Management.PowerShell.Capability

You can use the pipeline operator to pass a capability object to the *Name* parameter.

## OUTPUTS

### None

## RELATED LINKS
[Get-InsightsCapability](get-insightscapability.md)

[Update-InsightsCapability](update-insightscapability.md)

[Remove-InsightsCapability](remove-insightscapability.md)

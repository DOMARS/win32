---
Description: 'This per-machine system policy is used only if logging has not been enabled by the &\#0034;/L&\#0034; command line option or by MsiEnableLog.'
ms.assetid: '1f28cbce-b759-4293-8af2-15f86f23228c'
title: Logging
---

# Logging

This per-machine [system policy](system-policy.md) is used only if logging has not been enabled by the "/L" command line option or by [**MsiEnableLog**](msienablelog.md). If the policy is set in this case, the installer creates a log file in %temp% with the random name: MSI\*.LOG. Specify the logging mode by setting the policy value to a string of characters. Use the same characters to specify logging mode policy as used by the "/L" [command line option](command-line-options.md). Note that you cannot use "+" and "\*" for the policy.

The logging mode can be set using policy, a command line option, or programmatically. For more information about all the methods that are available for setting the logging mode, see [Normal Logging](normal-logging.md) in the [Windows Installer Logging](windows-installer-logging.md) section.

You can prevent confidential information, for example passwords, from being entered into the log file and made visible. For more information, see [Preventing Confidential Information from Being Written into the Log File](preventing-confidential-information-from-being-written-into-the-log-file.md)

## Registry Key

Set the value named Logging under the following registry key.

**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**

## Data Type

**REG\_SZ**

 

 



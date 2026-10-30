Outlook Verdana Font Configuration
Overview

A PowerShell script that configures Microsoft Outlook to use Verdana 10 pt as the default font for:

New email messages
Replies and forwards
Plain-text messages

The script applies the settings directly to the logged-on user's Windows Registry.

Features
Configures Outlook compose, reply and plain-text fonts.
Uses Verdana at 10 pt.
Checks existing registry settings before making changes.
Avoids unnecessary registry modifications.
Closes and restarts Outlook only when settings need updating and Outlook was already running.
Provides success and failure messages.
Requirements
Windows operating system.
Windows PowerShell.
Microsoft Outlook desktop application.
A logged-on Windows user.
Appropriate permissions to modify the logged-on user's registry settings.
Usage
Download Set-OutlookVerdanaFont.ps1 from this repository.
Open PowerShell.
Navigate to the folder containing the script.
Run:
powershell
.\Set-OutlookVerdanaFont.ps1


If script execution is restricted by your organisation's policies, follow your IT administrator's approved execution process.

Registry Location

The script configures the following registry location:

HKEY_USERS\<User SID>\Software\Microsoft\Office\16.0\Common\MailSettings

The following six binary values are configured:

ComposeFontSimple
ComposeFontComplex
ReplyFontSimple
ReplyFontComplex
TextFontSimple
TextFontComplex
Important Notes
Outlook may be forcibly closed if its font settings need changing.
If Outlook was running before the update, the script attempts to restart it.
If the existing settings are already correct, no registry changes are made and Outlook is not restarted.
Test in a controlled environment before deploying across multiple devices.
Disclaimer

Provided as an IT automation example. Always test scripts in a suitable environment before using them in production.

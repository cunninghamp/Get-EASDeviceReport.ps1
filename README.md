# Get-EASDeviceReport.ps1

This PowerShell script produces a simple report of the ActiveSync device associates in an Exchange organization.

## Synopsis

Get-EASDeviceReport.ps1 - Exchange Server ActiveSync device report

## Description 

Produces a report of ActiveSync device associations in the organization.

## Outputs

Results are output to screen, as well as optional log file, HTML report, and HTML email

## Parameters

- -SendEmail, Sends the HTML report via email using the SMTP configuration within the script.
- -Age, specifies the minimum number of days since last sync before including the device in the report. Default is 0 (all devices).

## Examples

> .\Get-EASDeviceReport.ps1

Produces a CSV file containing stats for all ActiveSync devices.

> .\Get-EASDeviceReport.ps1 -SendEmail -MailFrom:exchangeserver@exchangeserverpro.net -MailTo:paul@exchangeserverpro.com -MailServer:smtp.exchangeserverpro.net

Sends an email report with CSV file attached for all ActiveSync devices.

> .\Get-EASDeviceReport.ps1 -Age 30

Limits the report to devices that have not attempted synced in more than 30 days.

## Credits

Written by: Paul Cunningham

Find me on:

- My Blog:	http://paulcunningham.me
- Twitter:	https://twitter.com/paulcunningham
- LinkedIn:	http://au.linkedin.com/in/cunninghamp/
- Github:	https://github.com/cunninghamp

For more Exchange Server tips, tricks and news check out Exchange Server Pro.

- Website:	http://exchangeserverpro.com
- Twitter:	http://twitter.com/exchservpro

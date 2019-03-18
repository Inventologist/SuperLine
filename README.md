# SuperLine - PowerShell module
Full Description for this project at: https://evotec.xyz/hub/scripts/pswritecolor/

# Description:
SuperLine is a wrapper around Write-Host allowing you to create nice looking scripts, with colorized output.

# Quick install

```powershell
Install-Module -Name "SuperLine"
```

# Examples

![Image](https://evotec.xyz/wp-content/uploads/2018/05/img_5af07118e9f87.png)


```powershell
# Example 1
SuperLine "[i] ", "Parameter in configuration of ", "EmailParameters.EmailFrom", " exists." -Color White, White, Green, White -ShowTime
SuperLine "[i] ", "Parameter in configuration of ", "EmailParameters.EmailTo", " exists." -Color White, White, Green, White -ShowTime
```

```powershell
# Example 2
SuperLine "[i] ", "I will send email soon...", "Get ready.." -Color White
SuperLine "[i] ", "Sending email...." -Color White, White -NoNewLine
<#
    Do Something....
#>
if ($true) {
    SuperLine -Text "OK" -Color Green
}
```

```powershell
# Example 3
SuperLine -Text "Red ", "Green ", "Yellow " -Color Red, Green, Yellow
SuperLine -Text "This is text in Green ",
"followed by red ",
"and then we have Magenta... ",
"isn't it fun? ",
"Here goes DarkCyan" -Color Green, Red, Magenta, White, DarkCyan
SuperLine -Text "This is text in Green ",
"followed by red ",
"and then we have Magenta... ",
"isn't it fun? ",
"Here goes DarkCyan" -Color Green, Red, Magenta, White, DarkCyan -StartTab 3 -LinesBefore 1 -LinesAfter 1
SuperLine "1. ", "Option 1" -Color Yellow, Green
SuperLine "2. ", "Option 2" -Color Yellow, Green
SuperLine "3. ", "Option 3" -Color Yellow, Green
SuperLine "4. ", "Option 4" -Color Yellow, Green
SuperLine "9. ", "Press 9 to exit" -Color Yellow, Gray -LinesBefore 1
SuperLine -LinesBefore 2 -Text "This little ", "message is ", "written to log ", "file as well." `
        -Color Yellow, White, Green, Red, Red -LogFile "C:\testing.txt" -TimeFormat "yyyy-MM-dd HH:mm:ss"
SuperLine -Text "This can get ", "handy if ", "want to display things, and log actions to file ", "at the same time." `
        -Color Yellow, White, Green, Red, Red -LogFile "C:\testing.txt"
```

```powershell
# Example 4 with backgrund colors and usage of aliases
SuperLine -T "My text", " is ", "all colorful" -C Yellow, Red, Green -B Green, Green, Yellow
SuperLine -T "My text", " is ", "all colorful" -C Yellow, Red, Green -B Red, Green, Green
# Example 5 with aliases
wc -t "my text" -C Red
```

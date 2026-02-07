# Windows 11 Tools, Tips & Tricks

> # Bypassing NRO
> Internet Required Onboarding When Installing  Windows 11<pre>To open CMD:
> Shift + F10
>
> Some laptops / Smaller keyboards:
> Shift + Fn + F10
>
> Once in CMD run the following:
> OOBE\BYPASSNRO
>
> The Device should reboot into a more limited setup mode where a local account can be used - rather than a microsoft account
>
> Some newer builds don't work via the above method, so the below command must be run instead
>
> reg add HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\OOBE /v BypassNRO /t REG_DWORD /d 1 /f
shutdown /r /t 0
> Alternatively, disconnect any internet supply to the machine before booting it up, windows -> SHOULD <- fail the connectivity check and default to offline installer mode
> </pre>

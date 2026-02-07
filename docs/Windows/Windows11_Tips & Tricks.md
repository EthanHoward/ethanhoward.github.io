# Windows 11 Tools, Tips & Tricks
> Tips, Tricks & Tools for Windows. Plus some disambiguations as Microsoft loves ambiguity - seemingly.
## Bypassing NRO / Internet-Required Onboard
Getting past internet required onboarding when installing  Windows 11

To open CMD:
<pre>Shift + F10</pre>

Some laptops / Smaller keyboards:
<pre>Shift + Fn + F10</pre>

Once in CMD run the following:
<pre>OOBE\BYPASSNRO</pre>

The Device should reboot into a more limited setup mode where a local account can be used - rather than a microsoft account

I tested this in February 2026, on a fresh-install ARM Windows 11. If this becomes out of date by a while, it likely means they've changed it again, to make it more painfully obscure and idiotic (Thanks Microsoft!).

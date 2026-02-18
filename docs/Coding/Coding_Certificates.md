---
title: Coding - Certificates (HTTPS)
---

# Certificates

## Install & Trust Certificates
Generally I have noticed Windows really hates trusting certificates (it is strict), so in instances where you're in a dev situe and need to trust a cert with the site's FQDN, it just won't work on windows, obviously you still get HTTPS but the browser will be angry. On the other hand, my mac literally does not care that the url 'howardphotography.uk' and 'lab' are, in-fact, NOT the same thing.

### Windows
1. Open 'certmgr.msc'
2. When in Certificate Manager, go to Trusted Root Certification > Certificates (Click on it)
3. (Toolbar) Action > All Tasks > Import
4. Select your certificate file and follow the wizard

### macOS
1. Open Keychain Access
2. (Toolbar) File > Import Items
3. Select your certificate file
4. Finish the wizard
5. Find your certificate entry in the Keychain Access program
6. Double-Click it and go into the 'Trust' dropdown
7. Change it to 'Always Trust'
8. It should now be trusted 
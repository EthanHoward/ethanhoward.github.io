---
title: Google OSINT
---

<!-- @IGNORE:MORFOLOGIK_RULE_EN_GB@-->
# Google OSINT
> Google's Search Filters & Parameters allows you to very precisely query the countless sources attached to the internet, to search for a specific filename, title or search for something excluding something else.

## Search Filters??
There are a few filters which are very versatile and can be used in unique ways

| Filter | Example Use | Example Use Notes |
|--------|-------------|-------|
<!-- @IGNORE:MORFOLOGIK_RULE_EN_GB@-->
| filetype: | filetype:ts | Gets all .ts files, generally useless by itself but works nicely paired with site: |
<!-- @IGNORE:MORFOLOGIK_RULE_EN_GB@-->
| site: | site:raw.githubusercontent.com | Limits results to those from the url 'raw.githubusercontent.com' |
<!-- @IGNORE:MORFOLOGIK_RULE_EN_GB@-->
| -site: | -site:google.com | Excludes, in this case, google.com from results (doesn't matter anyway as we are requiring the above URL) |
<!-- @IGNORE:MORFOLOGIK_RULE_EN_GB@-->
| intitle: | intitle:index.ts | requires 'index.ts' be found in the &lt;title&gt; of the result pages | 
<!-- @IGNORE:MORFOLOGIK_RULE_EN_GB@-->
| allintitle: | -- | Requires multiple terms be in the title, not particularly useful when searching for files. |
<!-- @IGNORE:MORFOLOGIK_RULE_EN_GB@-->
| inurl: | inurl:master | Limits results to only URLs with 'master' in them, here effectively limiting which branch it is likely to find the file from. |
<!-- @IGNORE:MORFOLOGIK_RULE_EN_GB@-->
| allinurl: | -- | Same as allintitle but for URLs instead |
<!-- @IGNORE:MORFOLOGIK_RULE_EN_GB@  @IGNORE:ARROWS@ @IGNORE:EN_UNPAIRED_QUOTES@ -->
| intext: | intext:"=>" | requires a JS arrow function to be in the page content (text) |
stated) |
<!-- @IGNORE:MORFOLOGIK_RULE_EN_GB@ @IGNORE:GITHUB@-->
| related: | related:github.com | Shows stuff related to github.com |
<!-- @IGNORE:MORFOLOGIK_RULE_EN_GB@-->
| allintext: | allintext: esp32 i2c register | Requires ALL terms in page text / body |
<!-- @IGNORE:MORFOLOGIK_RULE_EN_GB@-->
| before: | before:2020-01-01 | Before date |
<!-- @IGNORE:MORFOLOGIK_RULE_EN_GB@-->
| after: | after:2020-01-01 | After date |
<!-- @IGNORE:MORFOLOGIK_RULE_EN_GB@-->
| * | "best * for photography" | Wildcard operator, placeholder essentially will find any phrase like the provided with anything in the middle |
<!-- @IGNORE:MORFOLOGIK_RULE_EN_GB@ @IGNORE:COMMA_PARENTHESIS_WHITESPACE@ -->
| " " | "liTeRal" | requires "liTeRal" be found exactly as-is in the content, case-sensitive |
<!-- @IGNORE:MORFOLOGIK_RULE_EN_GB@ @IGNORE:COMMA_PARENTHESIS_WHITESPACE@ -->
| - | -.d | requires '.d' is NOT in the content, essentially avoiding all .d.ts (if combined w/ all ex cases) |
<!-- @IGNORE:MORFOLOGIK_RULE_EN_GB@-->
| OR | &lt;case&gt; OR &lt;case&gt; | Logical OR of the two cases, AND is implicitly assumed (always AND unless OR is  
<!-- @IGNORE:MORFOLOGIK_RULE_EN_GB@ @IGNORE:DOUBLE_PUNCTUATION@ -->
| .. | £300..£600 | Number range, applicable to money and also NOT to money, example does show money |


Here's an example of a bigger query you might run
<pre>site:raw.githubusercontent.com filetype:ts "index" inurl:master -.d intext:"=>"</pre>

Honestly, these are frighteningly good, I've found my own pages which I presumed would be a needle in a haystack, not 'hidden' but essentially mainly unremarkable therefore harder to find. Fill one of your usernames into the example and see what comes up...


<pre>inurl:myusername32 OR intitle:myusername32</pre>

Now the above is quite literal as it will find the exact string, alternatively if your name always includes some count of components, you can comma separate them instead

<pre>inurl:my,username,32 OR intitle:my,username,32</pre>

Now these are somewhat a pain because if your username is genuinely just your name and some number, and your name isn't particularly uncommon, you'd be scrolling a while, but you would likely pop up, even to narrow it down you could do:

<pre>inurl:my,username,32 OR intitle:my,username,32 site:instagram.com</pre>

That narrows the search to only instagram.com, drastically reducing results, saving time sifting through the results.

Now obviously this is one of the most basic forms of OSINT you could employ, but it is still OSINT.
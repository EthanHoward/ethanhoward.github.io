---
title: Google OSINT
---

# Google OSINT
> Google's Search Filters & Parameters allows you to very precisely query the countless sources attached to the internet, to search for a specific filename, title or search for something excluding something else.

## Search Filters??
There's a few filters which are very versatile and can be used in unique ways

| Filter | Example Use | Example Use Notes |
|--------|-------------|-------|
| filetype: | filetype:ts | Gets all .ts files, generally useless by itself but works nicely paired with site: |
| site: | site:raw.githubusercontent.com | Limits results to those from the url 'raw.githubusercontent.com' |
| -site: | -site:google.com | Excludes, in this case, google.com from results (doesn't matter anyways as we are requiring the above URL) |
| intitle: | intitle:index.ts | requires 'index.ts' be found in the &lt;title&gt; of the result pages | 
| allintitle: | -- | Requires multiple terms be in the title, not particularly useful when searching for files. |
| inurl: | inurl:master | Limits results to only URLs with 'master' in them, here effectively limiting which branch it  is likely to find the file from. |
| allinurl: | -- | Same as allintitle but for URLs instead |
| intext: | intext:"=>" | requires a JS arrow function to be in the page content (text) |
stated) |
| related: | related:github.com | Shows stuff related to github.com |
| allintext: | allintext: esp32 i2c register | Requires ALL terms in page text / body |
| before: | before:2020-01-01 | Before date |
| after: | after:2020-01-01 | After date |
| * | "best * for photography" | Wildcard operator, placeholder essentially will find any phrase like the provided with anything in the middle |
| " " | "liTeRal" | requires "liTeRal" be found exactly as-is in the content, case-sensitive |
| -   | -.d | requires '.d' is NOT in the content, essentially avoiding all .d.ts (if combined w/ all ex cases) |
| OR  | &lt;case&gt; OR &lt;case&gt; | Logical OR of the two cases, AND is implicitly assumed (always AND unless OR is  
| .. | £300..£600 | Number range, applicable to money and also NOT to money, example does show money |


Here's an example of a bigger query you might run
<pre>site:raw.githubusercontent.com filetype:ts "index" inurl:master -.d intext:"=>"</pre>

Honestly, these are frighteningly good, I've found my own pages which i presumed would be a needle in a haystack, not 'hidden' but essentially mainly unremarkable therefore harder to find. Fill one of your usernames into the example and see what comes up...


<pre>inurl:myusername32 OR intitle:myusername32</pre>

Now the above is quite literal as it will find the exact string, alternatively if your name always includes some count of components, you can comma seperate them instead

<pre>inurl:my,username,32 OR intitle:my,username,32</pre>

Now these are somewhat a pain because if your username is genuinely just your name and some number, and your name isn't particularly uncommon, you'd be scrolling a while but you would likely pop up, even to narrow it down you could do:

<pre>inurl:my,username,32 OR intitle:my,username,32 site:instagram.com</pre>

That narrows the search to only instagram.com, drastically reducing results, saving time sifting through the reuslts.

Now obviously this is one of the most basic forms of OSINT you could employ, but it is still OSINT.
# Research




## Tooling

[WebArchiving Tools Index](https://docs.archivebox.io/en/latest/Web-Archiving-Community.html)

[Heritrix3](https://github.com/internetarchive/heritrix3)
[Crawling JS](https://github.com/internetarchive/heritrix3/wiki/crawling-JavaScript)
[Archiving Rich Media](https://github.com/internetarchive/heritrix3/wiki/Archiving-Rich-Media-Content)


[Brozzler](https://github.com/internetarchive/brozzler)

[WebRecorder Tools](https://webrecorder.net/tools)


[WebRecorder / Brozzer Speedruns](https://ws-dl.blogspot.com/2022/03/2022-03-02-web-archiving-speedruns.html)



## Wayback Machine


[New Save Page Now](http://blog.archive.org/2019/10/23/the-wayback-machines-save-page-now-is-new-and-improved/)
Uses Brozzler


[Batch archive URLs from google sheets](https://archive.org/services/wayback-gsheets/)


### Official Save Page Now API
[StackExchange Answer](https://webapps.stackexchange.com/questions/151299/does-the-internet-wayback-machine-api-support-adding-a-link-to-scrape/151360#151360)
[Save Page Now 2 Change Log](https://docs.google.com/document/d/19RJsRncGUw2qHqGGg9lqYZYf7KKXMDL1Mro5o1Qw6QI/edit)
[Save Page Now 2 Public API Docs Draft](https://docs.google.com/document/d/1Nsv52MvSjbLb2PCpHlat0gkzw0EvtSgpKHu4mk0MnrA/edit)


[Unofficial Wayback Save API](https://github.com/akamhy/waybackpy)


## Mark Graham
Director of Wayback

[Mark Graham Presentation Video](https://rjionline.org/presentation/mark-graham-lightning-rounds-archiving-news-at-the-internet-archive/)
> [01:25] "There are many of our partners that are using us, specifically, to archive the news. This is one particular crawl that I set up, archiving North Korean news. I am capturing something like forty-some North Korean sources every day."


[IA Reddit AMA](https://reddit.com/r/IAmA/comments/9sgf4z/hey_reddit_we_are_the_folks_behind_the_internet/e8olajx/#c)
> I am especially passionate about this archive of web content from and about North Korea: https://archive-it.org/collections/6777
> 
> - Mark


[Archive-It North Korea Collection](https://archive-it.org/collections/6777/?show=Sites&collectionIds=6777)


## Other IA Wayback Collections
[kcna.kp collections](https://web.archive.org/web/collections/20230000000000*/http://kcna.kp/)
GDELT appears to be prominent

## IA Whole Earth Web Archiving

[WEWA NK Page](https://webservices.archive.org/wewa/kp?q=North+Korea&type=web)
[IA Webservices](https://webservices.archive.org/)



## Archive Team

[ArchiveBot](https://wiki.archiveteam.org/index.php/ArchiveBot)
[North Korea](https://wiki.archiveteam.org/index.php/North_Korea)
[Governments/North Korea](https://wiki.archiveteam.org/index.php/ArchiveBot/Governments/North_Korea)

Could set up Archive Team project following [this guide](https://wiki.archiveteam.org/index.php/Dev).



## DNS Leak

[NK DNS Leak](https://github.com/mandatoryprogrammer/NorthKoreaDNSLeak)



## Behavior

Wayback SPN appears broken for kcna.kp and others.

[Example SPN2 not working](https://web.archive.org/save/http://kcna.kp/kp/article/q/abad1068ad4bd5dbd396e909231d648b.kcmsf)
[Crashes SPN for rodong.rep.kp](https://web.archive.org/save/http://www.rodong.rep.kp/ko/index.php?MTJAMjAyMi0xMS0yMS1OMDA3QDNAMUBAMEA1==#)

The same example website from the link above about SPN2 not working now appears to be displayed on Wayback and is working mostly. [Link](https://web.archive.org/web/20230304105257/http%3A%2F%2Fkcna.kp%2Fkp%2Farticle%2Fq%2Fabad1068ad4bd5dbd396e909231d648b.kcmsf) Perhaps it takes SPN a few days to show up on Wayback.

Some of the images are not being saved properly. Showing 403 access denied for some, but I can access from my browser. One example case of this strange behavior is with [this photo that was captured](https://web.archive.org/web/20230304105523/http://kcna.kp/siteFiles/photo/202302/PIC0072367.jpg), but failed 403 [a few days later here](https://web.archive.org/web/20230308070207/http://kcna.kp/siteFiles/photo/202302/PIC0072367.jpg).

User Agent probably doesn't matter. Most of these sites appear to have extreme rate limiting.



I'm also able to capture well using Webrecorder's [ArchiveWeb Extension](https://archiveweb.page/)

## How to connect and other resources

[Research Projects #467](https://github.com/mikeizbicki/cmc-csci046/issues/467)
[Webscraping README](https://github.com/mikeizbicki/cmc-csci143/blob/fc72ca9849022e7f20bb84a91cdea49d28e8d37c/future/maybe/week_13/README.md)
[War Dialing README](https://github.com/mikeizbicki/cmc-csci143/tree/fc72ca9849022e7f20bb84a91cdea49d28e8d37c/future/maybe/week_15/lab-wardialing)


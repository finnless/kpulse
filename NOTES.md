ArchiveBot job here https://archive.fart.website/archivebot/viewer/job/8veu3

Job ~10GB, 9000+ sites fetched, ~1000 failed

Number of fetches that were articles / pages:
grep -c "kcmsf’: 200" www.kcna.kp-inf-20230310-045852-8veu3-meta.warc
4463

First half of captured in this item
https://archive.fart.website/archivebot/viewer/item/archiveteam_archivebot_go_20230311134402_632a9be8
https://archive.org/details/archiveteam_archivebot_go_20230311134402_632a9be8


Second half and meta captured in this item
https://archive.fart.website/archivebot/viewer/item/archiveteam_archivebot_go_20230312102303_410c5394
https://archive.fart.website/archivebot/viewer/job/8veu3



Now on wayback


Also downloaded sitemap json. Look at that




TODO

Find which ones failed.

Next steps. Other sites?





Getting Better query using CDX server Docs
https://github.com/internetarchive/wayback/tree/master/wayback-cdx-server

In progress query
https://web.archive.org/cdx/search/cdx?url=kcna.kp/&collapse=urlkey&matchType=prefix&filter=urlkey:.*\.kcmsf$&filter=statuscode:200&output=json&limit=10





This cn article show a 2022 archive team capture, but not a 2023 capture. https://web.archive.org/web/20220819053803/http://kcna.kp/cn/article/q/0332729e8bd20a7d201be9a206f8ffaa.kcmsf

Q: Whats going on? Was this attempted in the 2023 crawl?
A: No. Grepping the crawl meta warc has not matches

What originated this one?
Looks like a lot of pages reference it. Natural.



How do I ensure this and others get found?

The various navigation pages at the footer (Latest News, Top News, etc.)
The next button for pagination on each page make a request here which responds with a 302 redirect to another page. You can click the next page button or type page(1) in the js console

POST /en/category/articles.kcmsf HTTP/1.1
Referer: http://kcna.kp/en/category/articles/q/12c03a49f7dbe829bceea8ac77088c21.kcmsf
FORMDATA:
_token: 88ec0310f649d5c0bc64cefaf65b6332d204323e3027345c79d8a2fa051ee993c20857dd9106ddde286ec59fa98d77cc
q: 12c03a49f7dbe829bceea8ac77088c21
page: 2
category: NT62 query:    


The ArchiveBot query could only see the first page of each category listing because the page buttons are js.
https://web.archive.org/web/20230310051534/http://www.kcna.kp/kp/category/articles.kcmsf




For example, the last English page 2858 has no web archive https://web.archive.org/web/*/http://kcna.kp/en/category/articles/q/4e17956c89f07d29cbb00c4e7cf60933d1a9e36b86602cd18ad314960e853289.kcmsf


Furthermore, Wayback has very few captures for article categories http://www.kcna.kp/en/category/articles

The process could be going through each page of every category and running a recursive capture using archive bot.

First get a list of urls mapping to each page.

Question is would that need to be done for each language.

Es
2138
http://kcna.kp/es/category/articles/q/c4e406c92f7900f8ceb9680cf2c5d572d1a9e36b86602cd18ad314960e853289.kcmsf
Patria radiante [Juche102.9.9.]



Es
2135
http://kcna.kp/es/category/articles/q/2a711283f1b8419cb3d603d890532ca5d1a9e36b86602cd18ad314960e853289.kcmsf



JP
2135
歌謡「祖国賛歌」 [チュチェ102.9.27.]
歌謡「わたしの運命を輝かした母なる党」 [チュチェ102.9.26.]
歌謡「かがやく祖国」　 [チュチェ102.9.9.]
http://kcna.kp/jp/category/articles/q/c4e406c92f7900f8ceb9680cf2c5d572d1a9e36b86602cd18ad314960e853289.kcmsf

These pages have identical contents but are different urls???

2135 also??
http://kcna.kp/jp/category/articles/q/2a711283f1b8419cb3d603d890532ca5d1a9e36b86602cd18ad314960e853289.kcmsf

When I open in private browser, the contents remains the same but page number go away
The next button works. It links to javascript:page(0);
For both pages, this redirects to http://kcna.kp/jp/category/articles/q/d96b6d127dc7596b9bc9ed5b11b9e8db675242b6ecaeb0fafef5e0ab1b09cb53.kcmsf
Yet another identical site. This one keeps linking to itself.

Also identical to http://kcna.kp/en/category/articles/q/1ee9bdb7186944f765208f34ecfb5407.kcmsf, which is the first page of latest news.
The previous three must have just been latest news on first page.

Yes, the reason this is happening is because cookies store session id. Pagination is stored in session.

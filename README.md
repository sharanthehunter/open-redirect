# open-redirect

Hey folks, today I came with an open redirect vulnerability bug.

First I started to enumerate all the subdomains using sublist3r tool.Then I sorted out the live subdomains.

I found showroom.ind**mart.com

In other tab I was running web.archive.org to list all URL’s of our target.

https://web.archive.org/cdx/search/cdx?url=*.target.com/*&collapse=urlkey&output=text&fl=original

It was listing n number of urls.I started to search for that particular subdomain(showroom.ind**mart.com)

![image](https://user-images.githubusercontent.com/84071887/204714370-a71b7e43-67ca-4820-9978-18cdec72cbbe.png)

At last I ended with this url :)

https://showroom.ind**mart.com/glpcat/demo.php?url=

It has a url= parameter



I opened my browser and changed the url parameter to my burp collaborator client url


![image](https://user-images.githubusercontent.com/84071887/204714581-91976a09-8ba8-47db-b587-473515bf8bd6.png)

Boom!!!

It was redirecting to my collab url. I got the response in the collab

![image](https://user-images.githubusercontent.com/84071887/204714641-70ce946f-8d90-4f47-a340-ee724aa6f999.png)

Using this I was able to do a open redirect to any website…

![image](https://user-images.githubusercontent.com/84071887/204714686-5cbb3aba-ab26-489d-a485-70ce5735bf66.png)


Report status :Duplicate 🥲

Thanks for reading Hope You guys enjoyed it!

Happy Hacking!

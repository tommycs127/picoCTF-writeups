# GET aHEAD

- Score: 20 points
- Tags: `picoCTF 2021` `Web Exploitation`
- Author: MADSTACKS

## Description

Find the flag being held on this server to get ahead of the competition http://mercury.picoctf.net:28916/

## Hints

- Maybe you have more than 2 choices
- Check out tools like Burpsuite to modify your requests and look at the responses

## Writeups

Browsing [the URL](http://mercury.picoctf.net:28916/) using any mainstream browser will show a webpage with a red background and two buttons. The HTML is not suspicious under inspection. Pressing the buttons will only switch the background colours.

The name of the challenge (Get a**HEAD**) is the biggest hint, as there is an HTTP request method named [HEAD](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/HEAD). Therefore, we can use tools or API platforms, like [Postman](https://www.postman.com/), to send a HEAD request to the URL.

The response header will have a key-value item containing the flag we want.

# BQ Analytics
User tracking and behavioral analytics based on the Device's Fingerprint.

<br />

## Initialization
Just add the script into your HTML or place bq.min.js into you code. No API Key Needed.
```html
<script async src="/path_to_script/bq.min.js"></script>
```
<br />

## bq.getID()
Returns a unique user ID based on the Device's Fingerprint, regardless of the session and cookies.
```js
bq.getID();
// aac9689d41a34e04b6db362d47b0fdbf
```

## bq.isNew()
Returns First or No site visit.
```js
bq.isNew();
/*
(bool) True - First time, False - No
*/
```

## bq.getFirstVisit()
Returns information about the first visit to the site.
```js
bq.getFirstVisit();
/*
JSON {
	referrer: "google.ru",
	time: "2020-12-18T06:29:17.000Z",
	title: "Google Search",
	url: "https://yoursite.com/landing-page-url"
}
*/
```

## bq.getIP()
Returns User's IP.
```js
bq.getIP();
/*
(string) 192.0.0.1
*/
```

## bq.getDevice()
Returns User's Device Information.
```js
bq.getDevice();
/*
JSON {
	"os":{
		"name":"Mac",
		"version":"10.11",
		"platform":""
	},
	"client":{
		"name":"Chrome",
		"type":"browser",
		"version":"87.0"
	},
	"device":{
		"type":"desktop",
		"brand":"Apple",
		"model":"iMac"
	},
	"mobile":false,
	"screen":{
		"h":1440,
		"w":2560
	}
}
*/
```

## bq.getCity()
Returns User's City name based on IP.
```js
bq.getCity();
/*
(string) "Vienna"
*/
```

## bq.getCountry()
Returns User's Country name based on IP.
```js
bq.getCountry();
/*
(string) "Austria"
*/
```

## bq.getUser()
Returns Full User's Information.
```js
bq.getUser();
```

## bq.push(options)
Push events to the analytics report that available on [https://hqmode.com/business-queries] if you set up your account.
```js
bq.push({group:"groupName",event:"eventName"});
```

<br />
<br />
<br />
<br />

## MIT License

Copyright (c) 2020 HQ

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
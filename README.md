# react-files-hax

> The react-files-hax will help you download files more easily.

<!-- [START getstarted] -->
## Getting Started

### Installation

To use react-files-hax in your project, run:

```bash
npm i react-files-hax
# or "yarn add react-files-hax"
```
### Usage 

For images

```js
const download = require('react-files-hax')
//or
import download from 'react-files-hax';

//Binary ajax Blob
var x=new XMLHttpRequest();
x.open("GET", file.url, true);
x.responseType = 'blob';
x.onload=function(e){download(x.response, "fileName.jpeg", "image/jpeg" ); }
x.send();
```

For Plain Text:

```js
const download = require('react-files-hax')
//or
import download from 'react-files-hax';

//text string
download("hello world", "dlText.txt", "text/plain");

//text dataUrl
download("data:text/plain,hello%20world", "dlDataUrlText.txt", "text/plain");

//text blob
download(new Blob(["hello world"]), "dlTextBlob.txt", "text/plain");

//text Uint8 array
var str= "hello world",	arr= new Uint8Array(str.length);
str.split("").forEach(function(a,b){
	arr[b]=a.charCodeAt();
});
   
download( arr, "textUInt8Array.txt", "text/plain" );
```

For HTML:

```js
const download = require('react-files-hax')
//or
import download from 'react-files-hax';

//Html string
download(document.body.outerHTML, "dlHTML.html", "text/html");

//Html blob
download(new Blob(["hello world".bold()]), "dlHtmlBlob.html", "text/html");
```

### The parameters

download(data, strFileName, strMimeType );

### Help us build more libraries

[donate](https://mpago.la/1zCdgRN).
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<title>My test page</title>
	<link href="styles/style.css" rel="stylesheet">
	<link href="https://fonts.googleapis.com/css?family=Open+Sans" rel="stylesheet">
</head>
<body>
<h1>Mozilla is cool</h1>
<img src="images/firefox-logo.png" alt="My test image" height="300px" width="300px">
<p>
At Mozilla,we're a global community of </p>
<ul>
	<li>technologists</li>
	<li>thinkers</li>
	<li>builders</li></ul>

<p>
working tigether to keep the Internet alive and accessible,so people worldwide can be informed contributors and creators of the Web. We believe this act of human collaboration across an open platform is essential to individual growth and our collective future. </p>  <br><br>
<p>Read the <a href="https://www.mozilla.org/en-US/about/manifesto">Mozilla Manifestp</a>to learn even more about the values and principles that guide the pursuit of our mission.</p>
<button>Change user</button>
<script src="scripts/main.js"></script>
</body>
</html>

html{
	font-size: 10px;/*px means "pixels":the base font size is now 10 px high*/
	font-family:"Open Sans", sans-serif;/*this should be the rest of the output you got from Google fonts*/
     }
	h1{
		font-size:60px;
		text-align:center;
	  }	
		
	p,li{
		font-size:16px;
		line-height:2;
		letter-spacing:1px;
	}
	html{background-color:#00539F;}

	body{
		width:600px;
		margin:0 auto;
		background-color:#FF9500;
		padding:0 20px 20px 20px;
		border:5px solid black;
	}
	h1{margin:0;
	   padding:20px 0;
       color:#00539F;
       text-shadow:3px 3px 1px black;
	}
	img{
		display:block;
		margin:0 auto;
	}
 
 
 
 
 const myHeading = document.querySelector('h1');
myHeading.textContent = 'Hello world!';
let myImage = document.querySelector('img');

myImage.onclick = function() {
    let mySrc = myImage.getAttribute('src');
    if(mySrc === 'images/firefox-icon.png') {
      myImage.setAttribute('src','images/firefox2.png');
    } else {
      myImage.setAttribute('src','images/firefox-icon.png');
    }
}
let myButton = document.querySelector('button');
let myHeading = document.querySelector('h1');
unction setUserName() {
  let myName = prompt('Please enter your name.');
  localStorage.setItem('name', myName);
  myHeading.textContent = 'Mozilla is cool, ' + myName;
}
if(!localStorage.getItem('name')) {
  setUserName();
} else {
  let storedName = localStorage.getItem('name');
  myHeading.textContent = 'Mozilla is cool, ' + storedName;
}
myButton.onclick = function() {
  setUserName();
}
function setUserName() {
  let myName = prompt('Please enter your name.');
  if(!myName) {
    setUserName();
  } else {
    localStorage.setItem('name', myName);
    myHeading.textContent = `Mozilla is cool, ${myName}`;
  }
}
  


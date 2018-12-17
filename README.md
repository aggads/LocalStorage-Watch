Local Storage
---

Web Storage or "Dom Storage" is a solution to store data localy in the browser.
The web storage is more powerfull than the cookies because the cookies are limited in size (only a few ko octets and many mo for the web storage) and use a lot of traffic to download the element like :
	- image
	- css file
	- javascript file
	- etc
With the web storage we have 2 methodes.

*The Session storage* and *the Local storage*

The difference is just if you close your browser or tab if the data are still stored or not.
But both is not secure. (Everyone can find easily your data)

How use it ?
---

**setItem(key, value)**
Store a couple of key and value
ex: 
>localStorage.**setItem**("position", "left");

**getItem(key)**
Get the data with the key
ex: 
>var position = localStorage.**getItem**(position);

**removeItem(key)**
Delete the key and the value
ex: 
>localStorage.**removeItem**("position");

**clear()**
Delete all the data
ex: 
>localStorage.**clear()**;

**.lengt**
Get the number of keys stored
ex: 
>localStorage.**length**;

**.key()**
Get a key with specific index
ex: 
>localStorage.**key(0)**;

**Direct access:**

>localStorage.position("left");

>console.log(localStorage.position);

Store object (Json)
--- 

**Store**

>let objJson = {
    name : "dany",
    age : 30,
    size : 170
}
let objLinea = JSON.stringify(objJson);
localStorage.setItem("obj",objLinea);

**Get data**

>let objLinea = localStorage.getItem("obj");
let objJson = JSON.parse(objLinea);
alert(objJson.age) // return 30

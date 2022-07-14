# B38-day1-assesment
about object and diff between http1.1 and http2

object and its internal representation
```````````````````````````````````````
    The Object class represents one of JavaScript's data types. 
It is used to store various keyed collections and more complex entities.
 Objects can be created using the Object() constructor 
where all object arwe the instance of object. object can be overridden.
when change made in parent object it could reflect in child object too.
The Object constructor creates an object wrapper for the given value.
If the value is null or undefined, it will create and return an empty object.
If the value is an object already, it will return the value.
Otherwise, it will return an object of a Type that corresponds to the given value.
When called in a non-constructor context, Object behaves identically to new Object().

Static methods
```````````````
Object.assign()

Object.create()

Object.defineProperty()

Object.defineProperties()

Object.entries()

Object.freeze()

Object.fromEntries()

Object.getOwnPropertyDescriptor()

Object.getOwnPropertyDescriptors()

Object.getOwnPropertyNames()

Object.getOwnPropertySymbols()

Object.getPrototypeOf()

Object.is()

Object.isExtensible()

Object.isFrozen()

Object.isSealed()

Object.keys()

Object.preventExtensions()

Object.seal()

Object.setPrototypeOf()

Object.values()

Instance properties of object
``````````````````````````````

Object.prototype.constructor

Object.prototype.__proto__

Instance methods 
`````````````````
Object.prototype.__defineGetter__()

Object.prototype.__defineSetter__()

Object.prototype.__lookupGetter__()

Object.prototype.__lookupSetter__()

Object.prototype.hasOwnProperty()

Object.prototype.isPrototypeOf()

Object.prototype.propertyIsEnumerable()

Object.prototype.toLocaleString()
Calls toString().

Object.prototype.toString()

Object.prototype.valueOf()



 http1.1and http2
````````````````````
    HTTP stands for hypertext transfer protocol, and it is the basis for almost all web applications.
More specifically, HTTP is the method computers and servers use to request and send information. 
For instance, when someone navigates to cloudflare.
com on their laptop, their web browser sends an HTTP request to the Cloudflare servers for the content that appears on the page.
Then, Cloudflare servers send HTTP responses with the text, images, and formatting that the browser displays to the user.
this first version of HTTP was called HTTP/1.1. This version is still in use on the web. In 2015, a new version of HTTP called HTTP/2 was created.
HTTP/2 solves several problems that the creators of HTTP/1.1 did not anticipate.
In particular, HTTP/2 is much faster and more efficient than HTTP/1.1.
One of the ways in which HTTP/2 is faster is in how it prioritizes content during the loading process.
where http2 offer multiplexing
Some difference between http1.1 and http2
`````````````````````````````````````
Multiplexing:
    HTTP/1.1 loads resources one after the other, so if one resource cannot be loaded, it blocks all the other resources behind it. In contrast, HTTP/2 is  able to use a single TCP connection to send multiple streams of data at once so that no one resource blocks any other resource. HTTP/2 does this by splitting data into binary-code messages and numbering these messages so that the client knows which stream each binary message belongs to.

Server push:
    Typically, a server only serves content to a client device if the client asks for it. However, this approach is not always practical for modern webpages, which often involve several dozen separate resources that the client must request. HTTP/2 solves this problem by allowing a server to "push" content to a client before the client asks for it. The server also sends a message letting the client know what pushed content to expect – like if Bob had sent Alice a Table of Contents of his novel before sending the whole thing.

Header compression:
    Small files load more quickly than large ones. To speed up web performance, both HTTP/1.1 and HTTP/2 compress HTTP messages to make them smaller. However, HTTP/2 uses a more advanced compression method called HPACK that eliminates redundant information in HTTP header packets. This eliminates a few bytes from every HTTP packet. Given the volume of HTTP packets involved in loading even a single webpage, those bytes add up quickly, resulting in faster loading.

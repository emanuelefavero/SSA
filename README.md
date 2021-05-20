[![Build Status](https://i.ibb.co/xgPQnrw/SSA-logo-100.png)](https://github.com/emanuelefavero/SSA)
# SSA
#### _A micro JS DOM selector library similar to jQuery, in less than 100 bytes._

Yes, this is simply a dummy library to select DOM elements, if like me, this is all you use jQuery for ($('')), this is the library for you!

## Installation
#### online, using the link to the SSA.js file on github:
- Insert the following script tag in your html document, before your js script tag.
```<script src="https://emanuelefavero.github.io/SSA/SSA.js"></script>```

#### OR, Install locally:
- Clone this repository or download this .zip
- Copy "SSA.js" to the root of your project folder
- Insert the following script tag in your html document, before your js script tag.
```<script src="./SSA.js"></script>```

## Features

##### Select one DOM element:
- select the p element
```S('p')```
- select an element with an id attribute
```S('#idName')```
- select an element with a class attribute
```S('.class-name')```
- select a span inside a div
```S('div span')```
##### Select Multiple DOM elements
- select all p elements
```SA('p')```

PLEASE NOTE: like javascript, if you want to apply code to all elements at once you still need to use a loop, like this:
- change the color of all p elements to red
    ```
    SA('p').forEach((e) => {
    e.style.color = 'red';
    });
    ```

## FAQ
#### Is this library useless?

Not for us! Yes, we agree that this is so simple yet we needed a quick micro library to import in our projects that replaces the jQuery handy selectors, without the need to import such large library, add extra npm files or write each time the functions needed fow this library to work, clogging our js files. Thanks to this github page, we can import this library with just one line of html code snippet, and what we like is that it stays away from our js code.

#### Why the S?
Reason 1: We wanted something that resembles the jQuery dollar sign $ but was different so anybody that still uses jQuery will not have confilcts using both libraries.
Reason 2: S is short of Selector or Select, so "S('p')" can be read as "Select Paragraph" A is short of All, so SA means SelectorAll (like its JS counterpart)
#### I need to support old browsers, "forEach" does not work?
No problem, a for loop will work:
```
for (let i = 0; i < SA('p').length; i++) {
SA('p')[i].style.backgroundColor = 'green';
}
```
## Basic template:
```
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8" />
        <meta http-equiv="X-UA-Compatible" content="IE=edge" />
        <meta name="viewport" content="width=device-width, initial-scale=1" />
        <title>Document</title>
    </head>
    <body>
        <p>Hello, world!</p>

        <!-- SSA -->
        <script src="https://emanuelefavero.github.io/SSA/SSA.js"></script>
        <script>
            S('p').style.color = 'blue';
        </script>
    </body>
</html>
```

## License

MIT

**Enjoy!**

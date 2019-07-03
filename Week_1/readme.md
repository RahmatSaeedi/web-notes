# Notes for Week 1
## GIT
`git init`: Initialize a `GIT` folder.
`git remote add origin git@github.com:USERNAME/REPOSITORY.git`: Add a remote repository for `fetch` and `push` to `master branch`.
`git remote -v`: Lists existing remotes.
`git push -u origin master`: Lists existing remotes.


Linting, staging, committing, and pushing: 
```bash
%eslint% . --fix && git add . && git commit -m "{MESSAGE}" && git push
```

## Creating Nested Folders via Windows CMD

To create 10 folders named "Week_#", each containing 5 folders named "Day_#", and a *readme.md* file, run the following command via CMD

```bash
├─── Week_1
│   ├─── Day_1
│   │    ├─── Readme.MD
│   │    
│   ├─── Day_2
│   │    ├─── Readme.MD
│   │    
│   ├─── Day_3
│   │    ├─── Readme.MD
│   │    
│   ├─── Day_4
│   │    ├─── Readme.MD
│   │    
│   └─── Day_5
│        ├─── Readme.MD
│   
├─── Week_2
│   ├─── Day_1
│   │    ├─── Readme.MD
│   ...
│
...
│
│
├─── Week_10
│   ├─── Day_1
│   │    ├─── Readme.MD
│   │    
│   ├─── Day_2
│   │    ├─── Readme.MD
│   │    
│   ├─── Day_3
│   │    ├─── Readme.MD
│   │    
│   ├─── Day_4
│   │    ├─── Readme.MD
│   │    
│   └─── Day_5
│        ├─── Readme.MD

```

Run the following nested FOR-loop command in cmd.exe
 ```bash
    for /L %i in (1, 1, 10) DO (
        mkdir "Week_%i" &&
        cd "Week_%i" && 
        (
            for /L %j in (1, 1, 5) do
            (
                mkdir "Day_%j" &&
                echo  # Notes for Week %i: Day %j > "Day_%j\readme.md"
            )
        ) &&
        cd ..
    )
 ```

 ## [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
Headers
```markdown
# H1
## H2
### H3
#### H4
##### H5
###### H6
```
Links
```markdown
[Display Text](URL)
```

Images
```markdown
![alt text](image_URL)


![alt text][logo]
[logo]: http://...
```


Blockquotes
```markdown
> this is a blockqoute
```

## Lintting
Installation
```bash
    npm install -g eslint
```
Configuration
```bash
    # in general
    eslint --init

    # lighthouse Labs specific configuration
    curl -o /vagrant/.eslintrc.json https://gist.githubusercontent.com/kvirani/6cdb9511522d4357839718a050e7dd3b/raw/.eslintrc.json

```
Running
```bash
    eslint app.js
    
    # alternativly, to run it for all
    eslint .
```

## Truthy and Falsey

All of the following are inherently falsey:
```javascript
False
// False is False. Makes sense, right?

0
// 0 is the only falsey Number

""
// an empty string is falsey

null
// a null, or empty value, is falsey.

undefined
// an object that has not been defined is considered falsey.

NaN
// Not a Number. You'll learn more about NaN as we go on.
```

## Primitive Types in JavaScript
In JavaScript, all values which are not Objects are collectively referred to as primitives.
* *`undefined`*
* *`null`*
* *`boolean`*
* *`string`*
* *`number`*
* *`symbol`* *(introduced in ES6)*

## Objects
* Contain key-value pairs. Each key maps to a value
* Contain keys which are always strings (or symbols)
* Have unique keys
* Have their keys point to values which can be of any type

```javascript
// Empty object
const emptyObject = {};


// Examples of two objects with same `key`.
// The `key` is a string in both case 
const someObject1 = { "key": "value" };
const someObject2 = { key: "value" };
```
```javascript
const person = {
  first_name: "Ali",
  last_name: "Smith",
  address: {
    street: "100 Queen St W",
    city: "Toronto",
    province: "ON"
    postalCode: "M5H 2N2"
  }
  phone: 4163380685
};


// key-value
person["address"]["city"]; // => Toronto

```
`Object.keys(...) ` retuns the keys of an object

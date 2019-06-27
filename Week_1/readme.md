# Notes for Week 1
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
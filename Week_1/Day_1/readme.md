 "# Notes for Week 1: Day 1"         
## Creating Nested Folders via Windows CMD

To create 10 folders named "Week_#", each containing 5 folders named "Day_#", and a readme.md file, run the following command via CMD

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
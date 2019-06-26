 "# Notes for Week 1: Day 1"         
## Creating Nested Folders via Windows CMD

To create 10 folders named "Week #", each containing 5 folders named "Day #", and a readme.md file, run the following command via CMD

```bash
├─── Week 1
│   ├─── Day 1
│   │    ├─── Readme.MD
│   │    
│   ├─── Day 2
│   │    ├─── Readme.MD
│   │    
│   ├─── Day 3
│   │    ├─── Readme.MD
│   │    
│   ├─── Day 4
│   │    ├─── Readme.MD
│   │    
│   └─── Day 5
│        ├─── Readme.MD
│   
├─── Week 2
│   ├─── Day 1
│   │    ├─── Readme.MD
│   │    
│   ├─── Day 2
│   │    ├─── Readme.MD
│   │    
│   ├─── Day 3
│   │    ├─── Readme.MD
│   │    
│   ├─── Day 4
│   │    ├─── Readme.MD
│   │    
│   └─── Day 5
│        ├─── Readme.MD
│
├─── Week 3
│   ├─── Day 1
│   │    ├─── Readme.MD
│   │    
│   ├─── Day 2
│   │    ├─── Readme.MD
│   │    
│   ├─── Day 3
│   │    ├─── Readme.MD
│   │    
│   ├─── Day 4
│   │    ├─── Readme.MD
│   │    
│   └─── Day 5
│        ├─── Readme.MD
│
├─── Week 4
│   ├─── Day 1
│   │    ├─── Readme.MD
│   │    
│   ├─── Day 2
│   │    ├─── Readme.MD
│   │    
│   ├─── Day 3
│   │    ├─── Readme.MD
│   │    
│   ├─── Day 4
│   │    ├─── Readme.MD
│   │    
│   └─── Day 5
│        ├─── Readme.MD
│
├─── Week 5
│   ├─── Day 1
│   │    ├─── Readme.MD
│   │    
│   ├─── Day 2
│   │    ├─── Readme.MD
│   │    
│   ├─── Day 3
│   │    ├─── Readme.MD
│   │    
│   ├─── Day 4
│   │    ├─── Readme.MD
│   │    
│   └─── Day 5
│        ├─── Readme.MD
│
├─── Week 6
│   ├─── Day 1
│   │    ├─── Readme.MD
│   │    
│   ├─── Day 2
│   │    ├─── Readme.MD
│   │    
│   ├─── Day 3
│   │    ├─── Readme.MD
│   │    
│   ├─── Day 4
│   │    ├─── Readme.MD
│   │    
│   └─── Day 5
│        ├─── Readme.MD
│
├─── Week 7
│   ├─── Day 1
│   │    ├─── Readme.MD
│   │    
│   ├─── Day 2
│   │    ├─── Readme.MD
│   │    
│   ├─── Day 3
│   │    ├─── Readme.MD
│   │    
│   ├─── Day 4
│   │    ├─── Readme.MD
│   │    
│   └─── Day 5
│        ├─── Readme.MD
│
├─── Week 8
│   ├─── Day 1
│   │    ├─── Readme.MD
│   │    
│   ├─── Day 2
│   │    ├─── Readme.MD
│   │    
│   ├─── Day 3
│   │    ├─── Readme.MD
│   │    
│   ├─── Day 4
│   │    ├─── Readme.MD
│   │    
│   └─── Day 5
│        ├─── Readme.MD
│
├─── Week 9
│   ├─── Day 1
│   │    ├─── Readme.MD
│   │    
│   ├─── Day 2
│   │    ├─── Readme.MD
│   │    
│   ├─── Day 3
│   │    ├─── Readme.MD
│   │    
│   ├─── Day 4
│   │    ├─── Readme.MD
│   │    
│   └─── Day 5
│        ├─── Readme.MD
│
├─── Week 10
│   ├─── Day 1
│   │    ├─── Readme.MD
│   │    
│   ├─── Day 2
│   │    ├─── Readme.MD
│   │    
│   ├─── Day 3
│   │    ├─── Readme.MD
│   │    
│   ├─── Day 4
│   │    ├─── Readme.MD
│   │    
│   └─── Day 5
│        ├─── Readme.MD
│

```

Run the following nested FOR-loop command in cmd.exe
 ```bash
    for /L %i in (1, 1, 10) DO (
        mkdir "Week %i" &&
        cd "Week %i" && 
        (
            for /L %j in (1, 1, 5) do
            (
                mkdir "Day %j" &&
                echo  "# Notes for Week %i: Day %j" > "Day %j\readme.md"

            )
        ) &&
        cd ..
    )
 ```
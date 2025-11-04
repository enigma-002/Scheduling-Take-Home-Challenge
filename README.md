# Scheduling-Take-Home-Challenge

A Python based scheduling system which creates a schedule based off the number of users and the amount of days each will work.


## Table of Contents

- [About the Project](#AbouttheProject)
- [Requirements and Dependencies](#RequirementsandDependencies)
- [How to Run](#HowtoRun)
    - [Installation](#Installation)
    - [Running Tests](#RunningTests)
- [Author](#Author)
### About the Project

This script reads two JSON files to create a schedule.

The schedule is determined by the number of users and the amount of days they cover before a handover to the next user.

The second file contains overrides, times in which certain users "take over" for small periods of time.



### Requirements and Dependencies

* Python (I used 3.14.0)

Libraries
 
 * JSON
 * argparse
 * datetime


## How to Run

1) Download all the 3 files

- render-schedule
- schedule.json
- overrides.json

2) Ensure they are all in the same directory 

3) To run this you will need python so ensure you have downloaded it

4) Check what version of python you have by running 
```bash
     python --version
```
5) Given your version edit the hashbang at the top of the render-schedule file.

```bash
     #!/usr/bin/env python (add your version)
```

6) Now open a git bash and run this command 
```bash
 chmod +x render-schedule
``` 

7) Setup is now complete to run the scheduler you can now paste this into the git bash 
```bash
   python ./render-schedule --schedule=schedule.json --overrides=overrides.json --from='2025-11-07T17:00:00Z' --until='2025-11-28T17:00:00Z'
  ``` 
### Running Tests

Notice!

All time variables must be in ISO 8601 time format.


To run tests all you need to do is change the --from and --until variables as seen below. By changing the times you change when the schedule is made for. 

```bash
  --from='2025-11-07T17:00:00Z' --until='2025-11-28T17:00:00Z'
```

You can also populate schedule.json and overrides.json with more users and data to create different schedules just ensure anything you add is in json format to ensure no errors when running the script. 

## Author

- [@engima-002](https://github.com/enigma-002)







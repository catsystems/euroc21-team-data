# EuRoC 2021 Team Data
A shared repository for all EuRoC 2021 flights.

This repo is intended as a central location of all flight data recorded by the teams participating at EuRoC 2021. By sharing this data all of the teams can benefit from the gathered information.

## Repo Structure

The data should be organized in the following way:

```
/<team_name>-<rocket_name>  
  README.md  
  <source_1>
    <data>  
    README.md
  <source_2>
    <data>  
    README.md  
```   
   
Every team should place their flight data in their own directory. This directory should have a README.md file describing the flight parameters (including whether any active control was used).

Every data source should be placed in a separate subdirectory with its own README.md with the information describing the file formats (sensor types, sampling rate, measurement units, etc.), the location of the flight recorders within the rocket as well as any other useful information.

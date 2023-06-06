Hour tracking:
Specify the component worked on in Toggl, write down detailed descriptions into Trello.


## Mechanics
| **Features for MVP (ordered by priority)**                                      | **Hours required(estimation)** | **Hours spent** | **Priority** |
|:------------------------------------------------------------------------------- |:------------------------------ |:--------------- |:------------:|
| [[Design document Tank Simulator#Concepts Tank controller]]                     | 50                             | 77              |      1       |
| [[Design document Tank Simulator#Concepts Tank shooting system]]                | 80                             | 75.5            |      2       |
| [[Design document Tank Simulator#Concepts Damage registration & repair system]] | 80                             | 68              |      3       |
| [[Design document Tank Simulator#Concepts Level design]]                        | 30                             | 15                |      4       |
| [[Design document Tank Simulator#Concepts Enemy tank AI]]                       | 80                             |                 |      5       |
| [[Design document Tank Simulator#Concepts Main menu]]                           | 20                             |                 |      6        |
| [[Design document Tank Simulator#Concepts Tank customization]]                  | 70                             |                 |      7       |
| [[Design document Tank Simulator#Concepts Minimap/Tactical map]]                | 15                             |                 |      8       |

| **Features for MVP (ordered by priority)**                                      | **Hours required** | **Hours spent** | Priority |
|:------------------------------------------------------------------------------- |:------------------:| --------------- |:--------:|
| [[Design document Tank Simulator#Concepts Tank controller]]                     |         50         | 77              |    1     |
| [[Design document Tank Simulator#Concepts Tank shooting system]]                |         80         |  75.5               |    2      |
| [[Design document Tank Simulator#Concepts Damage registration & repair system]] |         80         |  76 (+8)              |      3    |
| [[Design document Tank Simulator#Concepts Level design]]                        |         30         |  15.5               |    4      |
| [[Design document Tank Simulator#Concepts Enemy tank AI]]                       |         80         |  95 (+95)              | 5         |
| [[Design document Tank Simulator#Concepts Main menu]]                           |         20         |  6.25 (+6.25)              |  6       |
| [[Design document Tank Simulator#Concepts Tank customization]]                  |         70           |                 |    7     |
| [[Design document Tank Simulator#Concepts Minimap/Tactical map]]                |         15           |                 |     8     |


| **Optional features (ordered by priority)**                          | **Hours required** | Priority |
| -------------------------------------------------------------------- |:------------------:|:--------:|
| [[Design document Tank Simulator#Concepts Enemy tank communication]] |         30         |          |

I'll be working at school 1/2 days a week, on Thursday & possibly Friday.

## Weekly plannings
Week 1-4
| Week | Feature/activity                                                       | What will I deliver                                                                                          |
|:---- |:---------------------------------------------------------------------- |:------------------------------------------------------------------------------------------------------------ |
| 1    | Brainstorming concepts, choosing & planning concept.                   | Design documents, hour planning estimations, technology research                                             |
|      | [[Design document Tank Simulator#Concepts Tank controller]]            | A tank movement system capable of moving in all direction. Full cannon mobility                              |
| 2    | [[Design document Tank Simulator#Concepts Tank controller]]            |                                                                                                              |
|      | [[Design document Tank Simulator#Concepts Tank shooting system]]       | A system that enables any type of tank to be capable of firing several types of shells. Including VFX (SFX?) |
| 3    | [[Design document Tank Simulator#Concepts Tank shooting system]]       |                                                                                                              |
|      | [[Design document Tank Simulator#Concepts Damage registration system]] | A system that registers damage, processes information into HUD elements                                      |
| 4    | Playtesting                                                            | The results of several playtests.                                                                            |
| 4    | [[Design document Tank Simulator#Concepts Tank controller]]                                                                       |                                                                                                              |

Week 5-8
| Week | Feature/activity                                                       | What will I deliver                                                                                           |
|:---- |:---------------------------------------------------------------------- |:------------------------------------------------------------------------------------------------------------- |
| 5    | [[Design document Tank Simulator#Concepts Tank shooting system]]       | A shooting system with mildots, range finding, compatible for all camera modes                                |
|      | [[Design document Tank Simulator#Concepts Tank shooting system]]       |                                                                                                               |
| 6    | [[Design document Tank Simulator#Concepts Tank shooting system]]   | A system that detects where a shell hit the tank, at what angle and calculates the damage done. Includes HUD. |
|      | [[Design document Tank Simulator#Concepts Tank shooting system]]   |                                                                                                               |
| 7    | [[Design document Tank Simulator#Concepts Damage registration system]]      | A system to repair specific parts of a tank. Including HUD                                                    |
| 8    | [[Design document Tank Simulator#Concepts Damage repair system]]       |                                                                                                               |
|      | Playtesting                                                            |                                                                                                               |

Week 9-12
| Week | Feature/activity                                                                | What will I deliver                                                                                           |
|:---- |:------------------------------------------------------------------------------- |:------------------------------------------------------------------------------------------------------------- |
| 5    | [[Design document Tank Simulator#Concepts Damage registration & repair system]] |                                                                                                               |
|      | [[Design document Tank Simulator#Concepts Tank shooting system]]                |                                                                                                               |
| 6    | [[Design document Tank Simulator#Concepts Tank shooting system]]                | A system that detects where a shell hit the tank, at what angle and calculates the damage done. Includes HUD. |
|      | [[Design document Tank Simulator#Concepts Tank shooting system]]                |                                                                                                               |
| 7    | [[Design document Tank Simulator#Concepts Damage registration system]]          | A system to repair specific parts of a tank. Including HUD                                                    |
| 8    | [[Design document Tank Simulator#Concepts Damage repair system]]                |                                                                                                               |
|      | Playtesting                                                                     |                                                                                                               |

## Week 5-9
### Week 5 | 20-03/24-03:
[[Design document Tank Simulator#Concepts Tank shooting system]]
- Range finding (mildots - scrapped)
- Turret & barrel rotation
	- Crosshair current rotation & target rotation
[[Design document Tank Simulator#Concepts Level design]]
- Made rough concept of level
- Started designing landscape
### Week 6 | 27-03/31-03:
[[Design document Tank Simulator#Concepts Tank shooting system]]
- Bullet drop physics formula
- Enemy UI indicators
[[Design document Tank Simulator#Concepts Level design]]
- Continuing landscape, working on military base & village

- Converting codebase into Finite State Machine.
- Converting camera code into Finite State Machine.
### Week 7 | 03-04/07-04:
[[Design document Tank Simulator#Concepts Damage registration & repair system]]
- Processing collision data
	- Calculate new tank data
		- Armor, health
		- VFX systems that visualize this data even more (more damaged = more fire/smoke)
- Tank inspection (player & hostile)
	- HUD & camera tweening

[[Design document Tank Simulator#Concepts Level design]]
- Continuing landscape, working on military base & village, oil refinery

- Improving Finite State Machine
### Week 8 | 10-04/14-04:
- Converted old input to the new input system

[[Design document Tank Simulator#Concepts Damage registration & repair system]]
- Tank inspection (player & hostile). Rotating around tank
- Convenient editor tool to control camera movement limitations

- Converted old HUDManager -> new FSM states
### Week 9(.5, this week) | 17-04/19-04:
[[Design document Tank Simulator#Concepts Damage registration & repair system]]
- Finish system

QA



## Week 9.5-13
### Week 9 (.5, this week) | 17-04/21-04:
[[Design document Tank Simulator#Concepts Damage registration & repair system]]
	- Finish system
	- Hostile inspection
### Week 10 | 24-04/28-04:
[[Design document Tank Simulator#Concepts Enemy tank AI]]
	- Research behaviour trees (incorporate into current FSM, or decouple FSM from enemy functionality and , other AI techniques)
	- Start designing/implementing actions & conditions for those actions 
		- Repairing
		- Initiating combat
		- Falling back
		- Patrolling, etc
	- Movement through the level (navmesh)
	- Strategy (communication between NPCs, or every NPC for itself)?

*Probably some work during the holiday as well (27-04/07-05)*
### Week 11 | 08-05/12-05:
[[Design document Tank Simulator#Concepts Enemy tank AI]]
Continue with AI behaviour.

### Week 12 | 15-05/19-05:
[[Design document Tank Simulator#Concepts Enemy tank AI]]
Continue with AI behaviour.

### Week 13 (week of 3rd evaluation?) | 22-05/26-05:
[[Design document Tank Simulator#Concepts Enemy tank AI]]
Finish AI behaviour.

[[Design document Tank Simulator#Concepts Main menu]]
Make a simple main menu that leads to the gameplay, tank customization & credits

[[Design document Tank Simulator#Concepts Tank customization]]
Start tank customization functionality
	- God mode in terms of money.
	- Menu UI (accessible from main menu)
	- Can re-use the InspectionState code

## Week 14-20
### Week 14 (this week) | 29-05/02-06:
[[Design document Tank Simulator#Concepts Enemy tank AI]]
- Finish AI behaviour tree
	- Implement & combine all main nodes together into the tree
	- Fix bugs
- Work on main menu
### Week 15 | 05-06/09-06:
- Start working on report
- Improve navmesh 
	- Remove slight elevations 
	- Replace with flat ground
- Finish main menu

### Week 16 | 12-06/16-06:
- Polishing

### Week 17 | 19-06/23-06:
- Work on report
### Week 18 (week of final evaluation..?) | 26-06/30-06:

### Week 19 (week of final evaluation..?) | 03-07/07-07:

### Week 20 (week of final evaluation..?) | 10-07/14-07:





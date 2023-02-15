 
Hour estimations can be found in [[Hour planning for Tank Simulator concept]].

# Features for MVP
### [[Concepts#Tank controller]]
The tank should be able to move back and forth, and rotate in a full range. When rotating, the cannon stays where it is. The cannon will only be moved by moving the mouse.
3 different camera modes:
	- 3rd person
	- 1st person
	- ADS

### [[Concepts#Enemy tank AI]]
Finite State Machines or Behaviour Trees for AI. I haven't done Behaviour Trees before, so that would be interesting to learn.
The AI should have an FOV system.

### [[Concepts#Tank shooting system]]
There should be a targeting/fire control system in place. Possibly automatic target finding/radar?
SFX for shooting, reloading.

Shells are physical objects in the scene. Speed shouldn't be too high, so that the player is able to see the shell coming their way. 

Screen shake on shell fired.

### [[Concepts#Damage registration system]]
When being shot at, it should be very clear what parts of the tank have been hit. A HUD element, on which you can see whether any part of the tank has been damaged, and how severe that damage is. Likely color code this (red value = 0: no damage, red value = 255: nearly/completely destroyed). When a part of the tank has under "X" % health, another hit will destroy the tank.

Damage example:
	When the tank has been hit with a shell in its right driving tracks, driving is affected. The player will not be able to drive straight until the damage has been repaired. Smoke particle systems should emit from the damaged spot. In the HUD element, the right side/tracks of the tank are highlighted with a red value.

When hitting an enemy, there should be a log of tank parts that have been damaged/destroyed.

### [[Concepts#Damage repair system]]
Just like there is a damage registration system, there should be a way to repair the damage.
Possibly just some UI indicators and sound effects to start with. 
The tank cannot be used while repairing is done (moving or shooting.)
Repairing can be done for any length; it's not required to repair all the damage, as long as the core systems still function. 
Note: there are "destroyed" tank models in the asset pack, so I can easily switch between those on death. Also add particle systems for fire, smoke & explosion.

### [[Concepts#Landmines]]


### [[Concepts#Level design]]
The level does not have to be complex. I might even use existing maps as inspiration (and give credit to those maps)? 
For example, the maps "Sinai Desert" and "Suez" from Battlefield 1 were some I enjoyed playing, in particular with tanks.

### [[Concepts#Tank customization]]
There should be a customization menu in game to choose & upgrade tanks.
Upgrade skills for tanks:
	- Health
	- Speed
	- Damage
Unlock shell types

Not sure if these upgrades should be reflected in any visual changes in the tank and how that would be done. Can also make a "level" system to indicate the strength of a tank. Show enemy level as well.

I can practice my editor scripting skills by making an editor with which I can change the properties of these tanks & upgrades.

### [[Concepts#Minimap/Tactical map]]
The map tracks the player position & direction, as well as some kind of objective? Show conquered terrain?
**![[TacticalMap.png|500]]

A compass which shows North - East- South - West, and a range of 360 degrees.
![[Compass.png]]

# Optional features - nice to have
### [[Concepts#Destructible buildings/terrain]]

### [[Concepts#Enemy tank communication]]
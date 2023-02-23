 
Hour estimations can be found in [[Hour planning for Tank Simulator concept]].

# Features for MVP
### [[Concepts#Tank controller]]
The tank should be able to move back and forth, and rotate in a full range. When rotating, the cannon stays where it is. The cannon will only be moved by moving the mouse.
3 different camera modes:
	- 3rd person
	- 1st person
	- ADS

The tank tracks should be animated so that it's clear the tank is driving when the camera is in 3rd person mode. I can do this by animating the UVs.
Tank tracks should respond to terrain changes.

### Final product:
- A reusable tank controller, with an editor window to control properties such as 
	- Movement speed
	- Rotate speed
	- Max speed
	- Wheelcollider settings, etc. 
- The tank controlling functionality (functions to rotate, move, etc) should be seperated from the input functionality (if Mouse X > 0), so the system can be reused for the AI agents.
- In the tool, you will find a list of all found tanks. You are able to easily select a tank and update its properties.

### Subgoals
- Camera modes
	- ADS
	- 1st person
	- 3rd person
		- When the barrel aims up, the camera should move towards the ground.
		- When the barrel aims down, the camera should move up.
		- The camera should always be exactly behind the turret.
- Rotations
	- Make sure all rotations are correct, when on a slope (angled surface) as well.
	- Hull rotation 
		- Tanks do this by speeding up one track faster than the other: rotating to the right? Speed up left track.
	- Turret rotation - full 360° degrees around the tank
	- Barrel rotation - rotate on x-axis, so it only moves up and down.
	- Offset turret rotation when tank hull rotates (if lock bool is true). This ensures the barrel always stays on target without having to move the mouse.
- Implement custom editor.
	- Find available tanks
		- Select a tank to edit properties
			- Tank mass, max speed, acceleration, single track acceleration
			- Wheel collider properties.

### Skills I want to learn
- Improve editor scripting skills (external editor window, not just a script with buttons in the inspector)
- Improve system design skills.
	- Reusability: make the system as modular & compatible for multiple types of tanks as possible.


### [[Concepts#Enemy tank AI]]
Behaviour Trees for AI. I haven't done Behaviour Trees before, so that would be interesting to learn.
The AI should have an FOV system.

### Final product:
 - A system I can use for all AI agents, to create behaviours that are used for AI agents to respond against player actions.

### Subgoals
 - An FOV system
	 - ~160°
- Possibly a custom editor, if necessary. Not for updating tank physical related properties, but for AI related properties.
	- FOV range
	- Max view range
	- Action response time
	- Accuracy for shell firing
	- Max shooting distance
	- other variables

### Skills I want to learn
 - An intermediate understanding of how behaviour trees work
 - The capability of writing my own.
 - Designing the behaviour tree, so that I can create several behaviours for AI to respond against player actions.

### [[Concepts#Tank shooting system]]
There should be a targeting/fire control system in place. Possibly automatic target finding/radar?
SFX for shooting, reloading.

The system should support all camera perspectives (ADS, 1st person, 3rd person).

Shells are physical objects in the scene. Speed shouldn't be too high, so that the player is able to see the shell coming their way. 

Screen shake on shell fired.
Dust particle system around tank on shell fired.
Tank kickback on shell fired.
Popup system
   - Reloading main cannon
   - Enemy hit
   - {TankPartName} hit/destroyed!

### Final product:
 - A shooting system I can use for both the player and AI agents.

### Subgoals
 - UI for all camera modes
	 - Reloading
	 - Popups
 - A physics-accurate shell-firing system
 - A formula to calculate shell force needed to hit the target.
	 - If fired shell comes from an AI agent, include an "accuracy" variable into the formula.
 - Particle systems on shell fire & hit
 - Sound effects
	 - Shell fire & hit
	 - Reloading

### Skills I want to learn
 - System design.
 - A better understanding of how physics affect shell travel.

### [[Concepts#Damage registration system]]
When being shot at, it should be very clear what parts of the tank have been hit. A HUD element, on which you can see whether any part of the tank has been damaged, and how severe that damage is. Likely color code this (red value = 0: no damage, red value = 255: nearly/completely destroyed). When a part of the tank has under "X" % health, another hit will destroy the tank.

Damage example:
	When the tank has been hit with a shell in its right driving tracks, driving is affected. The player will not be able to drive straight until the damage has been repaired. Smoke particle systems should emit from the damaged spot. In the HUD element, the right side/tracks of the tank are highlighted with a red value.

When hitting an enemy, there should be a log of tank parts that have been damaged/destroyed.

### Final product
- A system compatible with both the player tank and enemy tanks.
- Capable of registering damage from any source, and relays information to the HUD. 

### Subgoals
- UI design
-   

### Skills I want to learn

### [[Concepts#Damage repair system]]
Just like there is a damage registration system, there should be a way to repair the damage.
Possibly just some UI indicators and sound effects to start with. 
The tank cannot be used while repairing is done (moving or shooting.)
Repairing can be done for any length; it's not required to repair all the damage, as long as the core systems still function. 
Note: there are "destroyed" tank models in the asset pack, so I can easily switch between those on death. Also add particle systems for fire, smoke & explosion.

### Final product
- A system compatible with both the player tank and enemy tanks.
- 

### Subgoals


### Skills I want to learn

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

I've found that the asset pack contains several "vehicle attachments", such as armor plates, storage crates, fuel jerrycans, lights, different types of cannon shells. With this, I can also make visual changes to the tank when upgrading rather than only a graph.
Can also make a "level" system to indicate the strength of a tank. Show enemy level as well.

I can practice my editor scripting skills by making an editor with which I can change the properties of these tanks & upgrades.

### Final product
- A customization menu, in which the player can view the tank and choose upgrades.
  Upgrades are applied visually if possible (attachment models), and stats are shown as graphs.

### Subgoals
- UI menu
- Custom editor
	- Upgrade tank properties
		- Acceleration
		- Max speed
		- Health
		- Armor
		- ADS speed
		- More fuel?
		- Lighting upgrade
		- Smoke cannisters
		- Ammo count?
		- Repair speed
	- Buy new types of shells
		- Armor piercing
		- Gas (affects armor over time?)
		- Napalm?

### Skills I want to learn
- Improved editor scripting skills
- Tween animations?
- 

### [[Concepts#Minimap/Tactical map]]
The map tracks the player position & direction, as well as some kind of objective? Show conquered terrain?
**![[TacticalMap.png|500]]

A compass which shows North - East- South - West, and a range of 360 degrees.
![[Compass.png]]

# Optional features - nice to have
### [[Concepts#Destructible buildings/terrain]]

### [[Concepts#Enemy tank communication]]
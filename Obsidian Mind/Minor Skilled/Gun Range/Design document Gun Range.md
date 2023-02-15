Hour estimations can be found in [[Hour planning for Gun Range concept]].

# Features for MVP
### [[Concepts#Character controller]]
The player should be able to do the basic movement controls, such as: 
- moving in any direction regardless of camera rotation,
- jumping with a certain force
- crouching

A 1st-person camera system should be in place.
- rotate camera in all directions
- rotate player when rotating camera
- keep track of player eye position; when crouching, lower camera

### [[Concepts#Shooting system]]
There should be an extendable gun-shooting system. I'll need [[Researched technologies & algorithms#Object pooling]] for this.
- Switch between auto/semi auto fire mode to easily customize weapons.
- Fire rate, damage, range,
- Accuracy counter ^690910
	- Shots missed - decrease accuracy grade
	- Headshots hit - slightly increase 
- Bullet drop-off in damage, range
- Cycle through weapons. Works together with [[Concepts#Inventory System]]

### [[Concepts#Gun range level design(s)]]
A basic gun range level should be present of course. A very simple version can be like this:
![[GunRange2Example.png|400]]
I'll be limited to the assets of the asset pack, so it won't look like this. This should also be a very early prototype range, most likely not the final one. Ideally, I'd like to have an area where the player can navigate through a __somewhat__ indicated path, where dummies (friendlies/hostiles) can pop up.

### [[Concepts#Dummy spawning system]]
While moving through the previously mentioned gun range, dummies (friendlies/hostiles) can pop up, which the player will have to shoot. Hitting friendlies costs them points, hitting hostiles awards them.

As mentioned in the [[Design document Gun Range#^690910]] paragraph, a points system works together with the dummy spawning system. 

In the prototype gun range, dummies will spawn in random "columns" at random positions in that column. 
In the final gun range, dummies will likely spawn at designated positions, but will choose randomly between hostiles & citizens.

### [[Concepts#Inventory System]]
Similar to the following inventory system, ![[InventorySystem.png]]the player should be able to inspect their current loadout (weapons, armor, other tools). 
The player should also be able to pick up items from the world, which will show in this inventory UI.

### [[Concepts#Player/enemy animations]]
Animations make a project look much better (if the animations are good). Since I'm obviously not an animator, I'm not making them. Luckily, the website https://www.mixamo.com/#/ has a ton of (or at least enough for me) animations, and they work seamlessly with the models Synty Studios made as they recorded an official tutorial on how to set up a basic animation controller for their humanoid models. Still, this is probably the last feature I'll implement for the MVP as the player's hand don't necessarily have to be visible and the dummies might not have to move.


# Optional features - nice to have
### [[Concepts#Minimap]]
As is often common in FPS games, there could be a minimap in some corner of the screen. It would show a simplified expression of the environment (outlines of the objects in the world?), the position and direction of the player, and the position of dummies/AI. Not necessarily the direction for those.

### [[Concepts#Commanding Officer AI]]
As sort of a motivating presence in the gun range, I might want an AI agent which would give commentary on the player's performance in the range, like the following lines:
Start of the gun range:
- "Stay focused. Stay alive."
- "No mistakes."
- "We've got a green light! MOVE YOUR ASS"

During gun range:
- "Come on maggot, I've seen you do better than this!"
- "You've got to get faster and better if you want to survive in the field."

After gun range:
- "Acceptable."
- "You'd be dead if those dummies were real."

While I don't think it's likely I'll find these voice-overs or anything similar of high-quality without paying for it (although I am willing to pay a small amount for it), I might be able to record them myself and put some filter on it. But this feature definitely won't be part of the MVP, and is only a nice-to-have.

### [[Concepts#Enemy bot AI.]]
Instead of stationary dummies, I might want moving bots going through the gun range. Of course the main priority is to have regular dummies working. 

The AI would also have to be able to shoot, make decisions on hiding/running to a hiding spot or vantage point, retreat, etc, causing this to probably be a complex feature. 

### [[Concepts#Killstreak system]]
A system with which you can try out several killstreaks, such as an airstrike, UAV, RCXD etc. Also an optional feature. 

### [[Concepts#Loadout customization]]
Preferably a physical shop location in the gun range, where you can choose a loadout (weapons, possibly armor), and customize those items. Optional feature.
![[Forge.png|400]]
A bit similar to this, but in a middle eastern style and instead of a smithy, a market stall and guns instead of swords.

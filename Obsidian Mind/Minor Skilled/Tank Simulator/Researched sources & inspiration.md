Gunner Heat PC
Warthunder
World of Tanks
GTA V
![[Pasted image 20230314094406.png]]
	- The blue circle represents the direction the player will aim when the barrel has finished rotating
	- The red circle represents the direction the barrel is currently aiming.
	- This means the turret rotation isn't instant - turret should take some time to rotate to the new position.
		- implement free look to allow for environment inspection? Middle mouse button press

![[Pasted image 20230314094647.png]]
![[Pasted image 20230314094738.png]]
- Range finding system - feasible to make?
- Mildots
- Default distance of 100m, adjust Y coordinates of the vertical UI element. Raise/lower tank barrel based on that information
![[Pasted image 20230314095029.png]]
- Tank consists of real seperate elements (tracks, side armor, turret)
- Effective thickness
	- The higher the angle of the shell against the armor, the higher the "effective thickness", making the armor harder or easier to penetrate based on the angle.
		- So if a shell hits armor in a perpendicular way, the effective thickness = thickness.
		- If a shell hits armor with an angle other than 90°, the effective thickness increases, making the armor harder to penetrate.
![[Pasted image 20230314095313.png]]
- Armor thickness, tank mass, engine power, max speed
	- Max speed: 16.5 kt = 30.558 km/h. Formula to convert to km/h: multiply kt with 1.852.
![[Pasted image 20230314095125.png]]
 - Several types of tank shells. Each with its own shell properties (velocity, caliber, mass etc)

![[Pasted image 20230314101737.png]]
 - Indication of where the shell hit

![[Pasted image 20230314101831.png]]
 - World space canvas for allies/enemies, showing their name/tank type?

![[Pasted image 20230314102634.png]]
- Compass 
![[Pasted image 20230315153146.png]]
Gear shifting system?
1. Is it obvious for every class/method what it is supposed to be doing?
	- yes, no suggestions for readability besides changing some magic values into variables
2. Can/should the code be broken down further into more classes/methods?
	 - The HUD-related code can be converted to a Singleton, which holds a collection with references to all entities with HUD data (player, enemies). The entities can then call functions in that manager which updates the HUD accordingly.
3. Are there any obvious performance issues?
	-  Remove some local Vector3's and the FindObjectWithTag call. 
4. Are there any logic issues?
	- None
2. How can the communication with the HUD be improved (base class - subclasses)?
	- Mentioned in question 2
3. How consistent are the naming conventions?
	- Very consistent
1. Other suggestions
	Remove old/unused code & variables
	Remove GetComponent for rigidbody, assign in inspector and do a nullcheck in onvalidate()
	Migrate to new input system
	Be careful with nesting components to prevent calls like component.movecomponent.component.component.Function()
	namespaces/assembly definitions
	Better to have a GameManager with a reference to the player rather than Gameobject.Find()/WithTag()


Remove old/unused code
hud max update time change to constant variable


remove getcomponent voor rigidbody, assign in inspector
private void onvalidate(){
	if(centerofmass == null)
	{
		debug.logerror
	}
}


replace 4 with properties.maxgears

playerhud replace with singleton manager (use new script)
	dictionairy with enemy 
		Update health etc through there


kickbackforce naar tankproprerties verplaatsen

fingameobjectwithtag in enemyhud too expensive
	better to have a gamemanager with a reference to player as variable


migrate to new input system
	this removes all the input values

camera component playerinput serializefield en onvalidate


Careful with components: nesting
	component.movecomponent,.component.component.

shell
	rb.addexplosiioonforce(force onimpact, transform.position, 1)
		remove 1 and change to variable
	var transformExplosiion = exploision.transform instead of repeated access

camera component: distanceDamp naar const
![[Pasted image 20230315211404.png]]

remove magic numbers in updateCameraPOisition() & offsetCameraOnCannonTilt()
remove local vector3 and introduce variable for all vector3 in turretControlcomponent

namespaces/assembly definitions
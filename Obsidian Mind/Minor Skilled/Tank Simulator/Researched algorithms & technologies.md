## Object pooling
Used to spawn large amounts of bullets, enemies or other objects. Particle systems, decals, etc. A substantial amount of instances of a prefab are instantiated at the start of the game, which will then be reused during runtime. Depending on the amount of instances and the amount of types, this can still cause quite a frame drop in the first frames, so it would be a good idea to use coroutines. This would allow me to spread out the instantiating over multiple frames (or even seconds).

## Behaviour trees
Combined with [[Researched algorithms & technologies#Multithreading/Jobs system/Burst compiler]], I can create behaviour trees for the AI in the project. Multithreading will mostly likely be used for pathfinding, depending on the implementation. The Jobs system doesn't work with any "Unity" code (GameObjects, transform, NavMesh etc), but only accepts so-called "blittable data types". 
- Abstract class behaviour tree
	- Branch setup is defined statically in every custom node class. If you want a slightly different parent node, you have to create a new node for it (or another tree class, redefining the nodes).
	- Agent values are reset automatically (health, target position etc) when exiting the game, so they are not stored. 
	- Values are NOT shared between agent instances.
- Scriptable object behaviour tree
	- Branch setup can be completely customizated for every behaviour tree instance.
	- Values in the blackboard are not reset on game exit. Values in the blackboard are shared between enemies (if they use the same blackboard asset instance)
		- Solution would be to not store agent-specific values (like NavMeshAgent reference, current agent moveposition) in the blackboard, but rather in a monobehaviour component attached to the agent.

## Design patterns
Already learned about this during the Software Architecture course, but I'm sure there are a lot of refinements possible, and of course quite a few new things to learn as well.

## Multithreading/Jobs system/Burst compiler
Used to run several processes at the same time. Unfortunately it's not possible to instantiate GameObjects in a different thread, so I can't combine it with Object Pooling to prevent the initial dropoff in performance when spawning the object pools.

However, I can still use it for the pathfinding & decision making of enemies. Refer to [[Researched algorithms & technologies#Behaviour trees]] for this.

## Finite State Machine
Another type of AI system. Although I already worked with this a few times, so I would rather learn about [[Researched algorithms & technologies#Behaviour trees]] to broaden my knowledge about AI. Behaviour trees might also be a better fit for my project.

In the FSM, there are several "states". Only one of these states can be active at the same time.
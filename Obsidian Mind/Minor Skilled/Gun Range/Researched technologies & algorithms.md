### Object pooling
Used to spawn large amounts of bullets, enemies or other objects. Particle systems, decals, etc.

### Multithreading/Jobs system/Burst compiler
Used to run several processes at the same time. Unfortunately it's not possible to instantiate GameObjects in a different thread, so I can't combine it with Object Pooling to prevent the initial dropoff in performance when spawning the object pools.

However, I can still use it for the pathfinding & decision making of enemies. Refer to [[Researched technologies & algorithms#Behaviour trees]] for this.

### Behaviour trees
Combined with [[Researched technologies & algorithms#Multithreading/Jobs system/Burst compiler]], I can create behaviour trees for the AI in the project. 

### Design patterns
It's important to keep structure in the project code base, especially when a lot of systems have to interact with eachother.

## CIS 568: Co-op Tower Defense
### Team members: Krishna Bharathala, Devesh Dayal, Natasha Narang, Carolina Zheng

Check out our project here: [Youtube](https://www.youtube.com/watch?v=BLJsaGhtmEM)
    
### Game Mechanics
There is one central castle in the game which serves as home base. The players spawn on one of three pillars which circle the castle and have to protect the castle from goomba attacks. Goombas have spawn points throughout the level and travel inwards towards the center of the map. When a goomba reaches the castle, it explodes and inflicts some amount of damage on the castle.  

##### Arrow Mechanics
There are two types of arrows in the game, teleportation arrows and damage arrows. 
* Teleportation arrows (silver) allow you to teleport anywhere on map within the bounds of the playing field.
* Damage arrows (gold) are used to destroy the goombas attacking your castle.
    
##### Castle Mechanics
Your castle starts with 100 health points and decreases by 5 every time a goomba explodes within it. When the health of the castle reaches 0, the game is over.

##### Multiplayer
One player creates a new game and other players search for games within the lobby. When joining a game, the two or more players will spawn at different locations and now have a joint mission to protect their castle at all costs.

### How to play

1. Nock your arrow. Bring your bow and arrow together in front of you and hold down the arrow trigger.
2. Charge your bow by pulling back with your arrow hand. The brighter the bow glows, the more force applied to the arrow.
3. Fire by releasing the arrow trigger.
4. Reload a new arrow by pressing the grip while reaching over your shoulder.

You can toggle between damage (gold) and teleport (silver) arrows by pressing the bow trigger.

### Techniques

#### Mechanical
##### Arrow drawback UX
We wanted to give the user a realistic experience of shooting an arrow within VR. To do this, we added several stages to arrow shooting. First the user must nock an arrow, and then pull back to "charge" the arrow, determining the velocity of the arrow once it is shot. We measure the power of the shot by the x-y distance between the two controllers. We opted for x-y distance instead of just x, sacrificing some level of realism to make arrow shooting easier and more enjoyable. Whenever the power level increases, the user receives haptic feedback in the form of their arrow controller vibrating, giving the feeling of tension when pulling back a string.

##### Arrow reloading
The user must grab a new arrow in between shots by reaching behind them and pressing the grip on their controller. We implemented this by adding a cube component to our character blueprint that served as a hit box. When the user presses the grip, we check whether the arrow controller is currently overlapping the cube to determine whether to reload the arrow. If a reload was successful, the controller vibrates.

##### Teleporting to top of pillars
When the user shoots a pillar, they are teleported to the top, allowing them to shoot goombas from a high angle. We determine the z location where the user should be translated by getting the bounding box of a cylinder component included in our pillar.

#### Visual
##### Arrow smoke trail
We realized that arrows needed to be more visible as they were flying through the air, especially in multiplayer when some arrows are shot by the other player. To achieve this, we added a particle system to the tail of our arrow. The particle system consisted of an emitter with TypeData ribbon that was linked to the arrow actor, allowing it to emit smoke-like particles along the trail of the arrow. The material we used for this was a simple semi-transparent material.

##### Charging bow glow
We also wanted to provide the user visual feedback as to the power level of the arrow they are about to shoot. After a suggestion from the instructor, we realized we could do this by making the bow glow with proportion to the power level. We edited the bow material, changing it from Opaque to Translucent, and adding an Emissive Color property, which consisted of a yellow color, scaled by a vector. The size of each component of the vector is scaled up in our bow drawing code based on the current power level. This allowed the bow to nicely glow when the user's arrow is close to full power.

##### Teleportation fade
We wanted the teleportation transition to be less jarring for the user. To do this, we employed a camera fade. Once a user's teleportation arrow hits the ground, we start a camera fade transparent to black for 0.2 seconds. Then, we teleport the user to the new location, and start a camera fade from black to transparent for another 0.2 seconds. We needed to use a timer with a callback to our teleport function to delay the teleportation until the user had faded to black.

##### Castle fire
When the castle health reaches certain levels, the castle catches fire to indicate that the health of the castle is diminishing.


### VR Mode
In our testing we have not felt motion sickness while playing the game. We believe the primary reason for this is due to the fading that we employ during teleportation. There is no other significant movement during the game.

### Hardest Part of the Assignment
Our team spent a lot of time working on getting multiplayer support for our game. The hardest part was making sure that the replication carried across client to server and did not affect game play in single player mode. In a similar vein, we spent a lot of time working on figuring out how to get teleportation to work on the client games.

### What do we wish we had done differently?

* One of the biggest thing we would change is to make the AI more intelligent in the game. Currently all the goombas spawn in the same locations around the map and then converge on the same point. In fact, there’s a funny bug which can occur if the goombas all converge in the castle at the same time. Instead we could have randomly spawned the goombas in various locations, with various speeds and targets.

* We could have also changed the way we displayed castle health. Currently it is on top of the castle which means that you cannot monitor health while inside the castle. Instead we could have had the display on the character some how.

* We also wished we had time to figure out how to deform the bowstring upon drawing back the arrow, which would have greatly improved the visuals and realism of the arrow shooting.

* Other extensions we would have liked to have had the time to implement were multiple arrow types and different damage level goombas.

### What do we wish you had done differently?

* We wish that we could have had more tips regarding "gotchas" that can occur with how Unreal handles server-client multiplayer. Specifically, we had a lot of trouble getting a reference to the player character because "Get Player Character" will always return the server, regardless of who calls it.


---------

### Work Division
Krishna: Multiplayer, Lobby

Devesh: Multiplayer, UX/UI, Lobby

Natasha: Assets and components, blueprint logic

Carolina: Blueprint logic, UX/UI

### Timeline

Thursday, February 16: [Alpha Demo](https://github.com/PennVR/unreal-project-materials-and-textures/releases/tag/Alpha)
   * Basic Arrow Shooting
   * Basic Assets in Level
   * Xbox Controllers Working

Thursday, February 23: [Beta Demo](https://github.com/PennVR/unreal-project-materials-and-textures/releases/tag/Beta)
  * Both types of arrow shooting
  * Teleportation
  * More detailed asset-building: castle, towers, etc.
  * Improved game logic - game-ending logic
  * Vive Controllers Working
  * Game lobby
  * Basic Multi-player

Tuesday, February 28: Final Demo
 * Multiplayer
 * Game Logic
    * Game mechanics
      * Arrow firing movement detection
    * Character and arrow blueprints
       * Teleportation
       * Spawn location/respawn mechanics 
    * End Game Logic
 * Assets
    * Level creation
    * Player/arrow components
 * UX/UI
    * Power Indicators
    * Visual/haptic feedback on game state changes
    * Game lobby
    * Tutorials
    * Arrow Nocking
 * VR
    * Vive Controllers working
    * No Motion Sickness

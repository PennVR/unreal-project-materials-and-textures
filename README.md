## CIS 568: Co-op Tower Defense
### Team members: Krishna Bharathala, Devesh Dayal, Natasha Narang, Carolina Zheng

Check out our project here: https://www.youtube.com/watch?v=BLJsaGhtmEM

### Technical Requirements
 * Multiplayer
 * Game Logic
    * Game mechanics
      * Arrow firing movement detection
    * Character and arrow blueprints
       * Teleportation
       * Spawn location/respawn mechanics 
 * Assets
    * Level creation
    * Player/arrow components
 * UX/UI
    * Power Indicators
    * Visual/haptic feedback on game state changes
    * Game lobby

It will probably be challenging to integrate multiplayer into the game. Multiplayer and writing the blueprint logic will likely take the most time and debugging and should be worked on the most up front (given that we have a basic level and assets in place). UX/UI can be left until near the end.

### Work Division
Krishna: Multiplayer, Lobby

Devesh: Multiplayer, UX/UI, Lobby

Natasha: Assets and components, blueprint logic

Carolina: Blueprint logic, UX/UI

### Timeline
Friday, February 10: Partial Team Meeting (bootstrapping the project)

Sunday, February 12: Team Meeting (working to get alpha demo ready)

Thursday, February 16: Alpha Demo
* Features to be completed by Alpha Demo:
   * Basic Arrow Shooting
   * Basic Assets in Level
   * Xbox Controllers Working
   
Sunday, February 19
* Features 
   * Castle Health
   * Goomba AI
   * Castle Explosions
   * Vive Initial Setup

Wednseday February 22: Meeting
* Features Started
   * Lobby creation
   * Multiplayer
      * Session Creation
      * Session Joining
   * VR
      * Haptic Feedback
      * Arrow pullback

Thursday, February 23: Beta Demo
* Features to be completed by Beta Demo:
  * Both types of arrow shooting
  * Teleportation
  * More detailed asset-building: castle, towers, etc.
  * Improved game logic - game-ending logic
  * Vive Controllers Working
  * Game lobby
  * Basic Multi-player

Tuesday, February 28: Final Demo

### Game Mechanics
There is one central tower in the game which serves as home base. The players spawn on pillars which circle the tower and have to protect the tower from Goomba Attacks. Goombas have spawn points throughout the level and travel inwards towards the center of the map. When a Goomba reaches the tower, it explodes and inflicts some amount of damage on the tower.  

* Arrow Mechanics
There are two types of arrows in the game, teleportation arrows and damage arrows. Teleportation Arrows (Silver) allow you to travel anywhere on map within the bounds of the playing field. You use these to get around. Damage Arrows (Gold) are used to destroy the Goombas attacking your tower.

### How to play

* Arrows
   1. Nock your arrow. Bring your bow and arrow together in front of you and hold down the arrow trigger.
   2. Charge your bow by pulling back with your arrow hand. The brighter the bow glows, the more force applied to the arrow.
   3. Fire by releasing the arrow trigger.
   4. Reload a new arrow by pressing the grip while reaching over your shoulder.
   5. Toggle between damage (gold) and teleport (silver) arrows by pressing the bow trigger.
   
* Castle
Your castle stars with 100 health points and decreases by 5 everytime a goomba explodes within it. When the health of the castle gets down to 0, the game is over.

* Multiplayer
One player creates a new game and other players search for games within the lobby. When joining a game, the two or more players will spawn at different locations and now have a joint mission to protect their castle at all costs.

### VR Mode
In our testing we have not felt motion sickness while playing the game. We believe the primary reason for this is due to the fading that we employ during teleportation. There is no other significant movement during the game.

### Hardest Part of the Assignment
Our team spent a lot of time working on getting multiplayer support for our game. The hardest part was making sure that the replication carried across client to server and did not affect game play in single player mode. In a similar vein, we spent a lot of time working on figuring out how to get teleportation to work on the client games.

### What do we wish we had done differently?



### What do we wish you had done differently?


  




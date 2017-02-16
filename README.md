## CIS 568: Co-op Tower Defense
### Team members: Krishna Bharathala, Devesh Dayal, Natasha Narang, Carolina Zheng

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
    * Health/energy indicators
    * Visual/haptic feedback on game state changes
    * Game lobby

It will probably be challenging to integrate multiplayer into the game. Multiplayer and writing the blueprint logic will likely take the most time and debugging and should be worked on the most up front (given that we have a basic level and assets in place). UX/UI can be left until near the end.

### Work Division
Krishna: Multiplayer, HUD

Devesh: Multiplayer, UX/UI

Natasha: Assets and components, blueprint logic

Carolina: Blueprint logic, UX/UI

### Timeline
Friday, February 10: Partial Team Meeting (bootstrapping the project)

Sunday, February 12: Team Meeting (working to get alpha demo ready)

Thursday, February 17: Alpha Demo
* Features to be completed by Alpha Demo:
   * Basic Arrow Shooting
   * Basic Assets in Level

More meetings

Tuesday, February 21: Beta Demo
* Features to be completed by Beta Demo:
  * Both types of arrow shooting
  * Teleportation
  * Basic multiplayer 
  * More detailed asset-building: castle, paths, etc.
  
More meetings

Tuesday, February 28: Final Demo

### Game Mechanics
There is one central tower in the game which serves as home base. The players spawn on pillars which circle the tower and have to protect the tower from Goomba Attacks. Goombas spawn randomly throughout the level and travel inwards towards the center of the map. A Regular Goomba will explode after being hit by one arrow, and we hope to add different types for our "Beta Demo" and "Final Game". When a Goomba reaches the tower, it explodes and inflicts some given amount of damage on the tower.  

* Arrow Mechanics

   1. “type” of arrow (Different types have different properties and different levels of damage). Some possibilities are freeze arrows (no damage, but cause the goomba to freeze in place) and power arrows (Each player only has three of these but they do double damage).

   2. “Power” of arrow: This is determined by how far back the player pulls the arrow. The further back the player pulls, the faster the arrow travels and the more damage it does.





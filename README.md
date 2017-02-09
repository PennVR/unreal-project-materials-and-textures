## CIS 568: Unreal Engine Project
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
Krishna: Multiplayer, teleportation

Devesh: Multiplayer, UX/UI

Natasha: Assets and components, blueprint logic

Carolina: Blueprint logic, UX/UI

### Timeline
Friday, February 10: Partial Team Meeting (bootstrapping the project)

Sunday, February 12: Team Meeting (working to get alpha demo ready)

Thursday, February 17: Alpha Demo
* Features to be completed by Alpha Demo:
   * Basic Arrow Shooting
   * 2 Levels

More meetings

Tuesday, February 21: Beta Demo
* Features to be completed by Beta Demo:
  * Both types of arrow shooting
  * Teleportation
  * Basic multiplayer 
  * 4-5 Levels

More meetings

Tuesday, February 28: Final Demo

#### Game Mechanics
Win Conditions: We are choosing between two different modes for winning in our game. 

Survival: Each player has a health meter and dies when they run out of health. The amount of damage that a player takes is determined by:

1. “type” of arrow (Different types have different properties and different levels of damage). Some possibilities are freeze arrows (no damage, but cause the opposing player to lose the ability to teleport for some time) and power arrows (Each player only has three of these but they do double damage).

2. “Power” of arrow: This is determined by how far back the player pulls the arrow. The further back the player pulls, the faster the arrow travels and the more damage it does.

Score: Every time an arrow lands on an opponent, the player gets a certain score determined by the type and power of the arrow as stated above. The first to reach a certain point number wins.





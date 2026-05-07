# GDIM 33 In-Class Activities
## Week 1
### Activity 1
[Game Inspo Pinterest Board](https://www.pinterest.com/gandresp20/gdim33-game-inspo/)

1. Some patterns I'm noticing in my inspiration is a sort of rivalry that the player may have with an NPC throughout the level/game. My inspiration comes from racing, more specifcally Formula 1 and some photos have crashes from F1 so perhaps I could add a mechanic where the player could try and damage NPC's cars which could turn back on the player and have them accidently damage their own car in the process. Some photos are from the movie, "Rush" which is based on a rivalry between two F1 drivers and the last race has one rival stop racing due to their injuries and the other rival continues despite the heavy rain. So what I was thinking was that I could possibly have rain appear and have lighting be a sort of power-up for the player that can make them go faster (unrealistic but still would be a fun mechanic to add).
2. My table-mate is interested in building a 2D platformer game but isn't quite sure what the game will be centered around. We both related to choosing the 2D platformer because we find the simplicity of 2D games easier to work with compared to 3D games in Unity.
3. My LA mentioned that another student a year ago did a game that was similar to mine in the aspect that it was a racing game. It was really cool to see that past students have similar interests to me such as racing.


### Activity 2
![F1 2D Racing Game Break-Down](https://github.com/user-attachments/assets/3677d0c4-9eae-4f36-b5bd-47507babf770)


## Week 2
Link to Commit for In Class Activity: [In Class Activity Week 2](https://github.com/gaelp-io/GDIM33-InClassActivities/commit/0303c26613d84d2d5b25e12be647be43f6df6c8e)

## Week 3
### Activity 1
Updated Break-Down
<img width="960" height="720" alt="F1 2D Racing Game Break-Down (3)" src="https://github.com/user-attachments/assets/2e11031f-4d0d-4537-bf4a-916dd7dfffe0" />

### Activity 2
1. It is advantageous to save "clickNpcEventName" as a scene variable because it allows us to access from any graph we are currently using in the scene.
2. Using a Debug log for when the Walrus is clicked was really helpful because it allowed us to see that the issue was the transition not firing instead of thinking that the click wasn't registered.
3. For my Vertical Slice the Set Cursor Lock State won't be relevant since my game is 2D it won't require any use for a cursor I won't need this state. Also, in general 2D games don't require cursors to be locked, usually they just disappear not lock, if the player isn't in a dialogue state.
4. The concept of a game state will be relevant in my game because since I am doing 2D I need a power up item which will change the state of the player whenever they equip it. Also, whenever the player is attacking an NPC in my game, the state will chaneg to stop them from moving and to have them complete a QTE.

## Week 4
### Activity 1
- What is currently playable in my build: I have a start menu and game scene that can be accessed back and forth by players, I have movement for the player down, I have a working timer that starts for whenever the player enters the game scene, and finally I have a powerup that spawns after 5 seconds of playing within the game scene.
- Playtesting goals:
    - See if players like the aesthetic of the game
    - See if playermovement is smooth
    - Get players' thoughts on the speed boost
- Playlist Team Members: Weida Chen, Leandro Lopez Ramirez, Andrew Hsur, Lillian Su
- Playtest Notes:
    - Have the boost spawn more than once
    - Add obstacles for a challenge
    - Movement is smooth
    - Unsure what timer is for (will make sense once game is complete as it will show the player's racing time)
    - Make timer bigger
    - Make boost more approachable (looks like a danger the player would avoid)
    - Add a cooldown for the boost (a ticking box or clock in the top right that shows your remaining time with the boost)

### Activity 2
- Yes, a writer could add more dialogue without writing code because scriptable objects allow editors to simply work with assets and menus when adding new dialogue rather than adding new lines within the code itself.
- There is technically no limit to the number of dialogue nodes a writer could make, however eventually there will be too many to stay organized within the scope of the project/graph.
- The purpose of the regenerate nodes button is for Unity to be able to recognize new scripts as types that can be used as nodes within a graph, we need to regenerate because every new script isn't automatically translated into a node for visual scripting.

## Week 5
### Activity 1
Steps:
1. Respawn Speedboost after a certain time
    - Have new boost spawn 20 seconds after the first one (playtest in unity)
    - Make sure both boosts spawn at the correct time (check in game timer during playtest)

2. Player collects Speedboost powerup
    - Player uses state machine in order to transition into new state for both speedboosts (debug.log)
    - Speedboost destroys itself after comparing tags with player gameobject (check in unity playtest)

3. Player gets temoporarily faster after 10 seconds
    - Player speed variable goes to 10 after hitting speedboost (check inspector during playtest)
    - The speedboost only lasts 10 seconds (check in game timer during unity playtest)

### Activity 2
First I cleaned up some UI stuff by making the boost timer transparent, then I was able to make the power-up spawn twice at certain times! I did this by instantiating the speedboost prefab and having two seperate bools to spawn the prefab at two specifc times on the game timer (5 seconds and 20 seconds). After the second power up spawns the player was able to "collect" the power up and then they gained a temporary speed boost (speed veriable set to 10) for 10 seconds just like the first powerup does!

## Week 6
### Activity 1
- What is new in my currently playable build: I have added mouse lock after the player clicks anywhere on the start screen, obstacles which look like other racers that the player has to avoid, a life system for the player so that every time they hit an obstacle they go invincible for 5 seconds and lose one of their 3 lives, and finally once the player loses all 3 lives the player gameobject is destroyed and the player can no longer continue the game.
- [Itch link](https://porrasg.itch.io/gdim-33-milestone-2)
- Playtesting goals:
    - See if the obstacle's movements are smooth
    - Observe the level of difficulty the player has against the obstacles
    - Get the player's overall thoughts on the obstacles
- Playtesting Notes:
    - 

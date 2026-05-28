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
    - Change speed boost color to not confuse player (red heart means they think they will get an extra life, so maybe change to blue?)
    - Make it so that the player's collider turns off for 5 seconds after taking a hit (temporary invincibility) instead of turning off the prefabs collider
    - Add a game end screen to show player how long they lasted
    - Make sure speed boosts don't spawn on top of obstacles
    - Make UI bigger
    - Switch timer text and lives UI with the speedboost UI
    - Make the playaer blink/flash when they get hit
    - Put an image for the speedboost UI circle (maybe like speedboost arrows?)
    - Make obstacles faster for a harder challenge
    - Add audio

### Activity 2
1. The multiply setting of the blend node makes the resulting colors darker and less saturated than the input colors because the values are between 0-1 which makes them decimals, and when they are multiplied with each other they become smaller decimals which leads to darker and less saturated colors.
2. The resulting value will be more transparent because just like the color values, the decimals multiplied by each other will result in smaller numbers, so when that smaller number is inputed into the alpha value, the material becomes more transparent.
3. The shader gets the UV values from the Shiba texture, which means it is essentially getting a 2D map spread of the Shiba texture on the model.
4. I think it is pretty interesting that we can manipulate colors using math because I sort of understand how it works now and that makes me feel a bit better/more confident with working with shader graphs.

## Week 7
### Devlog Questions
1. The data for the Vertex Color node orginally came from the mesh itself! Most nodes under geometry already have data that comes from the original mesh.
2. The data between each vertex is interpolated in order to have specific areas of the shiba be a different color, like the white parts of the shiba's fur.
3. The reason the vertex color is less detailed is because the resolution of the model is less than the resolution that a texture can provided, so a texture can simply provide more detail due to the texture having a higher resolution. Vertex color could most likely be useful for blending colors, simple prototypes, and possible even performance because lower resolution would cause less stress on devices.
4. Based on the color, the vector normals of the shiba are pointing away from the Shiba while the light is pointing towards the Shiba which creates a negative and causes the Shiba to have reverse colors than it should have.
5. Another piece of vertex data we could debug using a shader could be UV mapping to see if there are any texture mapping issues on our model.
6. The reason there is an error on the back of the Shiba is because of the way the model is made, which causes those surface normals to be pointed in a direction where the lighting believes shadows should be in that area, making it look not smooth.
7. I think we set the blend mode to Additive for the fire effect to remove black completely from the texture in order to have it blend in well with whatever background you decide.

## Week 8
### Activity 1
- What is new in my Itch build is that I made the obstacles more difficult for the player to avoid and have made infinite speed boost spawn throughout the entire time the player is playing the game.
- [Itch Link](https://porrasg.itch.io/gdim-33-milestone-3)
- My playtesting goals are:
    - Checking if the obstacles provide enough difficulty for the player to still have fun but also be challenged as they play
    - Determine if the boost spawns should be more spread out (whether this regards time in between spawns or if the boost spawns should also be able to spawn on the top and bottom lanes)
- Playtesting Notes:
    - Fix returning to menu turning off colliders
    - No backspace to return (make it the r key instead)
    - Make the r key also the start button (so player can use the same hand they are already playing with)
    - Make it so that the mouse is locked immediately (player shouldn't have to use the mouse at all in the game, not even to start it)
    - Change speed boost increase amount to make it more manageable (current speed is too fast and doesn't benefit the player)
    - Make it so that car obstacles can double spawn (i.e. one car in the middle lane and one car in the bottom lane at the same time, so that the player doesn't just go up and down in the same motion the entire game)

### Activity 2 (2B)
1. The fraction node is used to animate the shine effect by only keeping the decimal portion of a value which creates a cycle effect that gives the shine its animation.
2. The shine texture for the ShinySprite shader needs to be black by default because the value of black is (0,0,0) which allows the sprite to be left untouched by black and then once value is added that adds light/color to the sprite.
3. The building texture we used in the ShaderGraph isn't applied to all of the sprites that use the ShinySprite shader because the texture inside the shadergraph is usually exposed/seen as a material property and not actually hardcoded into each sprite individually.
4. We multiply fraction(time * ShineSpeed) with the speed variable inside the fraction instead of outside, as in fraction(time)*speed, because fraction allows the value to wrap around into something between 0-1, so if we did 2 shinespeed we would get 1.5 which would then be 0.5 and therefore double the speed.

## Week 9
### Activity 1
Chosen Games: Blashpemous and Minecraft

Rendering System 1: Dashing speed effect (Blasphemous)
- We believe this effect involves the sprite of the character, so when the player is in the middle of a dash the sprite is duplicated and the sprites behind the first one are all changed to a blue-ish color to signify the "dash" effect.
- When the player presses the shift key, the animation plays and causes the sprites to duplicate with some sprites moving slower and changing color to be blue to act as the speed/fast moving effect.

Rendering System 2: Enchanted Items (Minecraft)
- We believe that this effect is linked to the object's material because it acts similar to the in class activity we did last week!
- When the player enchants an item in the enchantment table, the item then gets the enchantment effect which most likely changes the material or layer of the gameobject in order to "activate" the shadergraph for the object's material which gives it the enchanting effect.

Rendering System 3: Powdered Snow Effect (Minecraft)
- We think that this effect is tied to post-processing as it effects the player's screen once they begin to stand inside a powdered snow block.
- Once the player enters a powdered snow block, which would be activated by an on trigger enter collider, the post-processing effect is enabled and makes the powdered snow effect appear more and more on the player's screen the longer they stand in the powdered snow block.

### Activity 2

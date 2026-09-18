This is the NEA coursework for my computer science A-Level.

It is a zombie shooter game and a 1v1 game

Idea:
The whole program will be a game. This game will have 2 gamemodes in it that the players can pick from in the menu screen. The menu screen will let the user be able to change the gamemode and select a gamemode. The first gamemode will be a zombie shooter PVE game where you have to protect a monolith from zombies by collecting resources from around the map to build with and protect with whilst hordes of zombies try to storm the area and break the monolith. The second gamemode is a 1V1 PVP game where the players can battle it out amongst each other and see who stands victorious. There will be random drops around the map of blocks the players can collect and build with.

Menu Screen Details
The menu screen is the screen the players will be greeted with initially. This screen will default to show the zombie game card but the players can press a, d, left arrow and right arrow on the keyboard to change this. The menu screen has a slight cooldown between switching gamemodes so the gamemodes don't rapidly change too fast as that would be unusable. The menu screen has 2 possible backgrounds. The zombie game background and the PVP game background. These backgrounds will change as the user switches gamemodes. This will be done by keeping a track of what mode is selecting and then changing the self.background in the main Game class. I will then re-draw the background on the screen so it replaces the old one.


Zombie Game Details
The Zombies are going to be a simple design. They will calculate the angle at which they need to move to be able to reach the monolith and then move in the direction of the monolith using vector math. The zombies will be able to be stopped temporarily by walls, however the zombies will be able to break the walls down after hitting it 3 times. They will then continue to go towards the monolith and try to destroy it. 
The zombies all spawn with a random amount of health, movement speed and attack damage and will spawn in a random spot on the screen. The health will be a random integer between 1-200 meaning you could have a very tanky zombie that is hard to defeat. However, the more health the zombies have, the slower they will move. This is to add balance to the game and to allow the user to have more of a chance against the zombies. The attack damage will be randomly chosen separately from the health. This means you could have a very low health zombie that outputs a lot of damage or you could have a low damage high health zombie or anything in between. 
The spawning of the zombies will get more frequent as the game goes on meaning that at the start of the game, there will be less zombies to worry about but nearer the end of the game there will be more zombies to worry about. 
When a zombie naturally spawns in it will have a small chance to spawn reinforcements to help it. These reinforcements can’t spawn reinforcements from themselves however one zombie can spawn multiple reinforcements upon spawning depending on how long the game has been going on for.

The Monolith is a structure that lives in the middle of the map. It has 1000 health and it is the player’s goal to protect it. If a zombie collides with the monolith, the monolith will take a number of damage depending on the damage of the zombie.
When the monolith’s health is 0, the game ends and the players are given their score based on how long they lasted.
The monolith doesn’t regenerate health over time meaning if the players make a mistake at the beginning, it will stay with them for the rest of the game.

PVP Game Details
The PVP game will consist of a simple top down shooter that the players can use to train or practice against each other. Similarly it can be used to add a bit of fun competition to the game as the players get to test their skills against each other. 
The walls will act differently in this gamemode as the player will be able to shoot the walls and bullets won’t go through them. Each wall will be able to take 2 bullets before it dies. The walls will not drop any material on death
The goal of the game is to kill the other player by outskilling them and shooting them. 
Each payer has 100 health and each bullet does 10 damage to the player.

The Materials Will spawn throughout the map as the game goes on. The longer you stay in the game the less frequently the materials spawn. These materials are necessary for building walls and 1 material will be used up every time a wall is placed.
The materials will be shown for each player in their colour on the screen. This allows the players to keep track of the materials they have and whether they need to use them strategically.

The Walls are one of the defences against the zombies. The walls act as a temporary barrier between the players and zombies
The walls will be able to be placed in an invisible grid on the screen. 
When a wall is placed, it will consume 1 material from the player that placed it. It will also be able to be broken by players if it is clicked on again by the player after a placement cooldown. When broken, it will not return the materials back to the plate’s inventory.
The walls can also be broken by zombies. Each wall takes 3 seconds for a zombie to break and won’t drop material when broken.
The player’s bullets will be able to shoot through these walls allowing for slowly reducing the health of the zombies and making them more manageable to deal with.

# Credits:
This program is made entirely by me (Caro122) and uses NO AI and NO Code that other people have made. It is all original content made by me and only me :)

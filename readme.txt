Project Started 8-12-2023 by UngaBunga Studios

For the record, we lost our third 'A' during a company garage sale where it was not meant to be sold. Thus, we are not a Triple A game company, but double A. Hopefully the scoring system works like golf. (This is a joke btw...)

HOW TO RUN: Go to https://github.com/KazuraIusami/Wendigo/tree/main and look for the green button called " <> CODE ", then click "DOWNLOAD ZIP." Extract to where ever you want, open the folder and launch "index.html" For the best experience, press F11 to go full screen. Enjoy! Thank you for playing!

DEV NOTES :

() The whole folder labeled "OG" is just the pre-created thing I made, not very useful. Title, logo, and prompt made in krita

() 10/27/23 Good foundation built for the Aztech engine. 

-Created a class called "Entity" to use to link sprites and data to the creature. 
Entity( URL, xPOS, yPOS, TYPE, NAME) URL = Source for entity sprite xPOS & yPOS = data values for placement TYPE = (MONSTER/NPC/PLAYER) NAME = Both gives the creature a name and makes it the ID of the sprite, linking them together
 -Created a class for a dev toolkit as well as a keylogger than toggles its visibility using Escape

() 11/1/23 CONTROLS So far, I have a developers log that can be toggled on and off using "Escape." Inside of it are (as of writing this) two buttons. Spawn player, and Clear All Entities 
Dev Note: Recently got rid of a "spawn random enemy" button due to some errors with EntityList array. Work to be done soon The "Player" sprite that spawns when you click "Spawn Player" in the dev log can be clicked! In which case, it will follow the mouse cursor around the browser screen! 
Using the great art by https://www.instagram.com/guiigs.art/ for the sprite I have been calling "Wendigo"

() 11/3/23 Got directional movement set up to work with sprites, as well as working with facedDirection so I can have Idle animations 
-Press SHIFT to speed up movement of selected sprite 
-Click on sprite to "pin" it in the spot you click.
-Major developements to the Entity Class such as taking urlFolder and dynamically choosing the appropriate gif based on functional variables like facedDirection
-Dev Tools now has two rooms, one for a Monster to spawn in the middle of the screen (useful for testing combat mechanics) and one for NPCs which can be used for other tests

()11/5/23 Created a pretty good foundation for rooms. Basically, using the devlog you have to spawn player, then you can spawn any of the rooms listed. The first room and second room is still pretty much the same as it was in the last dev log, but now I have a fun little "prison" scenario. And with that, INTRODUCING
	CONVERSATION TREES!
	When spawning a room with the dev log, I am hand creating each entity within the room. Much like the source engine loads maps and such, the rooms are the maps. When creating the entity, I am giving it a "conversationTree" tag. Eventually, I will make this more complicated. It will HOPEFULLY resemble 
	the fallout engine conversation tree. I have done it before, I can do it again:)

()11/14/23 Conversation Trees are basically implemented, after LOTS of trial and error. To think I thought of it as simple. HOPEFULLY there arent any cracks in it. Basically my biggest problem was having it update too fast?
	So basically, when I spawn a room, I also specify what entities are in the room. If the name matches up to a conversation tree in the list, and the player interacts with it, it should just "work"
	Also got the second sprite, hopefully the main character I am calling "Eugene Galliga".
	Also, extra little dev note: Im not actually having the player interact with the walls. The walls are not entities, and so do not exist in the collision list. I am straight up saying "if the player is outside limits => dont"
		now, this isnt a BAD thing...its just important to keep this in mind through further iterations

() 11/18/23 
	-Screwing around a lot with events. Made room 5, which is the outside of a house (background crudely made by me), and when you walk into the door (EntityList[0].x & y are near door), the background changes and the same listeners from room 4 are applied. This is done by hand, as the rooms are all
	     engineered inside the dev log. The dev log is almost becoming a console, but that would complicate things
	-Getting death animations made for the characters, and also working on getting death listeners to work.
	-Inventory system is pretty much working, although I am still inexperienced with using it in my code first try.
	-WASD controls are also working pretty well, although there are still plenty of bugs. There are often times the character will  get stuck moving in a direction (I assume because of problems in the pressedKeys array)

	

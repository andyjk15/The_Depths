The Depths - inactive
===
2D Platformer - Written in HTML5, CSS & Javascript
---

You find yourself in the sewers of ______, the city of prosperity in our day and age.

Where everyone is Square.

Unfortunatly you were not born into a life of luck, quite the opposite, you have had a hard life as a circle. Bullied for being different, institutions discriminated against you, no one wanted to hire you.

As your life became a constant downfall you find yourself as the low of the low of society, you now reside in the sewers of the city.

Trying to scrape together a decent meal to survive, but you have not given up hope! You can still become something, discover yourself by exploring the vast underground networks of the sewers. Discover what you life really entails for you!

---

Feel free to customise the maps, all maps are easily customisable
Key is provided detailing what each property does

---

Maps
---

**Setup**
*Key:*
```
keys : [
            {id  : 0,colour: '#333', solid: 0},
            {id  : 1,colour: '#888', solid: 0},
            {id  : 2,colour: '#555',solid: 1,bounce: 0.30},
            {id  : 3,colour: 'rgba(121, 220, 242, 0.5)',friction: {x: 0.9,y: 0.9},gravity: {x: 0,y: 0.1},jump: 1,fore: 1},    //water
            {id  : 4,colour: '#777',jump: 1},                                         //elevator
            {id  : 5,colour: '#E373FA',solid: 1,bounce: 1.1},
            {id  : 6,colour: '#666',solid: 1,bounce: 0},
            {id  : 7,colour: '#67b2e1',solid: 0,script: 'change_colour'},
            {id  : 8,colour: '#FADF73',solid: 0,script: 'next_level'},
            {id  : 9,colour: '#b42d2d',solid: 0,script: 'death'},
            {id  : 10,colour: '#848484', friction: {x: 0.85, y: 0.85}},   //Sludge
            {id  : 11,colour: '#9F9',solid: 0,script: 'reverse'},         //Reverse block
            {id  : 12,colour: '#0FF',solid: 0,script: 'unlock'},          //Normal unlock
            {id  : 13,colour: '#0FF',solid: 0,script: 'lock'},            //Unlock a path and lock another
            {id  : 14,colour: '#888',solid: 0,script: 'reset_reverse'},   //Resets player movement

                //Secret unlocks (Lock)
            {id  : 15,colour: '#555',solid: 1},
            {id  : 16,colour: '#888',solid: 0},

                //Secret unlocks (normal unlock)
            {id  : 17,colour: '#333',solid: 0},
            {id  : 18,colour: '#333',solid: 1},
            {id  : 19,colour: '#555',solid: 1},
            {id  : 20,colour: '#FFF',solid: 0,script: 'point'},           //coins

                /*20 IDs used for shading/textures if i can figure it out*/
            {id  : 21,colour: '#585858', solid: 1, bounce: 0.30},    //Horz Pillar
            {id  : 22,colour: '#5A5A5A', solid: 1, bounce: 0.30},    //Brick
            {id  : 23,colour: '#5B5B5B', solid: 1, bounce: 0.30},    //Mossy Brick

            {id  : 99, colour: '#888', solid: 1}                      //Invisible block
            ],
```

*Map Example*
```
[2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2],
[2,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,2,0,0,0,2,2,2,2,2,2,2],
[2,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,2,0,0,0,2,1,1,1,1,1,2],
[2,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,2,0,0,0,2,1,1,1,1,1,2],
[2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,1,1,1,1,2,0,0,0,2,1,1,2,2,8,2],
[0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,2,1,1,1,1,2,0,0,0,2,1,1,2,2,2,2],
[0,0,0,0,0,0,0,0,2,2,2,2,2,2,2,2,2,2,2,2,1,1,1,1,2,0,0,0,2,1,1,2,2,2,2],
[0,0,0,0,0,0,0,0,2,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,2,0,0,0,2,1,1,2],
[0,0,0,0,0,0,0,0,2,1,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,1,1,2],
[0,0,0,0,0,0,0,0,2,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,2],
[0,0,0,0,0,0,0,0,2,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,2],
[0,0,0,0,0,0,0,0,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,5,2],
[0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,2,2,2]
```

---

Map Properties
---

Other properties that can be changed per map:
```
Gravity 		- In both X and Y
Velocity 		- In both X and Y
Movement Speed	- In left, right and jump
Player Position	- In X and Y
Player Colour	- In Hex value
Custom Scripts	- Run a set of functions to alter the map during or after completion
```
*Set as: (as Example)*
```
map.player.y 			= 6;
map.player.colour 		    = #FFFFFF
map.scripts.nextLevel           = 'CALL FUNCTION';
map.gravity.x           = 0.4;
map.vel_limit.y             = 2;
map.movement_speed.jump	            = 3;

etc...
```

---

**Plan to further expand this to a total of 100+ maps, addition tiles, more properties and images for each tile. Game will further develop with a story**

*Expansion from dissumulte/Clarity*

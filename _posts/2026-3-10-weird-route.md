# what's ACTUALLY required for the weird route anyway?
well, not nearly as much as people might think! to first get a decent understanding of how the game determines your current standing in the weird route lets take a look at the first few lines of the step code for the object that handles basiclly everything weird route related.\
![a screenshot containing lines 1-26 of gml_Object_obj_weirdroute_manipulator_Step_0](/images/post2/kris-wrong-way.png)
\
on line 8 we see  ```snd_play(snd_ominous);``` snd_ominous is the weird route jingle, in almost every situation hearing this(the audio file below) means that you're advancing the weird route.
<audio src="/audio/snd_ominous.wav" controls preload></audio>

looking at the line above it we see ```if (global.flag[915] == 0 && global.flag[531] == 6)```, \
```global.flag[915]``` is the main flag for determining what phase of the weird route you are currently in, if that flag's value is ```== 0``` then you have not started the weird route. ```global.flag[531]``` is the encounter flag for the virovirokun that can give noelle a tutoriel on how battles work, for our purposes we just need to know that if that flag's value is ```== 6``` it means we made noelle freeze it, simple right?\
if we havent done anything weird route related yet and we just made noelle freeze the tutoriel virovirokun then play the weird route jingle!
after playing the jingle the next line of code sets ```global.flag[915] = 1```. that offically starts us on phase 1 of the weird route.\
\
for preface, anything that looks like a screenshot of a room in this post is probobly taken straight out of undertalemodtool, with some collision stuff hidden of course, so things might look a tad odd. if you this -> ![duck](images/post2/obj_bg_givedepth.png) sprite randomly thats the object that handles depth perception, if you see this -> ![music note](/images/post2/obj_musicer_room.png) sprite randomly thats the object that handles the game's music, if you see this -> ![kris](image/post2/obj_mainchara.png) kris sprite randomly and its not explicited stated to be a mockup i made then its the spawner object for the party, and lastly if you randomly see berdly's frozen body -> ![frozen chicken](/images/post2/obj_weirdroute_manipulator.png) thats the object that handles the weird route.

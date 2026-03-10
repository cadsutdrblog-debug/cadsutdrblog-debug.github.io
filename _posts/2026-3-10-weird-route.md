# what's ACTUALLY required for the weird route anyway?
well, not nearly as much as people might think! to first get a decent understanding of how the game determines your current standing in the weird route lets take a look at the first few lines of the step code for the object that handles basiclly everything weird route related.\
![a screenshot containing lines 1-26 of gml_Object_obj_weirdroute_manipulator_Step_0](/images/post2/kris-wrong-way.png)
\
on line 8 we see  ```snd_play(snd_ominous);``` snd_ominous is the weird route jingle, in almost every situation hearing this(the audio file below) means that you're advancing the weird route.
<audio src="/audio/snd_ominous.wav" controls preload></audio>

looking at the line above it we see ```if (global.flag[915] == 0 && global.flag[531] == 6)```, \
```global.flag[915]``` is the main flag for determining what phase of the weird route you are currently in, if that flag's value is ```== 0``` then you have not started the weird route. ```global.flag[531]``` is the encounter flag for the virovirokun that can give noelle a tutoriel on how battles work, for our purposes we just need to know that if that flag's value is ```== 6``` it means we made noelle freeze it, simple right?\
if we havent done anything weird route related yet and we just made noelle freeze the tutoriel virovirokun then play the weird route jingle!

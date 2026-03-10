# what's ACTUALLY required for the weird route anyway?
well, not nearly as much as people might think! to first get a decent understanding of how the game determines your current standing in the weird route lets take a look at the first few lines of the step code for the object that handles basiclly everything weird route related.\
![a screenshot containing lines 1-26 of gml_Object_obj_weirdroute_manipulator_Step_0](/images/post2/kris-wrong-way.png)
\
on line 8 we see  ```snd_play(snd_ominous);``` snd_ominous is the weird route jingle, in almost every situation hearing this means that you're advancing the weird route, audio file below.
<audio src="/audio/snd_ominous.wav" controls preload></audio>

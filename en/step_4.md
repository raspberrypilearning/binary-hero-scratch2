## Play notes

Play notes when the keys are pressed.

--- task ---
Broadcast a 'note change' message whenever **any of the four keys** is pressed.
![sprite 1](images/1.png)
![blocks_1545217796_9512737](images/blocks_1545217796_9512737.png)
--- /task ---

--- task ---
Add code to the Stage to play a note when a combination of keys is pressed.

Your notes should start at middle C, which is note 60.

![blocks_1545217798_0432928](images/blocks_1545217798_0432928.png)

--- hints ---
--- hint ---
![1 sprite](images/stage.png)

When your stage `receives`{:class="blockevents"} the 'change note' broadcast, it should `stop all sounds`{:class="blocksound"} before `playing a note`{:class="blocksound"} based on the value of the`note`{:class="blockdata"} variable.

+ When the `note`{:class="blockdata"} variable is `1`{:class="blockdata"}, note 60 should play
+ When the `note`{:class="blockdata"} variable is `2`{:class="blockdata"}, note 61 should play
+ When the `note`{:class="blockdata"} variable is `3`{:class="blockdata"}, note 62 should play
+ etc...

--- /hint ---
--- hint ---
Here are the code blocks you need:
![stage](images/stage.png)
![blocks_1545217799_1373682](images/blocks_1545217799_1373682.png)
--- /hint ---
--- hint ---
This is what your code should look like:
![stage](images/stage.png)
![blocks_1545217800_3504224](images/blocks_1545217800_3504224.png)
--- /hint ---
--- /hints ---
--- /task ---

--- task ---
Test your code. Can you hear that a note is repeatedly played when you hold down a key?

--- no-print ---
<video width="400" controls>
  <source src="images/play-note-bug.mp4" type="video/mp4">
  Your browser does not support HTML5 video.
</video>
--- /no-print ---

--- /task ---

--- task ---
Add code so that the **all** the key sprites only play a note **once** when a key is held down?

![1 sprite](images/1.png)
![blocks_1545217801_429509](images/blocks_1545217801_429509.png)
--- /task ---

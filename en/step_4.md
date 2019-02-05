## Play notes

Play notes when the keys are pressed.

--- task ---
Broadcast a 'note change' message whenever **any of the four keys** is pressed.
![sprite 1](images/1.png)
```blocks
when flag clicked
forever
if < key [v v] pressed?> then
switch costume to [on v]
+broadcast [note change v]
else
switch costume to [off v]
end
```
--- /task ---

--- task ---
Add code to the Stage to play a note when a combination of keys is pressed.

Your notes should start at middle C, which is note 60.

```blocks
play note (60 v) for (1) beats
```

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
```blocks
play note (60 v) for (1) beats
when I receive [note change v]
() + ()
(note)
stop all sounds
```
--- /hint ---
--- hint ---
This is what your code should look like:
![stage](images/stage.png)
```blocks
when I receive [note change v]
stop all sounds
play note ((59) + (note)) for (1) beats
```
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
```blocks
when flag clicked
forever
if < key [v v] pressed?> then
switch costume to [on v]
broadcast [note change v]
+wait until <not <key [v v] pressed?>
else
switch costume to [off v]
end
```
--- /task ---

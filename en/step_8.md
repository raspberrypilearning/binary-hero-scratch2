## Keep a score

Improve your game by giving the player points for playing the correct note.

--- task ---
Create a new variable called `score`{:class="blockdata"}, and place it at the top of your Stage.

![Add a score](images/add-score.png)
--- /task ---

--- task ---
Add to `score`{:class="blockdata"} whenever the player plays the correct note at the correct time. Remember to set `score`{:class="blockdata"} to `0`{:class="blockdata"} at the start of the game.

--- hints ---
--- hint ---
`Before each clone is deleted`{:class="blockcontrol"}, it should check to see `if`{:class="blockcontrol"} the `note`{:class="blockdata"} is `equal to`{:class="blockoperators"} the `costume number`{:class="blocklooks"}, and in that case, the score should be `changed`{:class="blockdata"}.
--- /hint ---
--- hint ---
Here are the code blocks you need:
![note](images/note-sprite.png)
```blocks
[ ] = [ ]
(costume #)
(note)
change [score v] by (1)

if <> then
else
end
```
--- /hint ---
--- hint ---
This is what your code should look like:
![note](images/note-sprite.png)
```blocks
when I start as a clone
go to x: (20) y: (160)
show
glide (2) secs to x: (20) y:(-130)
+if <(note) = (costume #)> then
change [score v] by (1)
else
end
delete this clone
```
--- /hint ---
--- /hints ---
--- /task ---

--- task ---
Broadcast a message called 'correct' when the correct note is played.
![note](images/note-sprite.png)
```blocks
when I start as a clone
go to x: (20) y: (160)
show
glide (2) secs to x: (20) y:(-130)
if <(note) = (costume #)> then
change [score v] by (1)
+broadcast [correct v]
else
end
delete this clone
```
--- /task ---

--- task ---
![Correct stage background](images/correct-costume.png)

Add code to your Stage to briefly change the backdrop when the player plays the correct note. The project already contains a second backdrop for this.

![stage](images/stage.png)
```blocks
when flag clicked
switch backdrop to [normal v]

when I receive [correct v]
switch backdrop to [correct v]
wait (0.3) secs
switch backdrop to [normal v]
```
--- /task ---

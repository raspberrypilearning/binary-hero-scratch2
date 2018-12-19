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
![blocks_1545217812_7206063](images/blocks_1545217812_7206063.png)
--- /hint ---
--- hint ---
This is what your code should look like:
![note](images/note-sprite.png)
![blocks_1545217813_8342302](images/blocks_1545217813_8342302.png)
--- /hint ---
--- /hints ---
--- /task ---

--- task ---
Broadcast a message called 'correct' when the correct note is played.
![note](images/note-sprite.png)
![blocks_1545217814_9673197](images/blocks_1545217814_9673197.png)
--- /task ---

--- task ---
![Correct stage background](images/correct-costume.png)

Add code to your Stage to briefly change the backdrop when the player plays the correct note. The project already contains a second backdrop for this.

![stage](images/stage.png)
![blocks_1545217816_108](images/blocks_1545217816_108.png)
--- /task ---

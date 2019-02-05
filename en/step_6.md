## Store your song

At the moment, notes are removed from the lists after being played, so you're left with empty lists:

![Empty lists](images/empty-lists.png)

You're now going to add code to store songs in your project, so that you don't have to add to your lists each time.

![Add notes and times to lists](images/lists-add.png)

--- task ---
Make a new block called `load 'happy birthday'`{:class="blockmoreblocks"} that clears both the `notes`{:class="blockdata"} and `times`{:class="blockdata"} lists, and then adds the correct numbers back into both lists.
[[[generic-scratch-make-block]]]
--- hints ---
--- hint ---
The `load 'happy birthday'`{:class="blockmoreblocks"} block should `delete all`{:class="blockdata"} items from both the `notes`{:class="blockdata"} and `times`{:class="blockdata"} lists and then `add`{:class="blockdata"} the correct six numbers to the list they belong in, in the correct order.
--- /hint ---
--- hint ---
Here are the code blocks you need:
![notes-sprite](images/note-sprite.png)
```blocks
delete (all v) of [notes v]

define load 'happy birthday'

add [1] to [notes v]

delete (all v) of [times v]
```
--- /hint ---
--- hint ---
This is what your code should look like:
![notes-sprite](images/note-sprite.png)
```blocks
define load 'happy birthday'
delete (all v) of [notes v]
delete (all v) of [times v]
add [1] to [notes v]
add [5] to [times v]
add [1] to [notes v]
add [5.5] to [times v]
add [3] to [notes v]
add [6] to [times v]
add [1] to [notes v]
add [7] to [times v]
add [6] to [notes v]
add [8] to [times v]
add [5] to [notes v]
add [9] to [times v]
```
--- /hint ---
--- /hints ---
--- /task ---


--- task ---
Test your new block by running it at the start of your project.
![notes-sprite](images/note-sprite.png)
```blocks
when flag clicked
+load 'happy birthday' ::custom
hide
reset timer
```

Each of your lists should now contain six numbers.

![Lists of notes and times](images/load-list-test.png)
--- /task ---

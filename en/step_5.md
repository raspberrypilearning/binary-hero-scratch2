## Scrolling notes

You need to make notes scroll down the Stage so that the player knows which keys to press and when to press them.

--- task ---
Create two lists called `notes`{:class="blockdata"} and `times`{:class="blockdata"}.

[[[generic-scratch-make-list]]]
--- /task ---

--- task ---
Add the following numbers to your `notes`{:class="blockdata"} and `times`{:class="blockdata"} lists. Note: make sure to **add these exact numbers in the right order**.

![Add notes and times to lists](images/lists-add.png)
--- /task ---

Here's how songs are stored in your game:

+ The `notes`{:class="blockdata"} list stores the notes of the song (from 1 to 15), in order
+ The `times`{:class="blockdata"} list stores the times when the notes should be played in the song

![Explaining lists](images/lists-explain.png)

So with the two new lists:

+ Note 1 (middle C) should be played at 5 seconds
+ Note 1 should be played again at 5.5 seconds
+ Note 3 should be played at 6 seconds
+ etc...

--- task ---
Right-click on the 'note' sprite, and click on **show**.

![Show the bar sprite](images/note-show.png)

Then click on **Costumes**.

![Bar sprite costumes](images/note-costumes.png)
--- /task ---

You should see that the 'note' sprite has 15 different costume, one for each different note from 1 to 15.

--- task ---
Add code to create a 'note' sprite clone for every note stored in `notes`{:class="blockdata"}. Each clone should be created at the correct time stored in `times`{:class="blockdata"}. Each clone should be created two seconds before its note needs to be played. This gives the clone two seconds to move down the screen. You'll create the code to move your clones in a little bit!

![Testing clones](images/clones-test.png)

--- hints ---
--- hint ---
![note](images/note-sprite.png)
When the `flag is clicked`{:class="blockevents"}, the 'note' sprite should `hide`{:class="blocklooks"}, and the `timer`{:class="blockdata"} should be `reset`{:class="blockdata"}.

The script should then `wait until`{:class="blockcontrol"} the value of `timer`{:class="blockdata"} is `greater than`{:class="blockoperators"} the next note to be played, which will be the `time`{:class="blockdata"} at the `start of the list`{:class="blockdata"} (`minus 2 seconds`{:class="blockoperators"}).

The costume for the 'note' sprite should then be set to the next `note`{:class="blockdata"} to be played (the `note`{:class="blockdata"} at the start of the list), before a `clone`{:class="blockevents"} of the 'note' sprite is created.

The items at the start of the `notes`{:class="blockdata"} and `times`{:class="blockdata"} lists should then be `deleted`{:class="blockdata"}, and the entire process should be `repeated until`{:class="blockcontrol"} there are no items left in the `notes`{:class="blockdata"} list.

--- /hint ---
--- hint ---
Here are the code blocks you need:
![note](images/note-sprite.png)
![blocks_1545217802_557496](images/blocks_1545217802_557496.png)

--- /hint ---
--- hint ---
This is what your code should look like:
![note](images/note-sprite.png)
![blocks_1545217803_7552915](images/blocks_1545217803_7552915.png)
--- /hint ---
--- /hints ---
--- /task ---

When you test your code now, nothing seems to happen, because the 'note' sprite is hidden. If you show (or don't hide) the sprite, then you should see clones being created on top of each other.

--- task ---
Add code to make each 'note' clone glide from the top to the bottom of the Stage before being deleted.
![note](images/note-sprite.png)
![blocks_1545217804_9580748](images/blocks_1545217804_9580748.png)
--- /task ---

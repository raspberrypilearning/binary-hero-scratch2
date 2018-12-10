### Binary numbers

You will use different combinations of pressing the four keys to play different notes. Each of the keys is either on (pressed) or off (not pressed). This means that you can think of each combination of keys as a __binary number__.

Moving from right to left the keys double in value: `1`, `2`, `4`, and `8`. By adding up the numbers above the keys that are pressed, you can work out the value of the note.

![Note value examples](images/note-values.png)

There are 2<sup>4</sup> = __16 combinations__ of pressing the four keys. This means that you can play 15 different notes, as `0` will mean that no note plays.

--- task ---
Create a new variable called `note`{:class="blockdata"}, and drag it next to the four note sprites.

![Note variable](images/note-create.png)

[[[generic-scratch-add-variable]]]


--- /task ---

`note`{:class="blockdata"} will store the value of the note that should be played.

--- task ---
Add code to the Stage to use the combination of pressed keys to calculate the value of `note`{:class="blockdata"}.

For example, when `c` and `v` are pressed, the value of `note`{:class="blockdata"} should be `3`.

![Testing the note variable](images/note-test.png)

--- hints ---
--- hint ---
![stage](images/stage.png)
When the `flag is clicked`{:class="blockevents"}, the `note`{:class="blockdata"} variable should be `set`{:class="blockdata"} to `0`{:class="blockdata"}.

+ `if`{:class="blockcontrol"} the `v key is pressed`{:class="blocksensing"}, the `note`{:class="blockdata"} should be `changed by 1`{:class="blockdata"}
+ `if`{:class="blockcontrol"} the `c key is pressed`{:class="blocksensing"}, the `note`{:class="blockdata"} should be `changed by 2`{:class="blockdata"}
+ `if`{:class="blockcontrol"} the `x key is pressed`{:class="blocksensing"}, the `note`{:class="blockdata"} should be `changed by 4`{:class="blockdata"}
+ `if`{:class="blockcontrol"} the `z key is pressed`{:class="blocksensing"}, the `note`{:class="blockdata"} should be `changed by 8`{:class="blockdata"}

All of this code should be repeated `forever`{:class="blockcontrol"}.
--- /hint ---
--- hint ---
Here are the code blocks you need, and you have to add some of them more than once:
![stage](images/stage.png)
```blocks
forever
end
if < > then
end
key [ v] pressed?

change [note v] by ( )

set [note v] to [ ]

when flag clicked
```
--- /hint ---
--- hint ---
This is what your code should look like:
![stage](images/stage.png)
```blocks
when flag clicked
forever
set [note v] to [0]
if <key [v v] pressed? > then
change [note v] by (1)
end
if <key [c v] pressed? > then
change [note v] by (2)
end
if <key [x v] pressed? > then
change [note v] by (4)
end
if <key [z v] pressed? > then
change [note v] by (8)
end
end
```
--- /hint ---
--- /hints ---
--- /task ---

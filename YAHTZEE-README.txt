=====================
CMPU-101, Spring 2016
README for Yahtzee
Travers Parsons-Grayson and
Grace Kirkpatrick
5/15/2016
=====================

To play Yahtzee download "yahtzee.txt" and "text-based-yahtzee.txt"
and place them in the same directory.

Then CD into that directory you have created.

Then type:  (load "text-based-yahtzee.txt") 

And follow the directions printed in the Interactions Window.

======================
DETAILED INSTRUCTIONS (if needed)
======================
To start playing Text-Based Yahtzee type the following in the interactions window:

      (define y (new-game))

Then: (show-yahtzee y)

=================================
To save or un-save a die: (toggle-save-die! <game> <list of die indexes>)
EX: Dice: (1 4 5 6 2) Index: 0, 1, 2, 3, 4    0: 1  1: 4  2: 5  3: 6  4: 2
Save the first and second die (1 4): (toggle-save-die! y '(0 1)) ==> saved-dice: (#t #t #f #f #f)
Un-Save the first and second die (1 4): (toggle-save-die! y '(0 1)) ==> saved-dice: (#f #f #f #f #f)
=================================
To roll the dice: (roll-em! <game>)
=================================
To score: (score! <game>  <index of category> )
The index of each category is shown under 'Potential Scores'
To score in three-of-a-kind: (score! y 7)
---------------------------------
For categories of index > 6 you may also score the following way:
To score in three-of-a-kind: (score! y *three-of-a-kind*)
	 in four-of-a-kind: (score! y *four-of-a-kind*)
	 in full-house : (score! y *full-house)
	 in small-straight: (score! y *small-straight*)
	 in large-straight: (score! y *large-straight*)
	 in chance: (score! y *chance*)
	 in yahtzee: (score! y *yahtzee*)
==================================
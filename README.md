# T9_Keypad
##**A) Required input and output expected**

###Input:
The digits from the keypad which forms the required word.
>Note: No letters are mapped to 1, *, 0 and #
according to the convention followed on all the
phones.

###Output:
List of all the words corresponding to the digit
pattern.
If no word matches the pattern, no word is shown in the
list.

![Screenshot of digit pattern 4663](https://github.com/kaustubhkhare/T9_Keypad/blob/master/screenshots/t9_dict_new.png)

##B) Design Model and Implementation

The key functioning here is done by a modified TRIE which is a tree data structure. It involves 2 processes:
###1. Building the trie:
Each node in the trie points to 10 nodes(having digits and an array of words) or null if its empty. To put a new word, convert the word into its	corresponding digit pattern and according	to it traverse through the trie from node to node via the pointers. If a particular node doesn't exist (ie. the pointer is null), add	that node. At the last digit node, put the word associated with the pattern in the array of words of that node.
###2. Retrieving words from the pattern:
To retrieve the words associated with a particular pattern, traverse through the trie via pointers and print the words in the array of the last node of the pattern. If the array is empty, no word is associated with that pattern.

![Tree built for 4663 and 2564](https://github.com/kaustubhkhare/T9_Keypad/blob/master/screenshots/tree_build.jpg)

##C) Applications

* Text messaging
* Searching a contact


##D) Limitations

Doesn't handle special characters like '-', ',', '.', '!', '?' etc.


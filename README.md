*This is the final version of word occurrence counter. Program using HashMap and each bucket is head of a BST.

-Logic of storing and searching the words:                                                 
*For each word, a node called word is being created and this nodes are stored in hash table, an array of node pointers. Later on when searching a word is needed, hash function locates the index of our word node. However if more than one word was placed on some position on hash table, searching algorithm wanders around the BST with recursive function to locate exact address of the word. Time complexity is almost O(n).

-Definition of a word:                                         
*This program does not only read words but also cleans them following to some rules. Here is program's rules for counting a string as a word; -> Any contiguous block of alphabetic characters (letters from “a” to “z”, both upper and lower case) which includes at most one single quotation mark between these letters is a word. According to this definition the following sentence in an article:"if we don't have local agreements settled by Thursday", has the words: “if”, “we”, “don’t”, “have”, “local”, “agreements”, “settled”, “by”, “Thursday” and if there are any symbol other than alphabetic character at the beginning/end, they must be removed. Also note that, every upper letters must be turned into lower. That means the string "the" and "The" are same.

-Tests *Program counts 2.078.530 words from a text file with 30 million letters in it and finds most used 10 words in;                 
-> 0.40 seconds on M1 chip.                          
-> 0.70 seconds on intel core 5i.

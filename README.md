# Breaking Caesar cipher

In cryptography, a Caesar cipher is one of the simplest and most widely known encryption techniques. It is a type of substitution cipher in which each letter in the plaintext is replaced by a letter some fixed number of positions down the alphabet.

Please refer to the full [description of the Caesar cipher on wikipedia](https://en.wikipedia.org/wiki/Caesar_cipher) for more information. You are allowed to use Internet for help (e.g. to consult StackOverflow or documentation).

# Specifications

For this exercise, we will consider the following simple alphabet: `abcdefghijklmnopqrstuvwxyz ,.!?`. Note the punctation marks which are part of the alphabet. This string can be found in `alphabet.txt`. You may assume that all plaintexts and ciphertexts provided are composed solely of symbols from this alphabet.

We will consider positive shifts to shift left (i.e. a shift of 3 turns `a` into `d`) and negative shifts to shift right (i.e. a shift of -3 turns `d` into `a`). 

The shift loops around the alphabet. For example a shift of 3 turns `y` to `,` and a shift of -1 turns `a` into `?`.

# Evaluation criteria

Your code should:
- work according to spec
- be clear (appropriate variable names, short functions, etc)
- be elegant when it does not impair readability
- rely on short functions with descriptive names and well-chosen arguments


# Question 1

Decrypt the ciphertext found in `q1_ciphertext.txt`. A Caesar cipher with a shift of (positive) 5 was used to encrypt sentence. You should obtain the sentence found in `q1_plaintext.txt`.

# Question 2

The objective of this question is to write a function that can "break" a Caesar's cypher by frequency analysis.

You are given the frequency distribution of letters in the english language in the tab-separated file `letter_distribution_english.txt`. 
 

We will take a probabalistic approach and define the most likely shift as the shift which maximises `P(shift | shifted sentence)`.

Using Bayes rule, we know that `P(shift | shifted sentence)` is proportional to `P(shifted sentence | shift) * P(shift)`. Assuming all shifts are equally likely, the most likely shift is therefore the one maximising `P(shifted sentence | shift)`

Assuming all letters in the shifted sentence are drawn for the letter distribution independently, we can treat the shifted sentence as a collection of independent letters, each having probability `frequency[letter]`.

- Express `P(shifted sentence | shift)` using the letters in the sentence and their frequencies in the english language
- Write a function that finds the most likely shift for a given sentence, given the english language frequency distribution. You may need to make extra assumption.
- Find the most likely shift for the sentence found in `q2_ciphertext.txt` and decrypt it.

# Question 3

Decrypt the sentences found in `q3_crypted.txt`. There is one sentence per line and each sentence has been encrypted using a different shift.

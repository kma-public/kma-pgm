# Breaking Caesar cipher

In cryptography, a Caesar cipher is one of the simplest and most widely known encryption techniques. It is a type of substitution cipher in which each letter in the plaintext is replaced by a letter some fixed number of positions down the alphabet.

Please refer to the full [description of the Caesar cipher on wikipedia](https://en.wikipedia.org/wiki/Caesar_cipher) for more information. You are allowed to use Internet for help (e.g. to consult StackOverflow or documentation).

# Specifications

For this exercise, we will consider the following simple alphabet: `abcdefghijklmnopqrstuvwxyz ,.!?`. Note the punctation marks which are part of the alphabet. This string can be found in `alphabet.txt`. You may assume that all plaintexts and ciphertexts provided are composed solely of symbols from this alphabet.

We will consider positive shifts to shift left (i.e. a shift of 3 turns `a` into `d`) and negative shifts to shift right (i.e. a shift of -3 turns `d` into `a`). 

The shift loops around the alphabet. For example a shift of 3 turns `y` to `a` and a shift of -1 turns `a` into `z`.

# Evaluation criteria

Your code should:
- work according to spec
- be clear (appropriate variable names, short functions, etc)
- be elegant when it does not impair readability
- rely on short functions with descriptive names and arguments


# Question 1

Decrypt the ciphertext found in `q1_ciphertext.txt`. A Caesar cipher with a shift of 5 was used. You should obtain the sentence found in `q1_plaintext.txt`.

# Question 2

You are given the frequency distribution of letters in the english language in the tab-separated file `letter_distribution_english.txt`. 

Find the most likely shift for the sentence found in `q2_ciphertext.txt`, assuming that the plaintext is an english sentence. What are the assumptions of your language model?

_Hint:_ the most likely shift corresponds to the most likely decrypted text under a simple language model using the letter distribution.

# Question 3

Decrypt the sentences found in `q3_crypted.txt`. There is one sentence per line and each sentence has been encrypted using a different shift.

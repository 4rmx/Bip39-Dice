# Bip39 Offline Mnemonic Generator

![outline](images/rolls.png)



[![YouTube Channel Views](https://img.shields.io/youtube/channel/views/UCz5BOU9J9pB_O0B8-rDjCWQ?label=YouTube&style=social)](https://www.youtube.com/channel/UCz5BOU9J9pB_O0B8-rDjCWQ)

## Manually Generate a Bitcoin Wallet using Dice

This is a pdf + code containing the instructions and the BIP39 list (English in pdf and English and Japanese in code) for offline generation a full BIP39 24 word seed (the words' lists are taken from https://github.com/bitcoin/bips/blob/master/bip-0039/bip-0039-wordlists.md). The first 23 words are generated using paper and dice, and the 24th word is generated using the script `24thword.py`.



## Step 1: First 23 words

Print the pdf,  grab a pen, a pocket calculator (optional) and some dice and generate the first 23 words. 

## Step 2: The 24th word

To determine the final 24th word, on an **OFFLINE** machine, edit `rolls.txt` and replace the words with the 23 that you chose using dice. Then run:

`python3 24thword.py`

You will be given a list of 8 valid 24th words. Pick one (eg by rolling 3 dice using and using the method above to get a number between 1 and 8), write your chosen word with the other 23. This is a valid wallet seed, and you can use it with [Electrum](http://electrum.org) or some other wallet application.

If you don't have an airgapped (permanently offline) machine, you could use [seedsigner](https://github.com/SeedSigner/seedsigner).

For more information you may check: https://learnmeabitcoin.com/technical/mnemonic

## Step 3: Receiving/ Sending

To receive money to the wallet. You'll need an address (derived from your xpub). To send, you'll need your private key. The keys you'll need to do both of these things can be derived using an offline version of the page https://iancoleman.io/bip39/ 

## Step 4: Storing your seed

The code that you generated needs to be stored in a secure way, here's  a video of one (of many) possible methods:

[![Electro Etching](http://img.youtube.com/vi/RVYHCVpeyEA/0.jpg)](http://www.youtube.com/watch?v=RVYHCVpeyEA "Video Title")


## Nothing is Original

Code for 24th word was based on [avsync/bip39chk](https://github.com/avsync/bip39chk)

## License

GPL 3.0

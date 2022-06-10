# CoinFlip

Hi There,

CoinFlip is a smart contract built on top of solidity language which allow users of the contract to place bets on the outcome of a coin flip i.e. Heads or Tails.
While placing bets, they will be entering the amount they would like to bet with and the bet itself. In case they win the bet, their balance would be doubled with the amount they chose to bet with after initial deduction of balance with the amount and if they lose the bet, their balance would be simply deducted by the amount of the bet.
To generate outcome result of the bet, I have used Harmony's Verifiable Random Function whose randomness is highly unbiased, as claimed by the Harmony team ensuring the trust factor, something blockchain is all about.

I have tested this contract on Harmony Testnet using their token ONE, the details of which are mentioned below:

The smart contract was deployed on this address : 0x0965cab25605ab54a5f55d282dcd16d1d94846e5

The details of all the transactions can be fetched from this link : https://explorer.pops.one/address/0x0965cab25605ab54a5f55d282dcd16d1d94846e5
To give a brief about it, I have used 4 Harmony Testnet accounts to place the bet with the amount and the bet I want to place in the function placeBet().
After which I am calling the rewardBets() function which rewards the winners of the bet with double the amount which they used to bet.
The accounts which were used for the transaction are : 
1. 0xdcdbb56420e76f11389742d4bf81e46f0d7fb7c1 :  placeBet(uint256: 25, uint8: 1)
2. 0xb3b87255a8e15922c2e83ec5f04fe57520b9b3bf : placeBet(uint256: 50, uint8: 0)
3. 0x5a2c49d3273e19e51cd09c02105aebbd1b107361 : placeBet(uint256: 76, uint8: 1)
4. 0x9e44b29875752ad68bf604f4a39b726b83409a84 : placeBet(uint256: 82, uint8: 0)

![image](https://user-images.githubusercontent.com/75273759/172987261-5bf460a6-2f3f-4dc6-b9eb-5c13b411e5a1.png)

This is the log content came out of remix directing those who placed bets as 0 (heads) won and were rewarded, confirming the event is getting correctly emitted.

I really hope you like it!!

Thankyou.


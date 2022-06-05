# CoinFlip

Hi There,

CoinFlip is a smart contract built on top of solidity language which allow users of the contract to place bets on the outcome of a coin flip i.e. Heads or Tails.
While placing bets, they will be entering the amount they would like to bet with and the bet itself. In case they win the bet, their balance would be doubled with the amount they chose to bet with after initial deduction of balance with the amount and if they lose the bet, their balance would be simply deducted by the amount of the bet.
To generate outcome result of the bet, I have used Harmony's Verifiable Random Function whose randomness is highly unbiased, as claimed by the Harmony team ensuring the trust factor, something blockchain is all about.

I have tested this contract on Harmony Testnet using their token ONE, the details of which are mentioned below:

The smart contract was deployed on this address : one1fsu4uqz2ylguch8kcjfy0zwg6vmwxpwea4e5ry

The details of all the transactions can be fetched from this link : https://explorer.pops.one/address/0x4c395e004a27d1cc5cf6c4924789c8d336e305d9
To give a brief about it, I have used 3 Harmony Testnet accounts to place the bet with the amount and the bet I want to place in the function placeBet().
After which I am calling the rewardBets() function which rewards the winners of the bet with double the amount which they used to bet.
The accounts which were used for the transaction are : 
1. one1tgkyn5e88cv728xsnsppqkhth5d3qumpzm7exv :  placeBet(uint256: 88, uint8: 0)
2. one1kwu8y4dgu9vj9shg8mzlqnl9w5stnval9emeyd : placeBet(uint256: 94, uint8: 1)
3. one1mndm2epquah3zwyhgt2tlq0yduxhld7p2vdyys : placeBet(uint256: 24, uint8: 0)

![image](https://user-images.githubusercontent.com/75273759/172034997-71c0fe06-7534-4442-85f2-c79868427838.png)

This is the log content came out of remix directing those who placed bets as 0 (heads) won and were rewarded.


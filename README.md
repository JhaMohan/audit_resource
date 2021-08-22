In this stream, I will do security reviews of ethereum smart contracts and share my approach to auditing ethereum applications. 

Here are some brief notes that I’ll use as talking points on the stream. A detailed blog post on https://mudit.blog/ will come later.

Resources
https://github.com/ethereumbook/ethereumbook
https://cryptozombies.io/
https://solidity-by-example.org/
https://docs.soliditylang.org/
https://ethereum.org/en/learn/
https://ethernaut.openzeppelin.com/

Auditing Approach
- Read about the project to get an idea of what the smart contracts are meant to do. Glance over all the resources about the project that were made available to you.
- Glance over the smart contracts to get an idea of the smart contracts architecture. Tools like Surya can come in handy.
- Create a threat model and make a list of theoretical attack vectors including all common pitfalls and past exploit techniques.
- Look at places that can do value exchange. Especially functions like transfer, transferFrom, send, call, delegatecall, and selfdestruct. Walk backward from them to ensure they are secured properly.
- Do a line-by-line review of the contracts.
- Do another review from the perspective of every actor in your threat model.
- Run tools like Slither and review their output.
- Glance over the test cases and code coverage.

Contracts under review
NOTE: I am only going to spend a few minutes on every contract. I am not affiliated with any of these projects. This is only for educational purposes, do not derive any conclusions from this.

BridgeDeposit - https://etherscan.io/address/0x324C7ec7fb2Bc61646aC2f22f6D06AB29B6c87a3#code
OptionsLM - https://gist.github.com/andrecronje/6c3da8b294488001adeda528f70bc301
Paywall - https://github.com/jierlich/paywall/blob/main/contracts/Paywall.sol
Timelock - https://github.com/yieldprotocol/yield-utils-v2/blob/tweak/boring-timelock/contracts/utils/Timelock.sol
UBIBurner - https://kovan.etherscan.io/address/0x595767572b565Bb289dBE313AdBEF3Bfa3e680c3#code
YieldTokenCompounding - https://github.com/rahul-kothari/hack-money-ape/blob/main/contracts/YieldTokenCompounding.sol

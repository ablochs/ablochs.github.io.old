---
layout: post
title:  "Etherum Notes"
date:   2015-03-23
categories: 
tags: [daaps, distributed applications, etherum]

---

{% highlight python %}
contract metaCoin { 
    mapping (address => uint) balances;
    function metaCoin() {
        balances[msg.sender] = 10000;
    }
    function sendCoin(address receiver, uint amount) returns(bool sufficient) {
        if (balances[msg.sender] < amount) return false;
        balances[msg.sender] -= amount;
        balances[receiver] += amount;
        return true;
    }
}

var metaCoin = web3.eth.contractFromAbi([{"constant":false,"inputs":[{"name":"receiver","type":"address"},{"name":"amount","type":"uint256"}],"name":"sendCoin","outputs":[{"name":"sufficient","type":"bool"}],"type":"function"}]);
contract metaCoin{function sendCoin(address receiver,uint256 amount)returns(bool sufficient){}}
90b98a11… :sendCoin
{% endhighlight %}


## Concepts

### Gas
- Gas comes into play when you try to make a contract do something.
- In order to execute this function, the contract will need gas, just like your car does. So, as part of the function call, you specify how much ‘gas’ you want to send to the contract, and how much you’re willing to pay for that gas (priced in ether, Ethereum’s fuel and unit of account).


## Coding languages
- Solidity is statically typed and will perform type checking at compile time. 


## Applcation ideas
- [http://www.quora.com/How-can-I-make-money-with-Ethereum](http://www.quora.com/How-can-I-make-money-with-Ethereum)
- [Ethereum, equality, and profits - How will decentralized apps make money?](http://www.reddit.com/r/ethereum/comments/2g6l1z/ethereum_equality_and_profits_how_will/)
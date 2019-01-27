# Orientum-Plus-Token

The ORT Plus Token contract is used for Orientum Plus an ERC-20 token deployed to the Ethereum blockchain initally on 1st December 2018.

After consultation it was decided to extend the standard ERC20 token protocol to incorporate optional wallet identification material. A second contract was deployed with a proprietory R-seb protcol on 27th January 2019.

The token details are as follows :

## Orientum Plus

Description       | Value
----------------- | -------------
Token Name        | Orientum Plus
Token Symbol      | ORT+
Total Supply      | 40,000,000,000
Decimal places    | 18
Ethereum Address  | 0xe02a471b2778b2d3a220e1ff82a0f8184fb73504

The token contract is based on standard contracts from https://openzeppelin.org

To give a little background:

ERC-20 is one of several technical standard used for token smart contracts on the Ethereum blockchain.

ERC stands for "Ethereum Request for Comment", and 20 is the number that was assigned to this request some time ago.

At this point the clear majority of tokens issued on the Ethereum blockchain are ERC-20 compliant. Well over 100,000 are presently issued.

The standard defines a common list of rules for Ethereum tokens to follow within the larger Ethereum ecosystem, allowing developers to accurately predict interaction between tokens, including how tokens are transferred between addresses and how data within each token is accessed.

Function required by ERC-20 and implemented within this contract are as follows:

#### totalSupply() - public view returns (uint256 totalSupply)

Get the total token supply

#### balanceOf(address _owner) - public view returns (uint256 balance)

Get the account balance of another account with address _owner

#### transfer(address _to, uint256 _value) - public returns (bool success)

Send _value amount of tokens to address _to

#### transferFrom(address _from, address _to, uint256 _value) - public returns (bool success)

Send _value amount of tokens from address _from to address _to

#### approve(address _spender, uint256 _value) - public returns (bool success)

Allow _spender to withdraw from account, multiple times, up to the _value amount.

If this function is called again it overwrites the current allowance with _value

#### allowance(address _owner, address _spender) - public view returns (uint256 remaining)

Returns the amount which _spender is still allowed to withdraw from _owner

Additional R-seb functionality is provided by the following functions

#### nameOf (address _owner)

Get Rseb info name of account with address _owner

#### telOf (address _owner)

Get Rseb telephone data of account with address _owner

#### emailOf (address _owner)

Get Rseb email data of account with address _owner

#### urlOf (address _owner)

Get Rseb url data of account with address _owner

#### infoOf (address _owner)

Get Rseb info data of account with address _owner

#### setRsebData (string memory _name, string memory _tel, string memory _mail, string memory _url, string memory _info)

Set all Rseb data of account

#### seeRsebData (address _owner)

Get all Rseb data of account with address _owner

# FirstMetaAssignment
First Project Assignment of creating tokens given by the Metacrafters Team . 

# Description
This above program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has public variables that store details about coin , a mapping ofaddress is also done in the program as per the requirement of project . There are two functions available in the program "mint" and "burn" functions , both of them have two paramets of address and value inside them .

# Getting Started
Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

# Code
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
    string public tokenName = "Meta";
    string public tokenAbbrv = "SSB";
    uint public  totalSupply = 0;
     
    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint (address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // burn function
    function burn (address _address, uint _value) public {
        if(balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile myToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar.

After deployment you can interact with code

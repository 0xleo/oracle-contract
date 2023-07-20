// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract Oracle {
    address public owner;
    uint public data;

    event DataUpdated(uint newData);

    constructor() {
        owner = msg.sender;
    }

    modifier onlyOwner() {
        require(msg.sender == owner, "Only the owner can call this function.");
        _;
    }

    function updateData(uint newData) external onlyOwner {
        data = newData;
        emit DataUpdated(newData);
    }

    function getData() external view returns (uint) {
        return data;
    }
}

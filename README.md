# SimpleStringReverse.sol
Remix - Deploy Contract On Base Network SimpleStringReverse.sol
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract SimpleStringReverse {
    function reverse(string memory s) public pure returns (string memory) {
        bytes memory b = bytes(s);
        bytes memory r = new bytes(b.length);
        for (uint i = 0; i < b.length; i++) {
            r[i] = b[b.length - 1 - i];
        }
        return string(r);
    }
}

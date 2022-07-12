# Audits


[![My GitHub Stats](https://github-readme-stats-one-bice.vercel.app/api?username=Keen-Sheen&show_icons=true&theme=dark&role=OWNER,ORGANIZATION_MEMBER,COLLABORATOR&include_all_commits=true&count_private=true)](https://github.com/billy1624#gh-dark-mode-only)

![An Image of Smart Contract Auditing](smart-contract-audit-cost.png)



# A collective ownership platform for NFTs on Ethereum

Below is a "Call Graph" of the NFT. This call graph is showing the Transfer functions within the `TransferRefernce.sol` file. 

* The `ERC20Transfer` has an internal call that points to an abstract `IERC20` contract
* `ERC721 TransferFrom` has an internal call that points to an abstract `IERC721` contract
* `ERC1155TransferFrom` & `ERC1155BatchTransferFrom` points to an abstract `IERC1155` contract.


![An Image of Audit Graph](TransferRefrences_Graph.svg)


## A call to a user-supplied addres is executed

  * An external message call to an address specified by the `caller` is executed. Note that the callee account might contain arbitrary code and could re-enter any function within this contract. Reentering the contract in an intermediate state may lead to unexpected behaviour. 



https://github.com/Keen-Sheen/Audits/blob/d94043fbc734e0e8bddd29b6888587ec00224954/src/interfaces/IERC20.sol#L41

# Audits


[![My GitHub Stats](https://github-readme-stats-one-bice.vercel.app/api?username=Keen-Sheen&show_icons=true&theme=dark&role=OWNER,ORGANIZATION_MEMBER,COLLABORATOR&include_all_commits=true&count_private=true)](https://github.com/billy1624#gh-dark-mode-only)

![An Image of Smart Contract Auditing](smart-contract-audit-cost.png)



# A collective ownership platform for NFTs on Ethereum

Below is a "Call Graph" of the NFT. This call graph is showing the Transfer functions within the `TransferRefernce.sol` file. 

* The `ERC20Transfer` has an internal call that points to an abstract `IERC20` contract
* `ERC721 TransferFrom` has an internal call that points to an abstract `IERC721` contract
* `ERC1155TransferFrom` & `ERC1155BatchTransferFrom` points to `IERC1155`



![An Image of Audit Graph](TransferRefrences_Graph.svg)

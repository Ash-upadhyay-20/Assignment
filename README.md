# Managing NFTs in JavaScript

This JavaScript script demonstrates a simple implementation of managing Non-Fungible Tokens (NFTs) using JavaScript objects and arrays. The script allows you to create NFTs with metadata and view a list of minted NFTs along with their details.

## Requirements

To run this script, you need to have Node.js and a code editor installed on your computer.

## How to Use

1. **Clone the repository**:

   Clone this repository to your local machine using the following command:

   ```
   git clone <repository-url>
   ```

2. **Navigate to the project directory**:

   Change your working directory to the cloned repository folder:

   ```
   cd <repository-folder>
   ```

3. **Run the JavaScript script**:

   Run the `nft_manager.js` JavaScript script using Node.js:

   ```
   node nft_manager.js
   ```

   The script will execute several functions to create NFTs, list their metadata, and display the total number of minted NFTs.

4. **View NFT Metadata**:

   The `mintNFT` function is used to create NFTs and store them in the `NFTs` array. Each NFT has metadata containing the sender's name, receiver's name, and the amount associated with the NFT.

5. **List NFTs**:

   The `listNFTs` function prints the metadata of all minted NFTs. It will display the sender's name, receiver's name, and the associated amount for each NFT.

6. **Get Total Supply**:

   The `getTotalSupply` function prints the total number of minted NFTs in the `NFTs` array.

## Functions

### mintNFT

```javascript
function mintNFT(sender_name, receiver_name, amount) {
    // Create an NFT object with metadata
    const NFT = {
        "sender": sender_name,
        "receiver": receiver_name,
        "amount": amount
    };

    // Store the NFT object in the NFTs array
    NFTs.push(NFT);
}
```

### listNFTs

```javascript
function listNFTs() {
    for (let i = 0; i < NFTs.length; i++) {
        console.log("ID:       " + (i + 1));
        console.log("Sender:   " + NFTs[i].sender);
        console.log("Receiver: " + NFTs[i].receiver);
        console.log("Amount:   " + NFTs[i].amount + "\n");
    }
}
```

### getTotalSupply

```javascript
function getTotalSupply() {
    console.log("\nTotal number of NFTs: " + NFTs.length);
}
```

## License

This code is released under the [MIT License](LICENSE).

## Disclaimer

This code is provided as a demonstration and for educational purposes. Use it at your own risk. The code may not have undergone full testing or security auditing. Always exercise caution when using or implementing code in production environments.

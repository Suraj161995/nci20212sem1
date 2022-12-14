## ERC-20 could be termed as a technical specification for exchangeable tokens which are produced for the Ethereum blockchain. This token is the one which is interchangeable with the other tokens, whereas, the non-exchangeable tokens or called as non-fungible tokens (NFTs) are non-transferable tokens which could never be interchanged with others.

## Lets get on to the steps for the creation of our own Ethereum contract of GoerliETH coin.

## In our file Storage.sol, we shall provide our own name and symbol of the contract for new coin ##

	constructor(string memory name_, string memory symbol_) {
        _name = "Suraj_95218";
        _symbol = "Suraj_95218";

        _mint(_msgSender(), 1000000000000000000000000);
    }
	
## Now running this file and then deploying the same over the Remix IDE. Please refer below snap that it activates the metamask tab for confirming the same and to proceed thereafter.##

![1](https://user-images.githubusercontent.com/52279327/207640957-dffa144a-ba9b-438a-b37c-8602a449a32f.png)


3. Now copy this contract and get into the transaction details for the same as per the below snap for reference.

![2](https://user-images.githubusercontent.com/52279327/207641023-1690633e-983f-4aac-a46b-710b36f78dfb.png)

## We see that the contract has been created ##

![3](https://user-images.githubusercontent.com/52279327/207641073-72a0fa9d-2065-4292-abb4-7fd0ac84979a.png)



## Building the image along with the docker tag, find the snap below the command for reference ##

```docker build -t suraj161995/my_goerli_eth:suraj .```

![4](https://user-images.githubusercontent.com/52279327/207642378-ade4884f-cfba-42f8-a549-4559ec075ab9.png)

	
## Now push the code to the Docker Hub using the Docker Tag, we shall see that the image is published over the Docker Hub ##

```docker push suraj161995/my_goerli_eth:suraj```


![5](https://user-images.githubusercontent.com/52279327/207642401-99330978-4dfc-4780-96c4-c99711e8cfdc.png)




## Run the curl command ##

## This transfers ETH: ##

```curl --header "Content-Type: application/json" --request POST --data '{"address":"0xac4FafdA6A3A6B48b4cDC2a896acf8D104C81d6C", "amount":"0.05"}' http://localhost:8090/eth```

## This transfers token: ##

```curl --header "Content-Type: application/json" --request POST --data '{"address":"0xac4FafdA6A3A6B48b4cDC2a896acf8D104C81d6C"}' http://localhost:8090/token```


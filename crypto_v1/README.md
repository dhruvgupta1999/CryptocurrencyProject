1) to add transactions to pending transactions list of user

curl "localhost:8070/txion"      -H "Content-Type: application/json"      -d '{ "to":"f", "amount": 10}'

2) 8070,8080,8080 are ports for users. 9000 is for miner

3) project does not have network layer implemented yet (future work)

4) node_urls:

user1 :  http://localhost:8070
user2 :  http://localhost:8080
user3 :  http://localhost:8090
miner :  http://localhost:9000

5) 
node_url/getchain -> to get current chain
node_url/updateChain -> to update chain picking longest chain from peers
node_url/createBlock -> to mine block after collecting pending transactions from all peers. (Works only on miner program)

curl "localhost:8070/txion"      -H "Content-Type: application/json"      -d '{ "to":"f", "amount": 10}'    -> to add entry to pending transaction

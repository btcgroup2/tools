# 命令行测试说明

### 查询钱包地址列表
bitcoin-cli -regtest getaddressesbyaccount ""

### 生成新地址
bitcoin-cli getnewaddress 1LnfTndy3qzXGN19Jwscj1T8LR3MVe3JDb

### 获取客户端信息（blocks、balance）
bitcoin-cli -regtest getinfo

### 获取余额
bitcoin-cli –regtest getbalance

### 获取区块链信息（blocks、headers）
bitcoin-cli -regtest getblockchaininfo

### 挖矿
bitcoin-cli -regtest generate 100

### 交易支付
bitcoin-cli -regtest sendtoaddress mwBXwXZ2xAzenbvvBroniEpbnUe17fVDNE 21

### 查询交易
bitcoin-cli -regtest gettransaction b555bf7b982160c00824c6e4a962ec84cc67f8f46d1305f879a2d498ffe67175

### 查询区块
bitcoin-cli -regtest getblock 44761c1f9061fda16f4eb1e5f69a0783683491b8033689454ce2288c3c416216

### 查询UTXO
bitcoin-cli listunspent

### 查询UTXO详情
bitcoin-cli gettxout 9ca8f969bd3ef5ec2a8685660fdbf7a8bd365524c2e1fc66c309acbae2c14ae3 0

### 手工造交易
bitcoin-cli createrawtransaction ‘JSON’

### 手工签名
bitcoin-cli signrawtransaction  0100000001e34ac1e2baac09c366fce1c2245536bda8↵
f7db0f6685862aecf53ebd69f9a89c0000000000ffffffff02a0252600000000001976a914d90↵
d36e98f62968d2bc9bbd68107564a156a9bcf88ac50622500000000001976a91407bdb518fa2e↵
6089fd810235cf1100c9c13d1fd288ac00000000

### 手工提交交易
bitcoin-cli sendrawtransaction  0100000001e34ac1e2baac09c366fce1c2245536bda8↵
f7db0f6685862aecf53ebd69f9a89c0000000000ffffffff02a0252600000000001976a914d90↵
d36e98f62968d2bc9bbd68107564a156a9bcf88ac50622500000000001976a91407bdb518fa2e↵
6089fd810235cf1100c9c13d1fd288ac00000000

### 解码交易
bitcoin-cli -regtest decoderawtransaction 020000000481146c5e691d5aa9cd0690b920feb443aa624fc234907990d6fcbcad174a96210000000049483045022100cf32d0386cd18251c4111fb8927b149bfef7a61ec7982c941d919093bf8da3fd02200080915b941c15c4dab032a42cefd71bb6a90df393c2538498a47570006a2d5701feffffff9182fb73a3b3c791f5f1543c5adce8c7e91755b9956ca443858d9648d883dee30000000049483045022100e48758645c126ab2904878b0948448f7100b98daf8a04889a08c5e095fa32a5a022047baa2572683a697bf4ae0ce346232a6054590e9f0883196dd0a21d30ef4c84801feffffff9ed41001bf00916d656446e332d970601dc9200a624f0ccaf62383ba4e4dd86d000000006b483045022100c9793f287c579577e51b978487f7da0749b3aec18c9b0f49af29b37196045f1402201236233d15e1b55eeeb046276a2713d8847c9ac284447c952706dc339541040d012102f66cf660381048ff9aa477c3aac0381b38525a7c544b28ffc845fc1a93ad616bfefffffff31a2c128278f6f3c952c777d5aed2c644c00e66bd471b46ee79de390232a81a0000000049483045022100f6b3d53d47d03059e91bc412647b32e4f085b02da6a3c197499dc4b336e2413c022060f5f8c840c14ee1f2309a716cd96275cd40773e4fec102fd02f1485789a6d6701feffffff0200f2052a010000001976a9141f6d648f728128746ad6c72dccdd11bce907949388ac7874e60e000000001976a9146687810048bf8c996420c6ed2e0672308ee6028788ac66020000

### 查询指定高度块Hash
bitcoin-cli -regtest getblockhash 225

### 获取内存池原始交易ID
bitcoin-cli -regtest getrawmempool

### 获取节点信息
bitcoin-cli -regtest getpeerinfo

### 获取连接数
bitcoin-cli -regtest getconnectioncount

### 获取UTXO汇总信息集
bitcoin-cli -regtest gettxoutsetinfo


[bitcoin-cli常用命令汇总](https://github.com/btcgroup2/tools/blob/master/bitcoin-cli常用命令.pdf)

# 脚本使用说明


### getinfo:查询所有节点的info
getinfo [日志文件名]

Eg. getinfo getinfo11
### generate:挖矿
generate [节点名] [块数] [日志文件名]

Eg. generate btcorgNode1 101 generate12
### transaction:交易
transaction [节点1] [节点2] [金额] [日志文件名]

Eg. transaction btcorgNode1 btcorgNode2 10 transaction22
- 生成节点2交易地址
- 节点1向节点2发起交易
- 所有节点查询交易
### confirmtx:确认交易
confirmtx [节点名] [日志文件名]

Eg. confirmtx btcorgNode1 confirmtx11
- 挖矿1块打包交易
- 所有节点查询新打包区块
### getblockhash:获取指定高度块hash
getblockhash [高度] [日志文件名]

Eg. getblockhash 101 getblockhash101
### getnodes:获取节点信息
getnodes [日志文件名]

Eg. getnodes getnodes1

_注意：日志文件名不包含扩展名.log_

[脚本测试样例](https://github.com/btcgroup2/tools/blob/master/脚本测试样例v4.pdf)
[测试日志](https://github.com/btcgroup2/test-log)

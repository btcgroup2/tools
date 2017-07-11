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

[脚本测试样例](tools/脚本测试样例v3.pdf)

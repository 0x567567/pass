# pass
这是测试文件
请注意不要随意使用
lens op
// 查询 ETH 等原生资产余额
function getEthBalance(walletAddress, network) {
  let rpcLink = RPC_MAP[network];
  if (!rpcLink) {
    return "Error: Invalid Network Name";
  }
  const data = "0x" + "balanceOf" + "000000000000000000000000" + walletAddress.slice(2);
  const response = UrlFetchApp.fetch(rpcLink, {
    method: "post",
    payload: JSON.stringify({

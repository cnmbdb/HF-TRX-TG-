#`appsettings.json`说明
{
  "Serilog": {
    "MinimumLevel": {
      "Default": "Information",
      "Override": {
        "Microsoft": "Warning",
        "Microsoft.Hosting.Lifetime": "Information"
      }
    }
  },
  "AllowedHosts": "*",
  "TronNet": {
    "Host": "grpc.trongrid.io",
    "ChannelPort": 50051,
    "SolidityChannelPort": 50052,
    "ApiKey": "123456" //ApiKey，可以在此处申请：https://www.trongrid.io/dashboard/keys
  },
  "TronConfig": {
    "Address": "Taaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa", //钱包地址，建议另外新建钱包地址
    "PrivateKey": "aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa", //私钥，建议另外新建钱包地址
    "USDTContractAddress": "TR7NHqjeKQxGTCi8q8ZY4pL8otSzgjLj6t", //此为USDT合约地址，请勿修改！！！
    "ApiHost": "https://api.trongrid.io" //节点地址，默认官方节点，自己有节点也可以用自己的
  },
  "ConnectionStrings": {
    "DB": "Data Source=TG-CoinConvert.db;"
  },
  "Address": {
    "USDT-TRC20": [ "TA7uZiE2kLpyEjJrLhyLvmBk8cjsb8ipar", "TS6gwDBNWDy51unAQHAysJ53u2mtLMAKhZ" ] //监听的USDT入账地址，同时也是展示给用户的转账地址，修改为你自己的地址，只有一个就只填写一个
  },
  //"WebProxy": "http代理或socks5代理字符串，如：http://127.0.0.0:6666，如无需代理请去掉此项",
  "BotConfig": {
    "Token": "5432101234:AA111-11111111111111111111111111111",
    //"Proxy": "Telegram Api代理，如无，可去掉",
    "AdminUserId": 10086, //管理员UserId，可至 @QueryCoinBot处发送 查id 获取
    "AdminUserUrl": "@TestUserName" //你的联系方式，可以是文字、@YourUserName、或t.me/YourUserName
  },
  "MinToken": {
    "USDT": 5 //最小兑换USDT数量
  },
  "TrxRate": 0, //1 USDT兑换的TRX汇率，不设置或设为0使用实时汇率
  "FeeRate": 0.1, //从最终用户获取的TRX中的抽成比例，设置0.1表示抽成10%
  "USDTFeeRate": 0, //USDT手续费，设置0.01表示抽成1%，不足1U扣1U，设为0时不扣此项手续费
  "SendTo": 0, //目标群组的TG ID，通常是一个很大的负数 可以将@QueryCoinBot拉入群，发送查id获取群id
  "BlackList": [ "Txx1" ], //黑名单地址，不处理此地址的兑换请求，多个地址以逗号隔开
  "SetDefaultMenu": true //设置默认菜单，机器人初始菜单
}

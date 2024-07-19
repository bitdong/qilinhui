# 以 1、3、bc1 开头的比特币地址都有啥区别？

大家应该都接触过比特币地址。比特币地址就好像银行卡卡号，通过银行卡卡号，任何人都可以向你转账；而通过比特币地址，任何人也可以向你转比特币。

比特币地址是由26\~34位字母和数字组成的字符串。比特币的地址的前缀（开头的字符）有如下这些：

<figure><img src="https://btcdayu.gitbook.io/~gitbook/image?url=https:%2F%2Fpic1.zhimg.com%2F80%2Fv2-7c5ad36328797312a3f9fdc2b0b80bac_1440w.webp&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=938f3dad0badcf849f0128055d5d16ff0d9bfb6198b5bf5bd14bd621ae8c7284" alt=""><figcaption></figcaption></figure>

我们常见的比特币地址前缀有： 1、3、bc1。它们有什么区别？哪一个的转账手续费更便宜呢？

要说清楚这些，我们得结合比特币地址的分类。比特币地址的分类如下：

## 1、传统地址 <a href="#id-1-chuan-tong-di-zhi" id="id-1-chuan-tong-di-zhi"></a>

1开头的地址，被称为传统地址 ( Legacy Address )。这就是最原始的比特币地址，比如：创世地址：[1A1zP1eP5QGefi2DMPTfTL5SLmv7DivfNa](https://link.zhihu.com/?target=https%3A//tokenview.com/cn/search/1A1zP1eP5QGefi2DMPTfTL5SLmv7DivfNa)，属于中本聪。该地址内初始50个BTC，后来，比特币爱好者不断往该地址转入BTC，以表达对中本聪的敬意，写文章这一刻，BTC 余额：68.13424603个。

1 开头的地址，采用 P2PKH ，P2PKH(Pay-to-Pubkey Hash)，支付公钥哈希，即比特币交易输入输出脚本，采用公钥及公钥哈希。

1开头的传统地址，上线至今，一直被支持，我们可以从它发送 BTC 到下面介绍的多签地址和隔离见证地址。

## 2、多签地址 <a href="#id-2-duo-qian-di-zhi" id="id-2-duo-qian-di-zhi"></a>

3开头的地址，比如 3EktnHQD7RiAE6uzMj2ZifT9YgRrkSgzQX。2012年的比特币改进提案中，新增 P2SH 的地址。

P2SH (Pay-to-Script-Hash)，支付脚本哈希，即比特币交易输入输出脚本，采用赎回脚本及赎回脚本哈希。其地址结构类似于 P2PKH，但它支持比传统地址更复杂的功能。P2SH 脚本函数最常用于 multisig 地址，这些地址可以指定多重数字签名来授权事务。举个例子：某个3开头的地址由三人控制，其中，任意两人同意，便可发起转账。

### 隔离见证地址 <a href="#ge-li-jian-zheng-di-zhi" id="ge-li-jian-zheng-di-zhi"></a>

隔离见证是一种区块链扩容的方法，已在比特币和莱特币上成功实施。我们常见的部分 3 开头的地址，和 bc1 开头的比特币地址，就是隔离见证地址。

### 隔离见证 <a href="#ge-li-jian-zheng" id="ge-li-jian-zheng"></a>

隔离⻅证，是比特币协议的一个兼容性升级，它将签名数据从比特币交易中分离出来。

话说比特币区块链上的每个区块内，不仅记录了每一笔转账交易的时间、账户、收到或转出的比特币数量等具体信息，还包括每一笔交易的数字签名。矿工们在打包区块时，需要用数字签名来验证每一笔交易的合法性，确认无误后，才会将交易记录在区块里。

然而，普通用户只关心自己账户有多少比特币，并不需要验证每一笔交易。所以，隔离见证就把区块内的数字签名信息拿掉，从而减少交易字节数，让每个区块可以承载更多笔交易，进而达到扩容的目的。

2017年8月，隔离见证正式激活。

隔离见证具有如下优势：

1、更安全：对比传统地址（1 开头的地址），隔离见证地址具有更好的安全性。 2、更快速，可增大区块容量，检查交易速度更快。 3、更便宜，隔离见证地址的转账手续费比传统地址（1 开头的地址）更便宜。 4、具备兼容性：隔离见证是软分叉，是兼容性升级，支持旧节点；

因为隔离见证是兼容性升级，因此存在兼容地址和原生地址两种。

## 3、 隔离见证兼容地址(Nested Segwit Address) <a href="#id-3-ge-li-jian-zheng-jian-rong-di-zhi-nested-segwit-address" id="id-3-ge-li-jian-zheng-jian-rong-di-zhi-nested-segwit-address"></a>

3开头的地址：因为使用 P2SH 方式打包，所以隔离见证兼容地址，也以3开头，旧节点能识别。

大家不需要知道——以3开头的比特币地址，到底是多签地址，还是隔离见证兼容地址，只需要知道以3 开头的地址，被广泛支持，可以向 1开头 和 bc1 开头的地址发送比特币即可。

## 4、 原生隔离见证地址 （Native Segwit Address） <a href="#id-4-yuan-sheng-ge-li-jian-zheng-di-zhi-native-segwit-address" id="id-4-yuan-sheng-ge-li-jian-zheng-di-zhi-native-segwit-address"></a>

bc1 开头的地址，是由新的隔离见证脚本生成的地址（P2WPKH 或 P2WSH），是纯正的隔离见证地址。

它采用 Bech32 编码，其风格和 P2PKH 和 P2SH（即 1开头和 3开头）风格的地址完全不同。 由于使用 bc1 前缀，它比上面两种地址要长，由42个符号组成，比如：

bc1qa5ndt07z2lu7r2kl6zrffw362chj74vse76lq5

不过，它具有更多优势：

1、没有大小写 2、生成的二维码面积更小 3、可以错误纠正（不推荐使用）

目前，只有部分钱包支持原生隔离见证地址 ，支持的交易所也不多。

## 转账手续费，哪家强（便宜）？ <a href="#zhuan-zhang-shou-xu-fei-na-jia-qiang-bian-yi" id="zhuan-zhang-shou-xu-fei-na-jia-qiang-bian-yi"></a>

当然是隔离见证地址的转账费用强，更便宜。这是因为，传统地址、多签地址交易事务更大，占用更多字节。而隔离见证可以减少交易字节数，如果我们使用隔离见证地址作为收款地址，之后再使用该隔离见证地址给其他人转账，就可以节省转账成本。

[Bitcoin Optech 的统计数据](https://link.zhihu.com/?target=https%3A//bitcoinops.org/en/newsletters/2019/04/16/)的统计数据显示：

隔离见证兼容地址（部分3开头）比传统地址（1开头）节省 24% 转账手续费； 原生隔离见证地址（bc1开头）比传统地址（1开头）节省 35% 转账手续费； 隔离见证地址（bc1开头和部分3开头） 比 多签地址（部分3开头），最多可以节省 70% 转账手续费；

总结：bc1 开头的原生隔离见证地址，最省转账费用。

## 建议 <a href="#jian-yi" id="jian-yi"></a>

目前，仅有不到 1% 的 BTC 存储在 bc1开头的地址中。

比特派（bitpie）、imToken2.0、Ledger、Keepkey 钱包，目前都不支持 bc1 开头的地址 。 而大多数交易所，只支持将 BTC 发送到 bc1 开头的地址，但不支持以 bc1 地址接收 BTC。

支持 bc1 开头地址的钱包和交易所数量，还在缓慢增加中。

但是，隔离见证地址的转账手续费又便宜那么多，怎么办？建议：

## 1、先切换到 3开头的 隔离见证兼容地址 <a href="#id-1-xian-qie-huan-dao-3-kai-tou-de-ge-li-jian-zheng-jian-rong-di-zhi" id="id-1-xian-qie-huan-dao-3-kai-tou-de-ge-li-jian-zheng-jian-rong-di-zhi"></a>

如果你的比特币地址还是 1 开头的传统地址；而且你又使用 比特派钱包，或 imToken2.0 钱包，他们目前又只支持 以 3 开头的隔离见证兼容地址。同时，你又不打算更换钱包，那么，你在钱包 APP 中，可以直接切换成 以 3 开头的隔离见证兼容地址。

注意：比特派 V4.4.4 开始支持三种地址（传统地址，隔离见证兼容地址，隔离见证地址）

<figure><img src="https://btcdayu.gitbook.io/~gitbook/image?url=https:%2F%2Fpic2.zhimg.com%2F80%2Fv2-3fc8c2ca5e42eab2ac37d4d041bbde69_1440w.webp&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=567a7f83cbb54f35ef3c5b6f2e87445940a9e1b1d1def951f644faa86a3ad1b1" alt=""><figcaption></figcaption></figure>

<figure><img src="https://btcdayu.gitbook.io/~gitbook/image?url=https:%2F%2Fpic3.zhimg.com%2F80%2Fv2-a40fa43649402517a87ea6ddae9e2ce6_1440w.webp&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=b1c97436065bc1a6cece0dac8bf9c79ccfd1ed4788c28f822606b9b168b15f42" alt=""><figcaption></figcaption></figure>

详细步骤请点击：

[《地址簿》](https://link.zhihu.com/?target=http%3A//docs.bitpie.com/zh\_CN/latest/AddressBook/index.html%23id6) [《比特币钱包如何切换地址类型？》](https://link.zhihu.com/?target=https%3A//support.token.im/hc/zh-cn/articles/360005001894-%25E6%25AF%2594%25E7%2589%25B9%25E5%25B8%2581%25E9%2592%25B1%25E5%258C%2585%25E5%25A6%2582%25E4%25BD%2595%25E5%2588%2587%25E6%258D%25A2%25E5%259C%25B0%25E5%259D%2580%25E7%25B1%25BB%25E5%259E%258B-)

## 2、直接创建 bc1 开头的原生隔离见证地址，将BTC转入 <a href="#id-2-zhi-jie-chuang-jian-bc1-kai-tou-de-yuan-sheng-ge-li-jian-zheng-di-zhi-jiang-btc-zhuan-ru" id="id-2-zhi-jie-chuang-jian-bc1-kai-tou-de-yuan-sheng-ge-li-jian-zheng-di-zhi-jiang-btc-zhuan-ru"></a>

你可以直接用比特派 V4.4.4创建 bc1 开头的原生隔离见证地址。

<figure><img src="https://btcdayu.gitbook.io/~gitbook/image?url=https:%2F%2Fpic2.zhimg.com%2F80%2Fv2-3fc8c2ca5e42eab2ac37d4d041bbde69_1440w.webp&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=567a7f83cbb54f35ef3c5b6f2e87445940a9e1b1d1def951f644faa86a3ad1b1" alt=""><figcaption></figcaption></figure>

<figure><img src="https://btcdayu.gitbook.io/~gitbook/image?url=https:%2F%2Fpic1.zhimg.com%2F80%2Fv2-0c243921d5d43211b2ae3014dddea6f8_1440w.webp&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=8df0177fa5572528abe901ffd8fd28f85fef75d2486612a85f456365f02b8521" alt=""><figcaption></figcaption></figure>

大家也可以使用[Electrum](https://link.zhihu.com/?target=https%3A//electrum.org/%23download) 比特币钱包，来创建 bc1 开头的原生隔离见证地址。

bitcoin:bc1qhldx2ec8nkwdq4yt37em0rgn0gjf55945v8r22 (二维码自动识别)

如果未来，你会有很多比特币，那么 bc1 比特币地址值得拥有，赶紧准备起来吧！

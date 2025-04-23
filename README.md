## 使用方法
1. 新建一个私人仓库，项目可随意命名，但要避开 BPB 敏感词。
2. 在该项目创建`.github/workflows/Obfuscate.yml`。
3. 点击`Obfuscate.yml`旁边的小黄点同步到 BPB 代码，同步完成生成`_worker.js`与`origin.js`，前者是混淆代码，后者是明文代码。如果找不到小黄点，请前往：`你的项目`→`Actions`→左边的`Build Obfuscate BPB Panel`→中间的`Build Obfuscate BPB Panel`的工作流文件是否有效。
4. 到`Cloudflare`里创建`Pages+github`，找到刚刚的 github 项目，用其创建 Pages 项目，并修改下面的变量及绑定 kv 空间。


## 变量的使用
1. `UUID`，[在线生成](https://1024tools.com/uuid)。UUID-大写
2. `PROXYIP`，来源于网络分享：`proxy.xxxxxxxx.tk`、`edgetunnel.anycast.eu.org`、`ts.hpc.tw`、`cdn.xn--b6gac.eu.org`、`cdn-all.xn--b6gac.eu.org`、`bestproxy.onecf.eu.org`。
3. `TR_PASS`，默认要修改的密码。
4. `kv`，绑定`KV命名空间`。kv-小写
5. `/panel`，部署成功后，在 url 后面增加/panel来进行访问面板，访问面板修改的密码将会保存在`kv`对里。

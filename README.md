# awd-platform 原链：https://github.com/zhl2008/awd-platform
放在这里是避免自己重复造轮子，原链中有一些难搞的问题，也希望大家不用吧时间都花费在部署上边。

参考:https://mp.weixin.qq.com/s?__biz=MzU1MzE3Njg2Mw==&mid=2247486325&idx=1&sn=96c04f3609a04260eabdd187fc7c38b1&chksm=fbf79105cc8018131579ad228dbf22a33bbdf0c8c71d3b8c090583b42ea21d80de53fc1efa70&scene=27&key=593393174013ce6d958e86eb764289b105cb7cea44d471bd3f9fe1a2ed76f546343dacb9b40a352e642e425b55c2a4d9698146a114ecd9680ed3262c8f96f6a206f0c78d6818ce0028c9bc75830936f0&ascene=7&uin=NTQ5ODg5NzY1&devicetype=Windows+10&version=6206061c&lang=zh_CN&pass_ticket=s3n8uD0SG7m1vojw%2F%2BN7uxdrTxvWnumzuUe%2BTLY12QY9yFKjU7n%2FNruWi9PS1sJO&winzoom=1

**说明：**
已经修改了原平台的错误，可能会出现自己没有料想的错误吧。(未测)
如果你想自己安装可以参考如上链接，以及我自己的文章：https://www.yuque.com/u22312613/plo1s4/ogwgvz

## 关于平台的基本使用
1.cd awd-platform/
2.docker pull zhl2008/web_14.04
3.docker tag zhl2008/web_14.04 web_14.04

4.根据当前队伍数量copy所有的队伍的比赛文件夹
python batch.py web_yunnan_simple 10

5.启动比赛环境
python start.py ./10

6.关闭环境命令
python stop_clean.py


关于裁判页面！！重点：已经将别人的美化界面放入其中，但是需要修改一处设置;
root@qqq:~/awd-platform/flag_server# cat index.php 

**$result = file_get_contents("http://47.93.45.133:8080/score.txt");**将此处修改为自己的服务器。

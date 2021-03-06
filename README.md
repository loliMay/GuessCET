# CET猜号助手
让你没有准考证也能很快查到你的四六级成绩！
## 前言
是不是好不容易四级成绩出来了，却突然发现...尼玛怎么还要四级准考证呀！这东西早丢了啊，完了...
如果你是和作者一样的遭遇的话，寻求不需要准考证也能如愿查到四级成绩的方法，恭喜你找对地方了！

原理很简单，穷举法。前提条件是你要记得你在考场中的大概位置，记得越清楚就越能省去很多不必要的穷举，从而加快最终拿到成绩的速度。作者隐约记得自己的考场座位是在最后一组的靠后位置，这个特征比较明显。凭借着万年单身手速，二十多分钟就拿到成绩了！还好给杨超越上香了，最后险过。最后作者发现自己的考场是54考场，如果你们比较幸运的话，考场靠前，花的时间会比作者更少！

## 无准考证查分原理分析
### 准考证规律
准考证号一共是15位
1. 前6位是省份、校园、校区代码 [点此查你的学校的前6位码](UniversityCode.md)
2. 第7-8位是考试年份，例如2010年的即是10
3. 第9位是该年中第几次四六级考试，例如2010年12月份的考试由所以第2次考试，所以是2
4. 第10位是四六级种类，四级是1，六级是2
5. 第11-13位是考场号，例如第1考场即是001
6. 第14-15位是坐位号，例如1号坐位即是01

![](http://images.lolimay.cn/18-8-23/73398963.jpg)

### 确定准考证的前10位
1. 最简单的方法是问你们学校和你同一次参加考试的同学，你们的准考证**前10位**是一样的
2. 第2种方法就是按照上面所提到的准考证规律推测出前10位。

如，作者是安徽大学磬苑校区的，18年6月参加的四级考试。
1. 前6位：安徽大学磬苑校区对应的6位校区码是 ——> 340030
2. 7-8位：18年参加考试 ——> 18
3. 9位：18年的6月是该年的第一次考试 ——> 1
4. 10位：四级考试 ——> 1
故我的准考证号前10位是 3400301811

## 穷举最后5位
其实最难的是猜四级准考证的最后5位，倒数第3位到第5位这3位是考场号，最后两位是座位号。

我们学校的每个考场30人，故座位号的范围是 01～30。

## 脚本使用方法
### 1. 下载 Chrome 拓展 [Tampermonkey](https://tampermonkey.net/)
Download Tampermonkey Stable 将它添加到你的 Chrome 扩展程序中，这时你会发现你的 Chrome 的右上角多了个 <img src="http://images.lolimay.cn/18-8-23/18970281.jpg" />图标，点击这个图标选择 **添加新脚本** ，将编辑器清空， 如下图所示

![](http://images.lolimay.cn/18-8-23/59866667.jpg)

### 2. 将 [src/main.js](src/main.js) 中的内容添加到 Tampermonkey 的自定义脚本中
记住配置相关的参数
### 3. 打开 [四六级查分网站](http://cet.neea.edu.cn/cet/)
脚本会自动填充你的信息，这是只需要不停地输入验证码，回车查看结果。
如果提示查询结果为空，再回车一次，接着继续输验证码。重复上述步骤直到查到你的成绩。

## 彩蛋
因为作者四级考试的座位比较明显，我隐约记得自己是坐在考场的最后一组靠后的位置，所以我只穷举每个考场的25～30号。从第1考场一直穷举到 54 考场，一共穷举了三百多次。而且作者常年单身，手速超快，每3到5秒就能输一个验证码，实际穷举只花了大概**二十多分钟**就穷举出来了。如果你运气好考场号靠前的话，甚至更快！

最后，祝你成功在无准考证的情况下使用本工具查到你的四级成绩！Have fun!

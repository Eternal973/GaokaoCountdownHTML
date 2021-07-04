<!DOCTYPE html>
<!--注：所有标注“讲解”的地方都可以按自己的需求更改，同时可以按自己的水平加入一些新的内容如字体图片动画等等。-->
<html lang="zh-CN">
<!--讲解：语言中文简体-->
<head>
    <meta charset="UTF-8">
    <title>差不多得了</title>
    <!--讲解：标题-->
</head>
<body onload="time()" >
<div style="margin-top: 50px;border-radius: 50px;background: #39c5bb;padding-bottom: 10px;padding-top: 10px;margin-left: 200px;margin-right: 200px;">
<!--讲解：margin-top是上边距，border-radius是圆角的半径，background背景色（这里采用VOCALOID官方提供的初音色），padding是填充文本，下边距上边距，margin左右边距。-->
    <h1 align="center" style="font-size:  4em">这都什么时候了还在玩电脑？？</h1>
<!--讲解：居中，字号-->
    <h2 style="margin-left: 200px">现在是</h2>
<!--讲解：左间距-->
    <h2 id="now" align="center" style="color: #b37d67;font-size: 42px;"></h2>
<!--讲解：id是下面js里现在时间的id，居中，颜色（这里采用设定图中广泛认同的御坂美琴发色），字号-->
    <h2 style="margin-left: 200px">距离2022年高考只有：</h2>
<!--讲解：左边距-->
    <h1 id="time" align="center" style="color: #ee1c25;font-size: 72px;"></h1>
<!--讲解：id是js里倒计时id，居中，颜色（这里采用中国政府网国旗色），字号-->
</div>
<!--讲解：下面是JS部分-->
<script>
    function  time(){
    <!--讲解：定义time-->
        let N =new Date();
        <!--讲解：定义N为当前时间戳-->
        document.getElementById("time").innerHTML=Math.floor((new Date(2022,6-1,8)-N.getTime())/(24*60*60*1000))+"天"
        <!--讲解：document把后面的运行结果推到id为time的项里。计算剩余天数，new Date后括号里可以修改成自己想要的，格式yyyy,mm-1,dd，时间戳计算并转换成天数-->
        document.getElementById("now").innerHTML=N.getFullYear()+"年"+(N.getMonth()+1)+"月"+N.getDate()+"日"+N.getHours()+"时"+N.getMinutes()+"分"+N.getSeconds()+"秒";
        <!--讲解：document把后面的运行结果推到id为now的项里。导出获取到的N中的年月日时分秒并输出。-->
        console.log("log");
        <!--讲解：在控制台输出一个日志-->
    }
    setInterval(time,1000);
    <!--讲解：以1s为周期重复运行time，达到更新时间的效果。-->
</script>
<!--by Eternal973-->
<!--2021.6.24-->
<!--讲解更新于2021.7.4-->
</body>
</html>
<div align="center">

# **Bilibili粉丝牌助手**  

 </div>

1-2更新 **请大家及时更新代码，云函数版请删除先前创建的函数，重新下载压缩包部署**

基于Python3异步开发的自动获取每日小心心及直播间自动打卡脚本  
运行环境：不低于Python3.6  
***  

## 已实现功能  
> 直播区每日签到 ✅  
> 每日获取24个小心心 ✅  
> 指定房间每日弹幕打卡并赠送小心心、辣条 ✅  
> Server酱微信推送 ✅  
> 自动弹幕打卡所有粉丝牌房间 ✅   
## 更新修复  
请大家及时更新代码，云函数版请删除先前创建的函数，重新下载压缩包部署  
> 10-30 [0.2.0]修复：B站接口失效导致无法正常签到、送小心心  
> 11-1  [0.3.0]修复：Server酱推送失败问题，概率无法赠送所有小心心问题  
> 11-11 [0.4.0]修复：短房间号发送心跳、弹幕请求失败问题，当背包初始为空时程序会异常报错问题  
新增：自动赠送辣条、自动弹幕打卡所有粉丝牌房间、自动每日700银瓜子兑换1硬币、部署时ruid不填或为0时将不赠送礼物  
> 11-12 [0.5.0]修复：当粉丝牌主人未开通直播间会报错  
> 11-13 [0.6.0]修复：在特殊房间弹幕打卡失败问题  
> 12-7 [0.7.0] 修复好多bug!!!不列了，开摆！ 

> 1-2 [0.8.0] 修复了由于B站接口更换导致的"用户不存在"BUG，解除了云函数必须大于9个粉丝牌才能运行的限制,现在和本地运行并无区别,详见教程！  
## 部署方式  
> ### 腾讯云函数版（**推荐🌟**）  
> >优点：  
免费、稳定、无需服务器、零基础部署  
缺点：**无** 

> ### 本地运行版  
> > 优点：  
没有粉丝牌数量限制  
缺点：  
需要自己搭建本地Python环境，设置定时任务  

## 详细教程  
- [获取B站Cookie](doc/bili.md)（**🌟这个很重要🌟**）  
- [Server酱推送](https://sct.ftqq.com/)（可选）  
- [腾讯云函数运行](doc/tencent_cloud.md) / [本地运行](doc/local.md)（二选一）  

## 常见问题   
- 获取小心心报错，如：用户不存在，KeyError('LIVE_BUVID',)，请**关闭无痕模式**重新抓取cookie！！  
- 每日小心心无法获取24个，请更换云函数的运行位置，或触发器运行时间 常见Cron 表达式：  
每天中午12点运行：`0 0 12 */1 * * *`  
每天早上6点30运行：`0 30 6 */1 * * *`  
每天晚上8点运行：`0 0 20 */1 * * *`  
- 有时候运行一次无法获取满24个小心心，**请设置多个时间不同的触发器！！！两个触发器间隔建议大于俩小时**  
- 为了维持脚本正常运行,弹幕打卡限制了100个粉丝牌打卡,望周知！
## 写在最后
在部署或使用过程中遇到什么问题，请首先**仔细**阅读文档，若发现自己实在无法解决的问题，可以提交Issues或者B站私信 ~~@晓轩iMIKU~~ (号被封了) [@晓小轩iAS](https://space.bilibili.com/32957695)(小号)提问，提问时请带上详细的日志或者运行结果截图，以便快速解决问题！  
最后欢迎大家B站关注：  
[@嘉然今天吃什么](https://space.bilibili.com/672328094/) [@向晚大魔王](https://space.bilibili.com/672346917/) [@乃琳Queen](https://space.bilibili.com/672342685/) [@贝拉kira](https://space.bilibili.com/1772442517/) [@珈乐Carol](https://space.bilibili.com/351609538/)  
<sub>ps:本项目夹带作者私货：每次执行时会随机关注一位A-SOUL成员（如果你没关注的话），若想取消此功能请注释掉代码中的某一行（嘿嘿~）</sub>

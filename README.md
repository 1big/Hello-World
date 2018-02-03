# Hello-World

##微信自动抢红包APP##


模拟手势操作进行抢红包，非插件，不需要root权限。


有两种模式：

高速模式：通过viewID查找nodeInfo，效率高，需要匹配对应的微信版本号。

兼容模式：通过text查找nodeInfo，效率没有前者高，但是可适用绝大部分大部分微信版本（目前暂时没有完全实现该模式）。



###2018.01.22    微信自动抢红包初版###

实现的功能如下：

1、锁屏（无密码）状态下的抢红包。

2、自己发的红包可抢。

3、私发、群聊红包可抢。

4、处于最近联系人界面时可抢屏蔽的群的红包。


###2018.01.24    添加主界面UI###

1、在主界面上可以设置模式

2、在主界面上添加了通知监听、模拟操作的开关

3、添加相关的权限开启说明

4、打开AccessibilityService中对通知变化的监听


###2018.01.24    修正小米、锤子等手机卡在红包界面无法自动点开的问题###

1、关键：增加flagRetrieveInteractiveWindows属性

2、临时解决各个窗口界面的冲突，特使Notificaiton和WindowContenChanged同时响应的冲突


###2018.01.25    修正一些问题###

1、修复小米、锤子等手机偶尔在点开界面不动的问题

2、把NoificationListenerService提高权限，设置为前台服务

3、添加自用Log类，在release的时候可以去掉Log

4、添加一些工具方法

5、修复由于太慢而停留在红包界面的问题（自动后退）

6、修正对于服务是否在运行的判断方法

7、其它一些修改


###2018.01.28    修正一些问题###

1、修正NotificationListenerService无法正常开关

2、修正NotificationListenerService正常运行时也无响应的问题

3、去掉远程Service

4、完善软件兼容性，使得软件可以正常运行在android 4.4.4版本以上

5、其他一些小修改


###2018.01.28    修正一些问题###

1、去掉Accessibility的NotificationChanged事件

2、完善软件的兼容性

3、其它一些修改


###2018.01.28    修正一些问题###

1、当卡在红包“开”的界面时，先退出当前聊天窗口再进入。（很可能是MIUI9的bug）

2、其他修改


###2018.02.04    增加延时功能，关键字过滤功能，完善UI界面###

增加延时功能，关键字过滤功能，完善UI界面

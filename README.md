刚写的开源小插件，在这里宣传下 ^_^ 欢迎吐槽

# CountDown.js 

### 一个用来实现简单页面倒计时的轻量级工具

#### 2.0版本升级，加入倒计时还剩指定时间执行的回调方法

### API

 - CountDown.openTimeCountBySeconds()

    根据要计时的秒数打开一个显示剩余时间的倒计时
    
    ***参数***：
    
    Ele: 放置倒计时的元素
    
    CountDownSeconds: 要计时的秒数
    
    Sign: 用于给倒计时设置标记 （可以给多个倒计时设置同一个标记）
    
    Divider: 分割时分秒的分割符
    
    EndFunc: 倒计时结束时执行的方法
    
    ps:以上均为可选参数
    
    ***示例***
    
        CountDown.openTimeCountBySeconds({
            Ele: document.getElementById('h1'),
            CountDownSeconds: 3600,
            Sign: 'flypie',
            Divider: ':',
            EndFunc: function () {
                console.log('end');
            }
        });

 - CountDown.openTimeCountByStartAndEndDate()

    根据计时开始和结束时间打开一个显示剩余时间的倒计时
    
    ***参数***：
    
    Ele: 放置倒计时的元素
    
    StartDate: 倒计时开始时间 (date类型)
    
    EndDate: 倒计时结束时间 (date类型)
    
    Sign: 用于给倒计时设置标记 （可以给多个倒计时设置同一个标记）
    
    Divider: 分割时分秒的分割符
    
    EndFunc: 倒计时结束时执行的方法
    
    additionToggle: 当倒计时还剩指定时间时执行一个回调函数 (seconds:还剩多少秒时执行,callback:回调函数)
    
    ps:除StartDate,EndDate外均为可选参数
    
    ***示例***
    
        CountDown.openTimeCountByStartAndEndDate({
            Ele: document.getElementById('h1'),
            StartDate: startDate,
            EndDate: endDate,
            Sign: 'flypie',
            Divider: ':',
            EndFunc: function () {
                console.log('end');
            },
            additionToggle: {
                seconds: 10,
                callback: function () {
                    alert('soon');
                }
            }
        });
        
 - CountDown.openTimeCountByStartAndEndDate()

    根据计时开始和结束时间打开一个显示剩余天数加时间的倒计时
    
    ***参数***：
    
    Ele: 放置倒计时的元素
    
    StartDate: 倒计时开始时间 (date类型)
    
    EndDate: 倒计时结束时间 (date类型)
    
    Sign: 用于给倒计时设置标记 （可以给多个倒计时设置同一个标记）
    
    Divider: 分割时分秒的分割符
    
    DateDivider: 天数和时间之间的分隔符
    
    EndFunc: 倒计时结束时执行的方法
    
    ps:除StartDate,EndDate外均为可选参数
    
    ***示例***
    
        CountDown.openDateAndTimeCountByStartAndEndDate({
            Ele: document.getElementById('h1'),
            StartDate: startDate,
            EndDate: endDate,
            Sign: 'flypie',
            Divider: ':',
            DateDivider: '天 ',
            EndFunc: function () {
                console.log('end');
            }
        });
        
 - CountDown.stopBySign()

    根据标记零时暂停一个倒计时
    
        CountDown.stopBySign('flypie');
    
 - CountDown.resumeBySign()

    根据标记恢复一个被零时暂停的倒计时
    
        CountDown.resumeBySign('flypie');
    
 - CountDown.closeBySign()

    根据标记永久性地关闭一个倒计时
    
        CountDown.closeBySign('flypie');

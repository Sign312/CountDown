刚写的开源小插件，在这里宣传下 ^_^

# CountDown.js 

## 一个用来实现简单页面倒计时的轻量级工具

---

### API

 - CountDown.openTimeCountBySeconds()
    根据要计时的秒数打开一个显示时间的倒计时
    
    **参数**：
    
    Ele: 放置倒计时的元素
    
    CountDownSeconds: 要计时的秒数
    
    Sign: 用于给倒计时设置标记 （可以给多个倒计时设置同一个标记）
    
    Divider: 分割时分秒的分割符
    
    EndFunc: 倒计时结束时执行的方法
    
    **示例**
    
        CountDown.openTimeCountBySeconds({
            Ele: h1,
            CountDownSeconds: 3600,
            Sign: 'flypie',
            Divider: ':',
            EndFunc: function () {
                console.log('end');
            }
        });
    
    
 - 列表项目
 - 列表项目

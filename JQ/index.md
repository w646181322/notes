### jQuery HTML 操作

#### 获取内容
> text()    设置或返回所选元素的文本内容            
> html()    设置或返回所选元素的内容（包括HTML标记）            
> val() 设置或返回表单字段的值          
>> 上面的三个 jQuery 方法：text()、html() 以及 val()，同样拥有回调函数。回调函数由两个参数：被选元素列表中当前元素的下标，以及原始（旧的）值。然后以函数新值返回您希望使用的字符串

#### 获取属性
> attr()    方法也用于设置/改变属性值,设置多个值时参数使用JSON格式            
>> 也提供回调函数。回调函数由两个参数：被选元素列表中当前元素的下标，以及原始（旧的）值。然后以函数新值返回您希望使用的字符串           

#### 添加新的 HTML 内容
> append()  方法在被选元素的结尾插入内容            
> prepend() 方法在被选元素的开头插入内容            
> after()   方法在被选元素之后插入内容          
> before()  方法在被选元素之前插入内容          
>> 上面四个方法都能够通过参数接收无限数量的新元素，例：
```
$("img").append(txt1,txt2,txt3)
```

#### 删除元素
> remove()  方法删除被选元素及其子元素,方法也可接受一个参数，允许您对被删元素进行过滤          
> empty()   方法删除被选元素的子元素            

#### 操作CSS
> addClass()    向被选元素添加一个或多个类          
> removeClass() 从被选元素删除一个或多个类          
> toggleClass() 对被选元素进行添加/删除类的切换操作         
> css() 设置或返回样式属性          

#### 尺寸方法
> width()   方法设置或返回元素的宽度（不包括内边距、边框或外边距）          
> height()  方法设置或返回元素的高度（不包括内边距、边框或外边距）          
> innerWidth()  方法返回元素的宽度（包括内边距）          
> innerHeight() 方法返回元素的高度（包括内边距）            
> outerWidth()  方法返回元素的宽度（包括内边距和边框）          
> outerHeight() 方法返回元素的高度（包括内边距和边框）          
> outerWidth(true)  方法返回元素的宽度（包括内边距、边框和外边距）          
> outerHeight(true) 方法返回元素的高度（包括内边距、边框和外边距）          

### jQuery DOM 遍历方法

#### 祖先元素
> parent()  返回被选元素的直接父元素 ，只会向上一级对 DOM 树遍历            
> parents() 返回被选元素的所有祖先元素，一路向上遍历到根标签. 可带参数进行过滤搜索          
> parentsUntil()    返回介于两个给定元素之间的所有祖先元素          

#### 后代元素
> children()    返回被选元素的所有直接子元素，可带参数进行过滤搜索          
> find()    返回被选元素的后代元素，一路向下知道最后一个后代,可带参数进行过滤搜索           

#### 同级元素
> siblings()    返回被选元素的所有同胞元素，可带参数进行过滤搜索            
> next()    返回被选元素的下一个同胞元素，只返回一个元素            
> nextAll() 返回被选元素的所有跟随的同胞元素            
> nextUntil()   返回介于两个给定参数之间的所有跟随的同胞元素            
> prev()    返回被选元素的上一个同胞元素，只返回一个元素            
> prevAll() 返回被选元素的所有前面的同胞元素            
> prevUntil()   返回介于两个给定参数之间的所有前面的同胞元素            

#### 过滤搜索元素范围
> first()   返回被选元素中的首个元素            
> last()    返回被选元素中的最后一个元素            
> eq()  返回被选元素中带有指定索引号的元素          
> filter()  方法允许您规定一个标准。不匹配这个标准的元素会被从集合中删除，匹配的元素会被返回。          
> not() 返回不匹配的所有元素            

### jQuery AJAX

#### load()方法
> load() 方法从服务器加载数据，并把返回的数据放入被选元素中。           
```
$(selector).load(URL,data,callback);
```
> 必需的 URL 参数规定您希望加载的 URL。             
> 可选的 data 参数规定与请求一同发送的查询字符串键/值对集合。           
> 可选的 callback 参数是 load() 方法完成后所执行的函数名称。            

> 可选的 callback 参数规定当 load() 方法完成后所要允许的回调函数。回调函数可以设置不同的参数：
* responseTxt - 包含调用成功时的结果内容
* statusTXT - 包含调用的状态
* xhr - 包含 XMLHttpRequest 对象

#### get() 和 post() 方法

#### $.get()
> $.get() 方法通过 HTTP GET 请求从服务器上请求数据          
```
$.get(URL,callback);
```
> 必需的 URL 参数规定您希望请求的 URL。         
> 可选的 callback 参数是请求成功后所执行的函数名,第一个回调参数存有被请求页面的内容，第二个回调参数存有请求的状态           

#### $.post()   
> $.post() 方法通过 HTTP POST 请求从服务器上请求数据            
```
$.post(URL,data,callback);
```
> 必需的 URL 参数规定您希望请求的 URL。         
> 可选的 data 参数规定连同请求发送的数据。          
> 可选的 callback 参数是请求成功后所执行的函数名,第一个回调参数存有被请求页面的内容，而第二个参数存有请求的状态         

### noConflict() 方法
> noConflict() 方法会释放会 $ 标识符的控制，这样其他脚本就可以使用它了              
> 创建自己的简写            
```
let jq = $.noConflict()
jq(document).ready(function(){

})
```
> 如果不愿意改变这个快捷方式，那么您可以把 $ 符号作为变量传递给 ready 方法。这样就可以在函数内使用 $ 符号了 - 而在函数外，依旧不得不使用 "jQuery"           
```
$.noConflict();
jQuery(document).ready(function($){
  $("button").click(function(){
    $("p").text("jQuery 仍在运行！");
  });
});
```

###　jQuery 事件
> bind()	向匹配元素附加一个或更多事件处理器          
> blur()	触发、或将函数绑定到指定元素的 blur 事件            
> change()	触发、或将函数绑定到指定元素的 change 事件          
> click()	触发、或将函数绑定到指定元素的 click 事件           
> dblclick()	触发、或将函数绑定到指定元素的 double click 事件            
> delegate()	向匹配元素的当前或未来的子元素附加一个或多个事件处理器          
> die()	移除所有通过 live() 函数添加的事件处理程序。            
> error()	触发、或将函数绑定到指定元素的 error 事件           
> event.isDefaultPrevented()	返回 event 对象上是否调用了 event.preventDefault()。            
> event.pageX	相对于文档左边缘的鼠标位置。            
> event.pageY	相对于文档上边缘的鼠标位置。            
> event.preventDefault()	阻止事件的默认动作。            
> event.result	包含由被指定事件触发的事件处理器返回的最后一个值。          
> event.target	触发该事件的 DOM 元素。         
> event.timeStamp	该属性返回从 1970 年 1 月 1 日到事件发生时的毫秒数。            
> event.type	描述事件的类型。            
> event.which	指示按了哪个键或按钮。          
> focus()	触发、或将函数绑定到指定元素的 focus 事件           
> keydown()	触发、或将函数绑定到指定元素的 key down 事件            
> keypress()	触发、或将函数绑定到指定元素的 key press 事件           
> keyup()	触发、或将函数绑定到指定元素的 key up 事件          
> live()	为当前或未来的匹配元素添加一个或多个事件处理器          
> load()	触发、或将函数绑定到指定元素的 load 事件            
> mousedown()	触发、或将函数绑定到指定元素的 mouse down 事件          
> mouseenter()	触发、或将函数绑定到指定元素的 mouse enter 事件         
> mouseleave()	触发、或将函数绑定到指定元素的 mouse leave 事件         
> mousemove()	触发、或将函数绑定到指定元素的 mouse move 事件          
> mouseout()	触发、或将函数绑定到指定元素的 mouse out 事件           
> mouseover()	触发、或将函数绑定到指定元素的 mouse over 事件          
> mouseup()	触发、或将函数绑定到指定元素的 mouse up 事件            
> one()	向匹配元素添加事件处理器。每个元素只能触发一次该处理器。            
> ready()	文档就绪事件（当 HTML 文档就绪可用时）          
> resize()	触发、或将函数绑定到指定元素的 resize 事件          
> scroll()	触发、或将函数绑定到指定元素的 scroll 事件          
> select()	触发、或将函数绑定到指定元素的 select 事件          
> submit()	触发、或将函数绑定到指定元素的 submit 事件          
> toggle()	绑定两个或多个事件处理器函数，当发生轮流的 click 事件时执行。           
> trigger()	所有匹配元素的指定事件          
> triggerHandler()	第一个被匹配元素的指定事件          
> unbind()	从匹配元素移除一个被添加的事件处理器            
> undelegate()	从匹配元素移除一个被添加的事件处理器，现在或将来            
> unload()	触发、或将函数绑定到指定元素的 unload 事件          

### jQuery 效果函数
> animate()	对被选元素应用“自定义”的动画            
> clearQueue()	对被选元素移除所有排队的函数（仍未运行的）          
> delay()	对被选元素的所有排队函数（仍未运行）设置延迟            
> dequeue()	运行被选元素的下一个排队函数            
> fadeIn()	逐渐改变被选元素的不透明度，从隐藏到可见            
> fadeOut()	逐渐改变被选元素的不透明度，从可见到隐藏            
> fadeTo()	把被选元素逐渐改变至给定的不透明度          
> hide()	隐藏被选的元素          
> queue()	显示被选元素的排队函数          
> show()	显示被选的元素          
> slideDown()	通过调整高度来滑动显示被选元素          
> slideToggle()	对被选元素进行滑动隐藏和滑动显示的切换          
> slideUp()	通过调整高度来滑动隐藏被选元素          
> stop()	停止在被选元素上运行动画            
> toggle()	对被选元素进行隐藏和显示的切换          
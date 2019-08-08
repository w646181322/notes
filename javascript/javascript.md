### 字符串方法

> indexOf(str(,index)) 返回字符串中指定文本首次出现的索引(位置),未找到则返回-1，可接受第二参数作为检索起始位置         
> lastIndexOf(str(,index))  返回指定文本在字符串这种最后一次出现的索引，未找到则返回-1，可接受第二参数作为检索起始位置          
> search(str)  搜索特定值的字符串，并返回匹配的位置             

> slice(start,end)  提取字符串的某个部分并在新字符串中返回被提取的部分，省略第二参数将提取剩余的部分(负值不适用ie8之前的版本)          
> substring(start,end)  同slice(),但无法接受负的索引            
> substr(start,length) 类似于slice()，但第二参数为被提取部分的长度        

> replace(str1,str2) 用另一个值替换在字符串中指定的值,str2替换str1,该方法对大小写敏感          
> toUpperCase() 把字符串转换为大写          
> toLowerCase() 把字符串转化为小写
> concat()  连接两个或多个字符串            
> String.trim() 删除字符串两端的空白符             

> charAt()  返回字符串中指定下标的字符串            
> charCodeAt()  返回字符串中指定索引的字符 unicode 编码         

> split()   将字符串转换为数组              

### 数字的方法和属性
> toString()    以字符串返回数值                
> toExponential()   返回字符串值，它包含已被四舍五入并使用指数计数法的数字，参数定义小数点后的字符数 ,参数可选           
> toFixed() 返回字符串值，它包含了指定位数小数的数字            
> toPrecision() 返回字符串，它包含了指定长度的数字          
> valueOf() 以数值返回数值              
#### 全局方法
> Number()  可用与把JavaScript变量转化为数值，返回数值
> parseFloat()  解析一段字符串并返回数值，允许空格，只返回首个数字          
> parseInt()    解析一段字符串并返回数值，允许空格，只返回首个数字
#### 数值属性
> MAX_VALUE	返回 JavaScript 中可能的最大数。                
> MIN_VALUE	返回 JavaScript 中可能的最小数。                
> NEGATIVE_INFINITY	表示负的无穷大（溢出返回）。                
> NaN	表示非数字值（"Not-a-Number"）。                
> POSITIVE_INFINITY	表示无穷大（溢出返回）。                
>> 数值属性不可用于变量，只能作为 Number.MAX_VALUE 访问         

### 数组方法
> toString()    把数组转换为数组值(逗号分隔)的字符串            
> join()    方法也可将所有数组元素结合为一个字符串          
> pop() 方法从数组中删除最后一个元素,返回被删除的值            
> push()    方法（在数组结尾处）向数组添加一个新的元素，返回新数组的长度          
> shift()   方法会删除首个数组元素，并把所有其他元素“位移”到更低的索引，返回被删除的值          
> unshift() 方法（在开头）向数组添加新元素，并“反向位移”旧元素，返回新数组的长度          
>> delete arr[i]            
>> delete 运算符也可以删除数组中的元素，但会在数组中留下未定义的空洞            

> splice(index,len(,elements))   移除数组元素，并添加新项           
>> 参数1：定义了移除元素或添加新元素的位置，            
>> 参数2：定义了应删除多少元素          
>> 参数3：可选，定义要添加的新元素          

> concat()  方法通过合并（连接）现有数组来创建一个新数组,不改变原数组，返回一个新数组            
> slice()   法用数组的某个片段切出新数组,不改变原数组，返回一个新数组               
#### 数组的排序
> sort()    方法以字母顺序对数组进行排序,默认按照字符串顺序，若排序数字需添加一个比值函数            
> reverse() 方法反转数组中的元素            
#### 数组迭代方法
> Array.forEach()   方法为每个数组元素调用一次函数（回调函数）          
>> 方法接受3参数：项目值，项目索引，数组本身            

> Array.map()   方法通过对每个数组元素执行函数来创建新数组,方法不会对没有值的数组元素执行函数,方法不会更改原始数组          
>> 方法接受3参数：项目值，项目索引，数组本身            

> Array.filter()     方法创建一个包含通过测试的数组元素的新数组         
>> 方法接受3参数：项目值，项目索引，数组本身            

> Array.reduce()    方法在每个数组元素上运行函数，以生成（减少它）单个值,方法在数组中从左到右工作。另请参见 reduceRight（）,方法不会减少原始数组            
>> 方法接受4参数：总数(初始值/先前返回的值)，项目值，项目索引，数组本身             
> Array.every() 方法检查所有数组值是否通过测试          
>> 方法接受3参数：项目值，项目索引，数组本身            

> Array.some()  方法检查某些数组值是否通过了测试            
>> 方法接受3参数：项目值，项目索引，数组本身            

> indexOf() 方法在数组中搜索元素值并返回其位置,未找到则返回-1          
> lastIndexOf() 数组结尾开始搜索，未找到则返回-1            
> find()     方法返回通过测试函数的第一个数组元素的值           
>> 方法接受3参数：项目值，项目索引，数组本身            
> findIndex()   方法返回通过测试函数的第一个数组元素的索引          
>> 方法接受3参数：项目值，项目索引，数组本身            

### javascript 日期
#### 创建新的日期对象方法
> new Date()    用当前日期和时间创建新的日期对象            
> new Date(year,month,day,hours,minutes,seconds,milliseconds)   用指定日期和时间创建新的日期对象,7个数字分别指定年、月、日、小时、分钟、秒和毫秒（按此顺序）           
> new Date(millisecondes)   创建一个零时加毫秒的新日期对象              
> new Date(date string) 从日期字符串创建一个新的日期对象         
>> toUTCtring() 方法将日期转换为 UTC 字符串（一种日期显示标准）         
>> toDateString()   方法将日期转换为更易读的格式

#### 日期获取
> getDate()	以数值返回天（1-31）            
> getDay()	以数值获取周名（0-6）           
> getFullYear()	获取四位的年（yyyy）            
> getHours()	获取小时（0-23）            
> getMilliseconds()	获取毫秒（0-999）           
> getMinutes()	获取分（0-59）          
> getMonth()	获取月（0-11）          
> getSeconds()	获取秒（0-59）          
> getTime()	获取时间（从 1970 年 1 月 1 日至今）            

#### 日期设置
> setDate()	以数值（1-31）设置日            
> setFullYear()	设置年（可选月和日）            
> setHours()	设置小时（0-23）            
> setMilliseconds()	设置毫秒（0-999）           
> setMinutes()	设置分（0-59）          
> setMonth()	设置月（0-11）          
> setSeconds()	设置秒（0-59）          
> setTime()	设置时间（从 1970 年 1 月 1 日至今的毫秒数）            

#### UTC 日期方法
> getUTCDate()	等于 getDate()，但返回 UTC 日期         
> getUTCDay()	等于 getDay()，但返回 UTC 日            
> getUTCFullYear()	等于 getFullYear()，但返回 UTC 年           
> getUTCHours()	等于 getHours()，但返回 UTC 小时            
> getUTCMilliseconds()	等于 getMilliseconds()，但返回 UTC 毫秒         
> getUTCMinutes()	等于 getMinutes()，但返回 UTC 分            
> getUTCMonth()	等于 getMonth()，但返回 UTC 月          
> getUTCSeconds()	等于 getSeconds()，但返回 UTC 秒            

### Math 对象
> Math.round()  返回值是 x 四舍五入为最接近的整数           
> Math.pow()    返回值是 x 的 y 次幂            
> Math.sqrt()   返回x 的平方根          
> Math.abs()    返回x 的绝对（正）值            
> Math.ceil()   返回值是 x 上舍入最接近的整数               
> Math.floor()  返回值是 x 下舍入最接近的整数           
> Math.sin()    返回角 x（以弧度计）的正弦（介于 -1 与 1 之间的值）         
> Math.cos()    返回角 x（以弧度计）的余弦（介于 -1 与 1 之间的值）         
> Math.min()/Math.max() 可用于查找参数列表中的最低或最高值          
> Math.random() 返回介于 0（包括） 与 1（不包括） 之间的随机数          



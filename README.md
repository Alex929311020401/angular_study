# angular_study
官网地址：https://angularjs.org/  
angular版本  
 v1.2及以下  
 v1.3及以上（主流）  
 v2.x（写法不同,TypeScript ）  
 v4.x（one framework mobile & desktip.一套代码搞定移动端和桌面应用）  
 cdn https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.js

**MVC**  
M modal 模型 -- 数据  
V view  视图 -- 表现层  
C controller 控制层 -- 业务逻辑
缺点： M ---V  耦合度高   C 臃肿

**MVP**  
P presenter 主持人 v -- p -- m --p -- v
有点：M --- V 没有直接耦合
缺点：P --- 超级臃肿

**MVVM**  
VM viewModel  视图层 + 数据层  
M --- V 没有耦合

双向数据绑定  数据改变 <---> 视图变化
ng-modal  双向数据绑定
ng-bind   输出（数据 --> 视图）
ng-app    范围  

**angular 核心是数据**
angular {{表达式}}
ng-init 初始化 给数据初始值

指令：1、系统指令；2、自定义指令

数据循环 ng-repeat  
1、数字数组数据重复 报错  
    angular 出于性能考虑  数据 <---> 元素对应   key：数字数组，数组中数字做key   
    $index 是angular 内针对ng-repeat提供的隐含index变量名称，如果在ng-repeat嵌套使用时，index名称会发生冲突及覆盖。这是也应该使用自定义的变量名。   
    item in arr track by $index  
2、json数组数据重复 不报错  
    [1,2,3] == [1,2,3] //false   
    new Array(1,2,3) == new Array(1,2,3) 对象  
3、ng-repeat = "(k,v) in json"  


angular 环境 和 js 环境 默认不互通
ng空间 与 js空间  

ng-click angular click 事件   
push数组结尾添加  unshift数组头添加    返回数组长度 
pop数组结尾删除  shift数组开头删除     返回删除数据

**模块化**
1、写模块  angular.modal(名字，[依赖])  
2、用模块  ng-app="名字"

**controller**  
controller 不能独立存在  属于某一个模块  



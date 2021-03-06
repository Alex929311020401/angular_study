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
    函数结尾有一个 检查语句 $scope.$apply();     
    异步时 先执行检查     $scope 改变没有正确监听   
    合理不合理都出于性能考虑

**scope**
1、$scope本身是一个普通的JavaScript对象  
2、$scope是一个表达式的执行环境    
3、angular 的作用域

AngularJS中，一个scope跟一个元素关联（以及所有它的子元素），而一个元素不是必须直接跟一个scope关联。元素通过以下三中方式被分配一个scope：  
1、scope通过controller或者directive创建在一个element上（指令不总是引入新的scope）  
    `<nav ng-controller='menuCtrl'>`  
2、如果一个scope不存在于元素上，那么它将继承它的父级scope  
    `<nav ng-controller='menuCtrl'><a ng-click='navigate()'>Click Me!</a></nav>`  
3、如果一个元素不是某个ng-app的一部分，那么它不属于任何scope。  


angular特性：  
**双向数据绑定**
    ng-modol  $scope <---> html   
    数据更新，视图自动更新

**依赖注入**    
    函数定义决定参数  
    $scope 、$http 、$timeout 依赖项  


**函数**  
    被动接受参数

**脏检查**




# CXUI 全局样式说明文档

## 布局
.container   设置为容器，规格：水平方向居中，宽度为100%，左右内边距为15px，没有高度
.container-fluid   设置为容器，规格：水平方向居中，宽度为100%，没有外边距，左右内边距为15px，上下为0px,没有高度

## 按钮 cx-btn
   ### 普通的按钮样式
   成功  cx-btn-success
   失败  cx-btn-fail
   警告  cx-btn-warning
   错误  cx-btn-error
   取消  cx-btn-cancel
   确认  cx-btn-sure
   默认  cx-btn-default
   危险  cx-btn-danger
   首选  cx-btn-primany
   一般信息 cx-btn-imfo
   禁止  cx-btn-disable
   百搭  cx-btn-normal
   暖色  cx-btn-warm

-型号
   大  cx-btn-bg
   小  cx-btn-sm
   中  cx-btn-md

-圆纽按钮
       cx-btn-radius

### 渐变的按钮样式
   成功  cx-btn-success-rgb
   失败  cx-btn-fail-rgb
   警告  cx-btn-warning-rgb
   错误  cx-btn-error-rgb
   取消  cx-btn-cancel-rgb
   确认  cx-btn-sure-rgb
   默认  cx-btn-default-rgb
   危险  cx-btn-danger-rgb
   首选  cx-btn-primany-rgb
   一般信息 cx-btn-imfo-rgb
   禁止  cx-btn-disable-rgb
   百搭  cx-btn-normal-rgb
   暖色  cx-btn-warm-rgb


### 伪类按钮样式
    cx-btn-radius

## 滑块

## select选择框

## 表单



## 规范
1.清空所有Html标签默认样式

2.字体标准：最小12px 最大36px 默认14px


3.布局：栅格系统（给一个父容器等分多少份）
        12份-将元素分为多少列
        每个子元素可以站12份中站1-12份中的任意一份
        col-12：表示占据12份

### 表格 .cx-table
.cx-table  表格基础类：表格元素要在cx-table中使用
.cx-table-column 半边框
.cx-table-striped 条状表格：表格偶数行有一定背景颜色
.cx-table-hover   悬浮表格
.cx-table-condensed 紧缩样式
.cx-table-border 边框表格
.cx-table-inverse 背景色为黑色的表格
.cx-table-inverse-striped 黑色条形
.cx-table-inverse-hover   黑色悬浮 需要依赖 .cx-table-inverse 或 .cx-table-inverse-striped
.cx-table-control 表示【控制列】固定，其他列可以滚动 .cx-table-control必须给table的祖籍元素添加，而不能给父元素添加  .cx-table-box 表示table的父容器
~~~css
.cx-table-control{
   position:relative;
}
.cx-table-control table>tr>td:last-child{
   position:absolute;
   right:0;
   min-width:120px;
   text-align:center;
   box-shadow:-5px 4px 6px 1px #ccc;
}
.cx-table-control table>tr>td:nth-last-child(2)::before{
   content:"";
   width:0;
}
.cx-table-control>.cx-table-box{
   overflow:hidden;
}

.cx-table-responsive 移动端表格：可以有横向滚动的效果
                     .cx-table-responsive 需要给.cx-table的父元素添加
状态表格：给tr添加类名
.success 成功
.info    通过
.warning 警告
.danger  危险
.primary 首选
.warm    暖色

### 分页  .cx-page
.cx-pagination 实现分页样式 由ul li a 完成的分页效果
.cx-pagination-bgc 带有颜色的分页样式
.cx-pagination-noBgc 表示没有背景颜色的分页

### 表单类 
#### 单选框多选框样式
.circle-check  圆形选择框      .circle-check需要给input[type=checkbox]的父元素添加
.square-check  正方形选择框    .square-check需要给input[type=checkbox]的父元素添加
/* 示例代码 */
~~~html
    <div class="circle-check">
        <input type="checkbox">
    </div>
    <div class="square-check">
        <input type="checkbox">
    </div>
~~~
#### 滑块 .sliderBar
.sliderBar-box 表示滑块外围的容器
.sliderBar 滑块条
.sliderBar-control 滑块控制键
~~~html
    <div class="sliderBar-box">
        <div class="sliderBar">
            <div class="sliderBar-control">
                <span class="progress-num">55</span>
            </div>
        </div>
    </div>
~~~
状态
.sliderBar-success  绿色
.sliderBar-info     浅蓝
.sliderBar-primary  深蓝
.sliderBar-error    灰色
.sliderBar-warm     黄色
.sliderBar-warning  橘色
.sliderBar-danger   红色
.sliderBar-

### 开关 .switch
.switch 开关样式的选择框 需要给 input[type=checkbox] 添加类名 class="switch"才能生效
        绿色为开 input=checked，灰色为关 input=disable
状态
.switch-info       蓝开 灰关
.switch-danger     红开 灰关
.switch-warm       橙开 灰关
.switch-primary    蓝开 红关

###  步骤组件 .step
.step-wrap 外部容器 55rem
.step-full 表示每个步骤容器 包含内容【圈  线  文本】
.step 具体进行的每一步，用Input[type=checkbox]，当有 checked 属性表示当前步骤已完成
.step-circle 表示圆
.step-line   表示 线
.step-text   表示文本

状态
.step-circle-info
.step-circle-success
.step-circle-primary
.step-circle-warm
.step-circle-error
step-circle-danger

### 导航 cx-nav
注意：导航仅仅适用于PC端，且只适用于静态样式，导航中所有的样式都是操作li下的a标签设置
.cx-nav-tab 表示像tab样式大的导航条 需要依赖基础样式(cx-nav)
.cx-nav-pills 胶囊式导航  需要依赖基础样式(cx-nav)
.cx-nav-stacked 

.cx-nav-inverse 背景色为黑色的导航
.cx-nav-aside 表示侧边栏导航
.cx-av-fixed-top 表示固定导航，在顶部
.cx-nav-fix-left 表示固定导航 在左部
.cx-nav-fix-right 表示固定导航 在右部
### 导航条 .cx-navBar
注意：兼容移动端
.cx-narBar 导航条 兼容移动 默认样式【隐藏】
 兼容移动端样式设置规则：媒体查询最小宽度；写pc端样式；当小于这个宽度时候；使用浏览器默认样式
 网站的导航条；到移动端时候可以折叠 
.cx-navbar-default 给导航条添加样式【背景色】
.cx-navbar-header 有媒体查询样式；做PC 端和移动端区分； 移动端宽度100%
.collapse  元素隐藏[移动端]
.cx-nav-collapse.collapse 在pc 端【强制】显示
.cx-navbar-nav 表示导航条下导航
.cx-navbar-form 表示导航条中输入框
.cx-navbar-left 让导航在导航条中左浮动【移动端无浮动】
.cx-navbar-right 让导航有又浮动【移动端无浮动效果】
.cx-navbar-toggle 表示显示隐藏列表导航栏，有【右浮动】效果

.cx-navbar-fixed-top 固定顶部导航条
.cx-navbar-inverse 黑色导航条 border-bottom:1px solid black
   .cx-navbar .active  背景颜色黑色  字体白色

 .breadcrumb 表示路径导航；没有基础类  

  - 每个a 添加伪元素； content:"Z/\00a0" 

### 表单样式组件
1.本组件包含表单基础样式和可选择样式，如有特殊需要，请自定义
2.表单没有进行验证处理，有对验证效果样式处理：static状态
3.表单验证需要使用JS正则完成。
  PS：正则规则只能写基础样式不可写新的正则（IE和部分Firefox不兼容新正则）

#### 表单组件基础样式：
.form-group 表示表单组件
.form-control 表示表单控件
.form-lable 表示input提示信息，只能应用在lable标签中
#### 表单组件可选样式
.form-inline 横向表单
.form-horizontal 纵向表单

#### 表单控件
.form-check 选择项组件，在ul中使用
.form-check-item 多选项，在li中使用
.check-content 表示 选择的文本描述

### 栅格系统 .col
栅格系统是横向布局的处理
提示信息：如果父容器非.row 那么所有使用的栅格都将没有高度，需您自己计算父容器高度，清除浮动
#### 容器 .row
将.row等分为12份

#### 屏幕
.col-xs-xx   小于768px
.col-sm-xx   大于等于768px
.col-md-xx   大于等于992px
.col-lg-xx   大于等于1200px

#### 分的分数（保留小数点后七位）
1份  8.3333333%
2份  16.6666667%
3份  25%
4份  33.3333333%
5份  41.6666667%
6份  50%
7份  58.3333333%
8份  66.6666667%
9份  75%
10份 83.3333333%
11份 91.6666667%
12份 100%

#### 列偏移
原理：通过改变position：relative; Left 来实现列偏移
<!-- *表示数字1-12 -->
.col-xs-offset-*
.col-sm-offset-*
.col-md-offset-*
.col-lg-offset-*

#### 排列
.co1-xs-pull-*  相对元素位置右边多远
.co1-sm-pull-*
.co1-md-pull-*
.co1-lg-pull-*

### 开发浏览器注意事项
1.如果您是IE7 8 请您更换浏览器
2. IE7 尽量使用 div 列如
   ul div-ul
   li div-li
   span div.span 设置display:inline;
3.IE7 8不支持浮动 清除浮动 css3绝大部分属性

## Jquery 层次选择器

选择器 | 描述
------------ | -------------
$("ancestor descendant") | 选取ancestor元素里所有的descendant(后代)元素
$("parent>child") | 选取parent元素下的子元素
$("prev+ next") | 选取紧接在prev元素后的next元素，等同于$("prev").next("xxx")
$("prev~siblings") | 选取prev元素后面的所有同辈元素，不包括自己，等同于$("#prev").nextAll("xxx")

## 过滤选择器
1. 基本过滤选择器


选择器 | 描述
------------ | -------------
 :first | 选取第一个元素
 :last | 选取最后一个元素
 :not(selector) | 去除所有与给定选择器匹配的元素
 :even | 选取索引是偶数的所有元素，索引从0开始
 :odd | 选取索引是奇数的所有元素，索引从0开始
 :eq(index) | 选择索引等于index的元素
 :gt(index) | 选取索引大于index的元素(index从0开始)
 :lt(index) | 选取索引小于index的元素(index从0开始)
 :header | 选取所有的标题如h2,h2...
 :animated | 选取正在执行动画的所有元素
 :focus | 选取当前获取焦点的元素

2. 内容过滤选择器

选择器 | 描述
------------ | -------------
 :contains(text) | 选取内容含有"text"的元素
 :empty | 选择不包含子元素或者文本的空元素
 :has(selector) | 选取含有选择器所匹配的元素的元素
 :parent | 选取含有子元素或者文本的元素
 
3. 可见性过滤选择器

选择器 | 描述
------------ | -------------
 :hidden | 选取所有不可见的元素
 :visible | 选择所有可见的元素

4. 属性过滤选择器

选择器 | 描述
------------ | -------------
 [attribute] | 选取拥有此属性的元素
 [attribute=value] | 选取属性的值为value的元素
 [attribute!=value] | 选取属性的值不等于value的元素
 [attribute^=value] | 选取属性的值以value开始的元素
 [attribute$=value] | 选取属性的值以value结束的元素
 [attribute*=value] | 选取属性的值含有value的元素
 [attribute|=value] | 选取属性的值等于给定字符串或以该字符串为前缀（该字符串后跟一个连字符“_"）的元素
 [attribute~=value] | 选取属性用空格分隔的值中包含一个给定值的元素
 [attribute]  [attribute2]  [attributeN]| 用属性选择器合并成一个复合属性选择器，

5. 子元素过滤选择器

选择器 | 描述
------------ | -------------
 :nth-child(index/even/odd/equation) | 选取每个父元素下的第index个子元素或者奇偶元素(index从1算起)
 :first-child | 选取每个父元素的第一个子元素
 :last-child | 选取每个父元素最后一个子元素
 :only-child | 如果某个元素是它父元素中惟一的子元素，那么将会匹配

6. 表单对象属性过滤选择器

选择器 | 描述
------------ | -------------
 :enabled | 选取所有可用元素
 :disabled | 选取所有不可用元素
 :checked | 选取所有被选中的元素（单选框，复选框）
 :selected | 选取所有被选中的选项元素（下拉列表）

## 表单选择器

选择器 | 描述
------------ | -------------
 :input | 选取所有的<input><textarea><select>和<button>元素
 :text | 选取所有的单行文本框
 :password | 选取所有的密码框
 :radio | 选取所有的单选框
 :checkbox | 选取所有的复选框
 :submit | 选取所有的提交按钮
 :image | 选取所有的图像按钮
 :reset | 选取所有的重置按钮
 :button | 选取所有的按钮
 :file | 选取所有的上传域
 :hidden | 选取所有不可见的元素

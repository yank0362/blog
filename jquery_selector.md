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

3. 可见性过滤选择器

4. 属性过滤选择器

5. 子元素过滤选择器

6. 表单对象属性过滤选择器

## 表单选择器

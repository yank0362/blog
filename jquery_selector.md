## Jquery 层次选择器

选择器 | 描述
------------ | -------------
$("ancestor descendant") | 选取ancestor元素里所有的descendant(后代)元素
$("parent>child") | 选取parent元素下的子元素
$("prev+ next") | 选取紧接在prev元素后的next元素，等同于$("prev").next("xxx")
$("prev~siblings") | 选取prev元素后面的所有同辈元素，不包括自己，等同于$("#prev").nextAll("xxx")

## 过滤选择器
1. 基本过滤选择器

2. 内容过滤选择器

3. 可见性过滤选择器

4. 属性过滤选择器

5. 子元素过滤选择器

6. 表单对象属性过滤选择器

## 表单选择器

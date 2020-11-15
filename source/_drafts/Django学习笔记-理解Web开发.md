---
title: Django学习笔记-理解Web开发
date: 2020-09-25 16:17:49
tags:
- web
- python
categories: Django
---

### template

模板，实现后端数据到前端显示。简单的语法如下：

~~~html
<h1>{{ question.question_text }}</h1>
<ul>
{% for choice in question.choice_set.all %}
    <li>{{ choice.choice_text }}</li>
{% endfor %}
</ul>
~~~

### DOM

Document Object Model，文档对象类型。将HTML文件抽象成一个对象，并提供API给Script或者编程语言。示例：

~~~html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
</head>
<body>
<script>
function changeImage()
{
	element=document.getElementById('myimage')
	if (element.src.match("bulbon"))
	{
		element.src="/images/pic_bulboff.gif";
	}
	else
	{
		element.src="/images/pic_bulbon.gif";
	}
}
</script>
<img id="myimage" onclick="changeImage()" border="0" src="/images/pic_bulboff.gif" width="100" height="180">
<p>点击灯泡 开/关 灯</p>

</body>
</html>
~~~


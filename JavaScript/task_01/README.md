## 绑定元素的几种方法
#### getElementById()方法
 - 返回对拥有指定 ID 的第一个对象的引用。
 - 语法：`document.getElementById(id)`

#### getElementsByName()方法
 - 返回带有指定名称的节点对象的集合。
 - 语法：`document.getElementsByName(name)`
 - **注意**：      
  （1）因为文档中的 name 属性可能不唯一，所有 getElementsByName() 方法返回的是元素的数组，而不是一个元素。      
  （2）和数组类似也有length属性，可以和访问数组一样的方法来访问，从0开始。

#### getElementsByTagName()方法
  - 返回带有指定标签名的节点对象的集合。返回元素的顺序是它们在文档中的顺序。
  - 语法：`document.getElementsByTagName(Tagname)`
  - 说明：      
    （1）Tagname是标签的名称，如p、a、img等标签名。      
    （2）和数组类似也有length属性，可以和访问数组一样的方法来访问，从0开始。


#### 区别getElementByID,getElementsByName,getElementsByTagName
 - 以人来举例说明：       
  （1）ID 是一个人的身份证号码，是唯一的。所以通过getElementById获取的是指定的一个人。       
  （2） Name 是他的名字，可以重复。所以通过getElementsByName获取名字相同的人集合。       
  （3） TagName可看似某类，getElementsByTagName获取相同类的人集合。如获取小孩这类人，getElementsByTagName("小孩")。

#### querySelector()方法
  - 语法：`document.querySelector("#id");`
  - 说明： 指定一个或多个匹配元素的 CSS 选择器。 可以使用它们的 id, 类, 类型, 属性, 属性值等来选取元素。
  - **注意**：       
    （1）`querySelector()` 方法不仅可以匹配id，还可以匹配类, 类型, 属性, 属性值。         
    （2）`querySelector()` 方法仅仅返回匹配指定选择器的第一个元素。如果需要返回所有的元素，请使用 `querySelectorAll() `方法替代。

***

## 获取某个元素内容的几种方法
#### textContent
  - 设置或返回指定节点的文本内容，以及它的所有后代。如果设置了 textContent 属性，会删除所有子节点，并被替换为包含指定字符串的一个单独的文本节点。

#### innerHTML
  - 用来设置或是获取某个元素内所有元素及内容，包括子元素。当内容都是文本的时候，可以把这个属性当做textContent属性来用。

#### outerHTML
  - outerHTML和innerHTML很像，它们的唯一区别就是outerHTML包括自身元素而innerHTML不包括自身元素。

#### nodeValue
  - 设置或返回指定节点的节点值。nodeValue 属性的替代选择是 textContent 属性。

#### outerText
  - 这个outerText和outerHTML有同样的功能它们都包括自身，不同的是outerText获取的是元素内容，而outerHTML获取到的内容包括元素。它能做的事，textContent、innerText和innerHTML都可以做。

#### value：
  - 属性可设置或返回密码域的默认值。获取文本框的值

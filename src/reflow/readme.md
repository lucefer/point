##演示强制reflow
众所周知，js操作dom的一些样式或者属性时，会触发浏览器的强制回流，这对web应用性能产生影响，所以我们要避免使用一些引起强制回流的操作。

本例对引起强制回流的属性和方法进行可视化演示。

引起dom强制回流的
####属性：
offsetWidth,offsetHeight,offsetLeft,offsetTop
scrollWidth,scrollHeight,scrollLeft,scrollTop

####方法：
var style=getComputedStyle/currentStyle
但是这个方法有一点要注意，仅仅执行这句代码是不会引起强制回流。
只有在方法之后，进行style的读取，方可触发回流。

####样式：
通过dom.style.XX进行读取样式，是不会触发强制回流的。
本例仅仅通过width和height进行了验证。

点击查看[示例](http://lucefer.github.io/point)

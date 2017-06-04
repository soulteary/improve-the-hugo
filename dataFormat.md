# DateFormat

Hugo 时间格式化采用golang的format函数，并且在程序内部内置了dateFormat函数来帮助用户格式化时间。

这个对于英文用户没有什么问题，但是对于CJK用户来说就不是那么友好了。

使用printv打印Date对象，发现对象是以ms保存在内存中的，不可以直接包装一个时间展示的html模版片段解决问题，也不能将内置函数拼合在一起，实现时间的转换。

于是扩展了pure-hugo-data-bridge，在Params中添加了dateForChinese字段，稍后将工具单独抽象出来使用吧。


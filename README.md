# 解析异步消息处理机制
### Android中的异步消息处理主要由4个部分组成：Message、Handler、MessageQueue和Looper
>* <strong>Message</strong></br>
>Message在线程之间传递的信息，它可以在内部携带少量的信息，用于在不同线程之间交换数据。在代码中我们使用到了Message的what字段，除此之外，还可以使用argl和arg2字段来携带一些整型数据，使用obj字段携带一个Object对象。
>* <strong>Handler</strong></br>
>Handler顾名思义就是处理者的意思，它主要是用于发送和处理消息的。发送消息一般是使用Handler的sendMessage()方法，而发出的消息经过一系列地辗转处理之后，最终会传递到Handler的handleMessage()方法中。

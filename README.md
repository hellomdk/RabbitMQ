# RabbitMQ
本文参考博客https://blog.csdn.net/hellozpc/article/details/81436980#57_673<br>
设计了三种模式（实际上四种模式，主题模式没做演示）<br>
1.work模式<br>
  ①一个生产者，多个消费者，公平分配（采用轮训的方式）<br>
  ②一个生产者，多个消费者，能者多劳（修改消息确认方式）<br>
 <br>
2.订阅模式（实现消息的一对多发送）<br>
  一个生产者，多个消费者，发送中间加了路由转发<br>
  ①1个生产者，多个消费者<br>
  ②每个消费者都有自己的一个队列<br>
  ③生产者没有将消息直接发送到队列，而是发送到交换机<br>
  ④每个队列都要绑定到交换机<br>
  ⑤生产者发送的熊爱惜，经过交换机，到达队列，实现一个消息被多个小费制获取的目的<br>
 <br>
 3.路由模式<br>
  与订阅模式相比，多了key,也正因此实现了消息的定向发送与接收<br>
  
  
  


(1)测试类应该比待测试类的类优先写出来

(2)在待测试类的设计时，就应该写好测试类

(3)在测试类中，对于单个的类成员函数，测试时需要走三个步骤
一是在测试类中将参数传入函数
二是传出参数，传到测试类中
三是对传出参数的校验
以上三个步骤均在测试类中进行

(4)测试发生的一个流程：
测试类调用实体类函数，将参数传入实体类中处理
实体类对传入参数进行处理，然后将处理结果，传给测试类
测试类对实体类传过来的参数进行校验
校验正确则进行下一个函数的测试
直到所有函数测试完成后，测试结束

(5)待测试类中应有专门的调试宏，并且不影响实际编译，仅在测试的时候参加调试
可以定义一个专门的测试宏然后将调试加入待测类中，实际可以参考判断操作系统的宏

(6)后期可以增加一个内存检测工具，检测待测试类是否发生内存泄漏

(7)一个模型： 

待测类---转发接口(类的类型处理与数据的交互)

---
服务器

---
转发接口(只要数据，无关类的类型)---测试类
(补充)此时测试类与

(8)后期可以考虑可以对多种函数性能的测试

(9)待测试类的转发接口可以考虑自动生成代码










# experiment-4-2020
## 一、实验目的  
掌握Java中抽象类和抽象方法的定义;  
掌握Java中接口的定义，熟练掌握接口的定义形式以及接口的实现方法  
了解异常的使用方法，并在程序中根据输入情况做异常处理  
## 二、实验内容  
1、某学校为了给学生提供勤工俭学机会，也减轻授课教师的部分压力，准许博士研究生参与课程的助教工作。此时，该博士研究生有双重身份：学生和助教教师。  
2、设计两个管理接口：学生管理接口和教师管理接口。学生接口必须包括缴纳学费、查学费的方法；教师接口包括发放薪水和查询薪水的方法。  
3、设计博士研究生类，实现上述的两个接口，该博士研究生应具有姓名、性别、年龄、每学期学费、每月薪水等属性。（其他属性及方法，可自行发挥）。  
4、编写测试类，并实例化至少两名博士研究生，统计他们的年收入和学费。根据两者之差，算出每名博士研究生的年应纳税金额（国家最新工资纳税标准，请自行检索）。  

## 三、实验要求  
  
1、在 博士研究生类中实现各个接口定义的抽象方法;  
2、对年学费和年收入进行统计，用收入减去学费，求得纳税额；  
3、国家最新纳税标准（系数），属于某一时期的特定固定值，与实例化对象没有关系，考虑如何用static  final修饰定义。  
4、实例化研究生类时，可采用运行时通过main方法的参数args一次性赋值，也可采用Scanner类实现运行时交互式输入。  
5、根据输入情况，要在程序中做异常处理。  

## 四、实验过程  
根据实验要求，我在package中建立了三个class,分别是Student、Teacher、和Graduate这三个class。  
在Student类中使用抽象方法void setFee(double fee)  
在Teacher类中使用抽象方法void setPay(double pay)和void getPay(double pay)  
Graduate类首先引入了java.util.Scanner  
然后使用关键词implements使Graduate类实现接口类：public class Graduate implements Student,Teacher  
方法包括：
- 构造方法Graduate（String args）  

- 重写void setFee（double fee）  

- 重写void getFee（）  

- 重写int getPay（），研究生获得工资1500  

- 新增方法boolean isLoan（），判断是否需要交税（若年收入小于42000元则无需交税）  
使用try{
       }catch结构检查输入是否有误，如有误则报错并提醒  
## 五、程序运行截图  
![运行截图](https://raw.githubusercontent.com/FanJiahang/Experiment-3-2020/main/java_experiment_3.png)  
## 六、编程感想  
   
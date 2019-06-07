---
layout: post
title:  C++基础教程
date:   2019-06-07 14:00:00 +0800
categories: 博文
tag: 博文
---

* content
{:toc}

-------------------------------

# C++基础教程系列

---

---

---
## 第一期 面向对象基础

---

---
### 第一节 类与对象

---

#### 什么是对象？

<div style="width:18%;height:12%;"><img src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1559886109259&di=aacdabcbf8f6343cd9327084e57f4696&imgtype=0&src=http%3A%2F%2Fn.sinaimg.cn%2Feladies%2Ftransform%2F20170720%2FBHbo-fyihrit1005075.jpg" /></div>
<br/>

对象，顾名思义，就是你谈恋爱时，恋爱中的另一方。
没错！就是这样！

<div style="width:14%;height:12%;"><img src="https://ss3.bdstatic.com/70cFv8Sh_Q1YnxGkpoWK1HF6hhy/it/u=3513841257,685747986&fm=26&gp=0.jpg" /></div>
<br/>

好了好了，打住打住，就算你new一个Object()，你还是没有女朋友。

<div style="width:12%;height:12%;"><img src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1559886538127&di=1a7646cb9cc95414bcc099c7f50e3209&imgtype=0&src=http%3A%2F%2Fb-ssl.duitang.com%2Fuploads%2Fitem%2F201610%2F05%2F20161005105402_xiLsK.thumb.700_0.jpeg" /></div>
<br/>

扯远了，我们来看看对象到底是什么：
> 对象，是不以人的意志为转移而又与自我的存在通过感性确定性进行关联的客体事物，是简单的、直接性的存在、本质性的现实。在哲学上，对象是简单、直接的存在本质，具有现实的本质性，是知识的生成者，没有对象就没有知识。是感性确定性中必要的两个条件之一，另一条件则是自我，缺一不可。对象本身是存在的，它的存在不依附任何关系。
<div style="width:14%;height:12%;"><img src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1559887861732&di=4b13d3cc44c3ae90428d11797a44f833&imgtype=0&src=http%3A%2F%2F5b0988e595225.cdn.sohucs.com%2Fimages%2F20180416%2F33a6f4ad349145fca986b3306e0c60ed.jpeg" /></div>
<br/>

天鸭，这是啥玩意鸭，怎么看不懂鸭！
<div style="width:100%;height:12%;"><img src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1559888001033&di=b8f2e6d0a8342a96c5e573b2cc5fa18a&imgtype=0&src=http%3A%2F%2Fimg.smzy.com%2Fimges%2F2018%2F1027%2F20181027023758807.png" /></div>
<br/>

好吧好吧，刚刚拿错剧本了，在计算机中：
> 对象就是客观世界中存在的人、事、物体等实体在计算机逻辑中的映射。
<div style="width:49%;height:12%;"><img src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1559888321006&di=fed078a186c5e14cc6c94ab403969eb5&imgtype=0&src=http%3A%2F%2Fimg.mp.itc.cn%2Fupload%2F20170625%2F70e5fce9e1024728b866aaf36a6a9675_th.jpg" /></div>
<br/>

百度百科中，面向对象释义如下：
> 面向对象(Object Oriented,OO)是软件开发方法。面向对象的概念和应用已超越了程序设计和软件开发，扩展到如数据库系统、交互式界面、应用结构、应用平台、分布式系统、网络管理结构、CAD技术、人工智能等领域。面向对象是一种对现实世界理解和抽象的方法，是计算机编程技术发展到一定阶段后的产物。

好的，知道你还是看不懂，看不懂也没关系，先跳过
<div style="width:64%;height:12%;"><img src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1559888690493&di=3443b2c4d0df98f3fde0393a85888af9&imgtype=jpg&src=http%3A%2F%2Fimg.mp.itc.cn%2Fupload%2F20160928%2Fc6eb06f56bde41148cf546b3f02307b8_th.jpeg" /></div>
<br/>

---
#### 代码构成
我们直接上代码
在正式写代码之前，我们要先列出我们写这个代码的目标：
> ·    生成一个对象
·    生成一个女朋友

好的，看起来目标没有问题，接下来我们要画出我们这次代码的流程
```flow
st=>start: 开始
op=>operation: 创建类
op2=>operation: 类实例化生成对象
op3=>operation: 女朋友get√
en=>end: 结束

st->op->op2->op3->en
```
<br/>

确定目标和具体流程以后，我们可以开始肝代码了
<div style="width:64%;height:12%;"><img src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1559889941370&di=b29d896e8595355a0a92200973d2ac95&imgtype=0&src=http%3A%2F%2Fmmbiz.qpic.cn%2Fmmbiz_jpg%2F7KiaT2KS1kdqia6s16V2mO8bWAUIuNiaxOKmALAR1mqo9eviahsmUlzovrPqlrWiapewAd7oEHcsD43Mg7USeVwKYLA%2F640%3Fwx_fmt%3Djpeg" /></div>
<br/>

打开Visual studio……
额好麻烦，假装你们都会创建一个新项目8
![创建一个项目](http://119.23.24.92:39999/video/创建一个新项目.mp4)
点击上面这个就可以看怎么用VS创建一个新项目了
<br/>

现在我要开始get一个女朋友了！代码如下：


    #include <iostream>
    #include <string>
    
    class Girlfriend {
    public:
    	Girlfriend(std::string name, int years){
    		this->name = name;
    		this->years = years;
    	}
    	~Girlfriend(){}
    	void say(){
    		std::cout << "我是你的女朋友" << this->name << ",今年" <<  this->years <<  "岁啦~" << std::endl;
    	}
    private:
    	std::string name;
    	int years;
    };
    
    int main()
    {
    	Girlfriend girlfriend("小雪", 20);
    	girlfriend.say();
    	return 0;
    }
<br/>

编译运行结果如下：

    我是你的女朋友小雪,今年20岁啦~
<br/>

好的，我终于有女朋友了！
<div style="width:64%;height:12%;"><img src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1559894108405&di=bf614edef302a93a8ce1680eaa0374cd&imgtype=0&src=http%3A%2F%2Ftc.sinaimg.cn%2Fmaxwidth.2048%2Ftc.service.weibo.com%2Fp%2Fmmbiz_qpic_cn%2F1b39d8304d4d2c9fbedbfe670158f81f.jpg" /></div>
<br/>

真开心啊！
<div style="width:49%;height:12%;"><img src="https://imgsa.baidu.com/forum/w%3D580/sign=b3dd357bb4389b5038ffe05ab535e5f1/ba7350fbb2fb4316e82e551f2da4462309f7d344.jpg" /></div>
<br/>

---
#### 类以及类的实例化

今天的代码中，我们用到了一个关键字 ***class***
> 在C++中,程序员用"类"来描述 "对象",所谓的"对象"是指现实世界中的一切事物。那么类就可以看做是对相似事物的抽象。

class就是一定义一个类的关键字。
如何理解类与对象？

类好比是一张图纸：
<div style="width:49%;height:12%;"><img src="https://www.51gaifang.com/tu/UploadFiles_1151/201906/2019060612463330.gif" /></div>
对象就好比是根据图纸建成的房子：
<div style="width:49%;height:12%;"><img src="https://www.51gaifang.com/tu/UploadFiles_1151/201906/2019060612463354.jpg" /></div>
<br/>

从图纸到房子，我们需要建造。我们用到水泥、砖石等等材料；
从类到对象，我们需要 ***实例化*** ，我们用到一部分内存空间。

实例化其实很简单，比如例子中的类Girlfriend，实例化一个对象girlfriend：

    Girlfriend girlfriend("小雪", 20);
    
类名像数据类型一样写在前面，后面跟着的是类似变量的对象名，括号里的内容是初始化的数据。

    int i = 0;
    
虽然形式不大一样，但我们可以看到类的实例化其实和定义一个变量的差别也不大，大概都是告诉编译器下面三样东西：

```flow
st=>start: 开始
op=>operation: 申请的空间的数据的类型  {Girlfriend, int}
op2=>operation: 这片空间的名字  {girlfriend, i}
op3=>operation: 这片空间具体存入的数据  {("小雪", 20), 0}
en=>end: 结束

st->op->op2->op3->en
```

剖开来看，其实类的实例化也不难理解，你甚至可以直接把它当成一个特殊的自定义数据类型。

---

#### 面向对象的意义
我们为什么要学习面向对象编程呢？~~是因为这样就能找到对象吗？~~

首先，我们有时候会遇到这样的问题，我们想要做一个数组，来存储学生的信息，但是学生有很多属性，假设有学号、姓名以及性别，共十个学生，那么我们就要分别建立三个数组来存储这些信息吗？

    std::string id[10];
    std::string name[10];
    std::string sex[10];
    
显然，这样是很麻烦的，因此我们如果想要实现上述操作，就会创建一个结构体：

    struct Student
    {
    	std::string id[10];
    	std::string name[10];
    	std::string sex[10];
    }typedef Student;
    
    Student student[10];
    
以后我们每次需要存储学生的信息，就直接包含了学生的这些属性进去，用Student直接创建结构体变量，能省很多事情。
我们如果想要使用学生的信息，直接像下面这样调用：

    student[0].id = "2017211999"
    
但是，我们并不能满足结构体带给我们的功能。
比如，学校突然要求，学生信息增添一项年龄，那么我们必须要重写整个结构体：

    struct Student
    {
    	std::string id[10];
    	std::string name[10];
    	std::string sex[10];
    	int years; // 增加了年龄的属性
    }typedef Student;
    
另外，struct是开放的，所有属性都能被外界使用，因此***安全性***得不到保证。

如果我们使用class，定义类，就能解决这些问题。

*   类可以***继承***，也就是可以添加新的属性到类中去
*   类中区分***公有类型、私有类型、保护类型***，公有类型可以被任意调用，私有类型只能被类内部调用，保护类型则可以被子类（即继承它的类调用）
*   类中可以写入函数，被称为“方法”，方法可以被对象调用，不必在结构体外写函数，提高了整合度。

好的，先就这么多，下一节讲类的定义

---

---

### 第二节 类的定义

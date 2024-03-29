# 一、实验目的
1.分析学生选课系统
2.使用GUI窗体及其组件设计窗体界面
3.完成学生选课过程业务逻辑编程
4.基于文件保存并读取数据
5.处理异常
# 二、实验内容
一、系统角色分析及类设计
例如：学校有“人员”，分为“教师”和“学生”，教师教授“课程”，学生选择课程。
定义每种角色人员的属性，及其操作方法。
属性示例：	人员（编号、姓名、性别……）
教师（编号、姓名、性别、所授课程、……）
			学生（编号、姓名、性别、所选课程、……）
			课程（编号、课程名称、上课地点、时间、授课教师、……）
以上属性仅为示例，同学们可以自行扩展。

二、要求:
1、	设计GUI窗体，支持学生注册、课程新加、学生选课、学生退课、打印学生选课列表等操作。
2、	基于事件模型对业务逻辑编程，实现在界面上支持上述操作。
3、	针对操作过程中可能会出现的各种异常，做异常处理
4、	基于输入/输出编程，支持学生、课程、教师等数据的读写操作。
5、	基于Github.com提交实验，包括实验SRC源文件夹程序、README.MD实验报告文档。
# 三、实验步骤
1．	写出新的GUI
2．	编写文件的读写
3．	输入选课信息。
4．	画出程序流程图
# 四、流程图
![](https://github.com/zhanghan11128/shiyan/blob/master/1.png)
# 五、核心代码
1. 选课部分
	public void init() {
		SystemTest s=new SystemTest();
		String[] s1=s.getclas();
		JFrame frame=new JFrame();
		frame.setTitle("选课");
		JPanel panel2=new JPanel();
		JList list =new JList(s.getclas());
		Choice moveistars = new Choice();
		moveistars.addItem("sub1");
		moveistars.addItem("sub2");
		moveistars.addItem("sub3");
		JButton btn1=new JButton("确定");
		btn1.addActionListener(new ActionListener(){
			public void actionPerformed(ActionEvent arg0) {
				writeFile(s2);
				JOptionPane.showMessageDialog(null, "选课成功");
				setVisible(false);
			}});
		JButton btn2=new JButton("退出");
		btn2.addActionListener(new ActionListener(){
			public void actionPerformed(ActionEvent arg0) {
				setVisible(false);
			}
		});
		panel2.add(btn1);
		panel2.add(btn2);
		panel2.add(list);
		this.add(panel2);
	}

# 六、实验结果
![](https://github.com/zhanghan11128/shiyan/blob/master/2.png)
![](https://github.com/zhanghan11128/shiyan/blob/master/3.png)
# 七、感想
实验过程中经常遇到不会的问题，这时可以选择向老师和同学求助，实在不行还可以上网搜索解决方案。在写代码的时候经常会出现小细节的错误，这提醒了我在以后的学习中要更加认真仔细，对每一行代码都要认真的阅读，进行检查和完善。养成这个好习惯将对我以后的学习有更多的好处。

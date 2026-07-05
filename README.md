# bianchenglianxi
在线编程练习与智能答疑功能设计与实现
1.开发环境要求
本系统部署时操作系统需要有Java17环境、MySQL8.0.37数据库、Maven4.0.0环境等，运行工具需要idea和Postman测试以及数据库工具Navicat Premium。
2.Java环境配置
1.根据需要的选择下载JDK安装包。
2.安装JDK包，选择安装的路径时，可以自定义，也可以默认路径。
3.配置环境变量，右击【我的电脑】---【属性】-----【高级】---【环境变量】。
4.在系统变量下点击【新建】--弹出“新建系统变量”对话框，在“变量名”文本框输入“JAVA_HOME”,在“变量值”文本框输入JDK的安装路径。
5.在“系统变量”选项区域中查看PATH变量，如果不存在，则新建变量 PATH，否则选中该变量，单击“编辑”按钮，在“变量值”文本框的起始位置添加“%JAVA_HOME%\bin;%JAVA_HOME%\jre\bin;”或者是直接“%JAVA_HOME%\bin;”。
6.在“系统变量”选项区域中查看CLASSPATH 变量，如果不存在，则新建变量CLASSPATH，否则选中该变量，单击“编辑”按钮，在“变量值”文本框的起始位置添加“.;%JAVA_HOME%\lib\dt.jar;%JAVA_HOME%\lib\tools.jar;”。
7.成功安装之后，进行测试是否真的成功安装，win+r----输入 CMD，在命令提示符里面输入“JAVAC”并按回车键，如果出现主机配置则证明安装成功
3.MySQL安装配置
3.1下载完成解压到自定义目录
在MySQL官网下载8.0.37版本的MySQL数据库，下载完成解压到自定义目录，以下演示的解压路径为D:\Program Files\mysql-5.7.26-winx64。
3.2设置环境变量
1.点击我的电脑->属性->高级系统属性->环境变量
2.系统变量里面新建“MYSQL_HOME”值“D:\Program Files\mysql-8.0.37-winx64”
3.在系统变量里的path中新建%MYSQL_HOME%\bin;
3.3MySQL配置
1.以管理员身份打开命令行，转到MySQL的bin目录下
2.安装MySQL服务：MySQL --install
3.初始化MySQL： mysqld --initialize --console
4.开启MySQL服务：net start MySQL
5.登录验证，验证MySQL是否安装成功
4.Maven安装配置
4.1下载完成解压到自定义目录
在Maven官网下载安装4.0.0版本（apache-maven-4.0.0-bin.zip），下载完成后解压到自定义目录
4.2安装Maven
1.设置系统环境变量MAVEN_HOME，指向maven的根目录 ;
2.设置环境变量Path，将%MAVEN_HOME%\bin加入Path中;
3.配置完成后检查是否安装成功 ,打开命令提示符cmd，在命令行中输入:mvn -version，看是否配置成功
4.3Maven数据仓库配置
进入Maven的安装路径 -> conf -> 找到settings.xml文件，打开文件，找到localRepository标签，该标签默认是被注释掉的，保留原有的注释，新添加该标签，对应的路径可以自定义，配置本地仓库，创建一个空文件夹用于存放远程下载的jar包。
4.4在IDEA中集成Maven
1.打开IDEA编辑器，打开file->Setting搜索maven，若打开IDEA之前已经安装了Maven，则IDEA会自动发现Maven并进行关联
2.倒数第二个选项，勾选Override，选择刚刚修改的setting.xml文件
3.最后一个选项，勾选Override，选择创建的本地仓库
5.Redis安装配置
通过官网下载Redis数据库，下载完成后按步骤安装即可，Redis官网地址为https://github.com/tporadowski/redis/releases。
6.系统部署
6.1数据库配置
本系统在部署时，需要对数据库进行配置，首先将数据库文件导入MySQL数据库，该系统正常运行需要使用user表、problem表、submission表、course_resource表等，因此在系统部署时需要提前进行数据库配置。
7.系统运行
先打开docker服务，然后在IDEA中先后启动oj-backend、oj-front项目，系统就能够正常运行，通过访问http://localhost:5173地址登录本系统管理系统，管理员的账号为admin密码123456；教师账号为teacher密码123456；学生账号6个，分别s1到s6密码均为123456，登录后即可查看系统功能。

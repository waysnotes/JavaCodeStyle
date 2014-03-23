JavaCodeStyle
=============

**优美代码，从CodeStyle起**


> 该规范为个人习惯的编码规范。另请使用 UTF-8 格式来编写代码，避免出现中文乱码。

注：该规范是根据公司同事的分享总结的。
整理代码
-------

 - Java 代码中不允许出现在警告，无法消除的警告要用 @SuppressWarnings。
 - 去掉无用的包、方法、变量等，减少僵尸代码。
 - 使用 Lint 工具来查看并消除警告和错误。
 - 使用 Ctrl+Shift+F 来格式化代码，然后再进行调整。
 - 使用 Ctrl+Shift+O 来格式化 Import 包。

命名规则
----

###基本原则  

 - 变量，方法，类命名要表义，严格禁止使用 name1, name2 等命名。
 - 命名不能太长，适当使用简写或缩写。（最好不要超过 25 个字母）
 - 方法名以小写字母开始，以后每个单词首字母大写。
 - 避免使用相似或者仅在大小写上有区别的名字。
 - 避免使用数字，但可用 2 代替 to，用 4 代替 for 等，如 go2Clean。

###类、接口

 - 所有单词首字母都大写。使用能确切反应该类、接口含义、功能等的词。一般采用名词。
 - 接口带 I 前缀，或able, ible, er等后缀。如ISeriable。  

###字段、常量

 - 成员变量以 m 开头，静态变量以 s 开头，如 mUserName, sInstance。
 - 常量全部大写，在词与词之前用下划线连接，如 MAX_NUMBER。
 - 代码中禁止使用硬编码，把一些数字或字符串定义成常用量。
 - 对于废弃不用的函数，为了保持兼容性，通常添加 @Deprecated，如 doSomething()

###注释

请参考 SampleCode 类的注释。 

 - 常量注释，参见 ACTION_MAIN
 - 变量注释，参见 mObject0
 - 函数注释，参见 doSomething(int, float, String)

###Class 内部顺序和逻辑

 - 每个 class 都应该按照一定的逻辑结构来排列基成员变量、方法、内部类等， 从而达到良好的可读性。
 - 总体上来说，要按照先 public, 后 protected, 最后 private, 函数的排布 也应该有一个逻辑的先后顺序，由重到轻。

 
4.3. 以下顺序可供参考：

> 定义TAG，一般为 private（可选）  
定义 public 常量  
定义 protected 常量、内部类   
定义private 变量   
定义 public 方法   
定义 protected 方法   
定义 private 方法

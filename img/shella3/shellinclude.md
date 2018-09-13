# Shell 文件包含 #
#### shell外部脚本
<div class='mdContent'>
 　　和其他语言一样，Shell 也可以包含外部脚本。这样可以很方便的封装一些公用的代码作为一个独立的文件。

　　Shell 文件包含的语法格式如下：

	. filename   # 注意点号(.)和文件名中间有一空格

　　或

	source filename
##### 实例
　　创建两个 shell 脚本文件。
  
　　test1.sh 代码如下：

	#!/bin/bash
	# author:赋能教程
	# url:www.ultrapower.com.cn
	url="http://www.ultrapower.com.cn"
　　test2.sh 代码如下：

		#!/bin/bash
		# author:赋能教程
		# url:www.ultrapower.com.cn

		#使用 . 号来引用test1.sh 文件
		. ./test1.sh

		# 或者使用以下包含文件代码
		# source ./test1.sh

		echo "赋能教程官网地址：$url"
　　接下来，我们为 test2.sh 添加可执行权限并执行：

		$ chmod +x test2.sh
		$ ./test2.sh
		赋能教程官网地址：http://www.ultrapower.com.cn

</div>
#### 
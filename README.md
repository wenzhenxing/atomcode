Atomcode PHP 开发框架
========

这个框架一个新的版本完成了。之前也有一个同名的框架，也是我做的，但是规则仍然太复杂。所以重新做一个。

为什么要做这个框架呢？
--------
我感觉框架的规则都太多了。这个非常少。你要能接受就接受，不能接受这么简单，那还是要使用别的框架得了。

### 目录结构

总共需要有三套目录： 框架的目录， 你自己的程序目录，你的入口文件和图片之前Web资源目录。分别如下：

		| atomcode
		
		| app         # 这个名字无所谓
		
		| public	# 这个名字更无所谓，但是 Web 服务器一定要访问到

atomcode 目录你不需要关心，只需要找个地方放就行了。

app 目录结构：

		|- config
		  |- config.php
		|- controller
		|- model
		|- view


### 快速体验

我们把三个目录放好，把web服务器目录指向到public目录。然后开始写一个 controller

		<?php
		class IndexController extends Controller {
			public function indexAction() {
				echo "hello world";
			}
		}

OK, 开始访问吧：

http://example.com/index.php?_url=index/index
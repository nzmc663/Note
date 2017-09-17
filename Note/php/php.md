# 性状（trait） #
1. 性状是类的部分实现
2. 作用：
	1. 表明类可以做什么（类似接口）
	2. 提供模块化（类似类）

    		<?php  
    		namespace App\Tra;  
    		Trait logTrait{  
    			public function show(){  
    				echo 'Hello Yaha!';  
    			}  
    			public function print(){  
    				echo 'Hello World!';  
    			}  
    		}  
			

			<?php  		  
			namespace App\Http\Controllers;  
			use Illuminate\Http\Request;  
			use App\Tra\logTrait;  
			class LearnController extends  Controller{  
			    use logTrait;  
			    public function index()  {  
			        $res = $this->show();  
			    }  
			}  


# 生成器（generator） #


# 闭包 #


# PSR规范 #


# 组件 #

# 过滤、转义和验证 #
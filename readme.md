##popShow是什么?
一个优化alert提示效果，遮罩提示，基于AntUI

##popShow有哪些功能？
*
*普通文本提示，带图标文本提示，询问提示，带输入询问提示，页面提示,嵌套ifreme
***************************


##popShow使用方法
 * 
 * 调用方法，
 * 引入 AntUI 主文件 antui.css
 * 引入popShow.js
 * 以上准备完成即可
 
 * 举个栗子：
```javascript
    Pop.Show("弹出文本提示")//弹出普通文本提示
```    	
 * *********************************************************************
 * 提示框：Pop.Show({icon:"",content:"",time:""})
 * Icon:"带图标类型";int（1:加载  2:警告  3:成功  4:网络  5:失败）不设置属性为普通文本框
 * content:"提示内容" string
 * time:"显示时间" int 默认两秒
```javascript
    Pop.Show({icon:3,content:"hello,word!",time:3})//弹出一个带有成功图标的提示框 3秒
```  
 * *******************************************************************
 * 对话框：Pop.Dialog({title:"",content:"",but:""},function(e){})
 * title: 带标题对话框 string 不传为不带标题
 * content：内容 string 必传
 * but: 按钮方式 'ok' 不传或为空 为双按钮， 传 "ok" 只有一个确认按钮
 * input: 是否有输入框 bool 输入为普通文本框
 * placeholder：输入框暗提示 string
 * function(e){}: 回调函数 e为回调数据 {ok:bool,input:string} e.ok 判断用户点击取消还是确认
 * 可直接传内容 例如：Pop.Dialog("直接传递内容字符串"，funciton(e){})
```javascript
   Pop.Dialog({title:"hello",content:"欢迎",but:"ok",input:true,placeholder:"这里是暗提示"},function(e){
	   if(e.ok){
			Pop.Show("你点击成功！你在输入了："+e.input);
		}
   });
   //弹出一个只有一个确认按钮的输入对话框
``` 
 * ********************************************************************
 * 页面提示：Pop.Loading({type:"",title:"",content:""},function(){});
 * ****type:"页面类型" int （1:加载 2：网络 3:内容）
 * ****title:"标题" string 仅内容页调用该参数
 * ****content："内容" string 仅内容页调用该参数
 * ****function(){}  回调函数 监听刷新按钮回调事件 不传则不显示刷新按钮
```javascript
  Pop.Loading({type:2,content:"网络错误请刷新"},function(){
		Pop.Show({icon:3,content:"页面加载完成"});
  });
  //弹出一个只有一个页面遮罩层
``` 
 * ********************************************************************
 * 页面：Pop.Iframe({title:"",url:""},function(){});
 * ****title:"标题" int
 * ****url："打开链接" int
 * ****function(){}  回调函数 监听返回按钮回调事件
```javascript
  Pop.Iframe({title:"iframe窗口",url:"http://www.jhjlwang.com"},function(){
		Pop.Show("你点击了返回");
  });
  //弹出一个只有一个页面遮罩层
``` 
 * *********************************************************************
 * 其他：Pop.Down(int) 关闭所有弹出/指定窗口 (1:文本 2：图标  3:对话框 4:页面 )
 
************************************************************************

##有问题反馈
在使用中有任何问题，欢迎反馈给我，可以用以下联系方式跟我交流

* 邮件(swift_dc@qq.com)
* QQ: 779590853
* weibo: [@从面向BUG到面向对象](http://weibo.com/p/1005051929504707)
* 个人小站： [饥荒交流网](http://www.jhjlwang.com)

##捐助开发者
在工作的驱动下,写一个`免费`的东西，有欣喜，也还有汗水，希望你喜欢我的作品，同时也能支持一下。


##感激
感谢以下的项目,排名不分先后

* [AntUI](https://antui.alipay.com/10.0.18/index.html)

##关于作者

```javascript
  var info = {
    nickName  : "swift_dc",
    site : "http://www.jhjlwang.com"
  }
```

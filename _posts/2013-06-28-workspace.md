---
layout: default
title: chrome workspace使用笔记
---

以前就幻想过，为啥我们用浏览器的开发者工具调试页面的样式什么的，不能保存呢，要知道苦逼的前端每每调试多了，根本就是会分分钟忘记刚刚改了哪些属性滴！


帅气的谷歌给了我答案！用chrome的workspace就可以让我们调试的同时，<!-- more -->在我们的编辑器里做对应修改。  

正式版的chrome workspace功能并没有默认开启，我们需要进入chrome://flags手动开启对应的"启用开发者工具实验"  
<img style="border:1px solid #ccc;" src = "http://lixiaochou077.github.io/images/ws1.png" /> 
 
启动之后重启chrome，打开开发者工具，进入设置，可以看到新增的Experiments选项，勾选File system folders in Sources Panel选项，如下图：  
<img style="border:1px solid #ccc;" src = "http://lixiaochou077.github.io/images/ws2.png" />  

重启开发工具栏，即可看到新增的Workspace选项，如下图，我们在左侧的File systems里填写本地的文件夹路径，右侧Mappings可以设置文件的路由，url填写服务器上需要路由的文件url路径，path填写本地的对应文件所在文件夹路径。这一步需要注意的是，需要在本地路由的文件夹中创建一个名为.allow-devtools-edit的空文件，浏览器才会认可。  
<img style="border:1px solid #ccc;" src = "http://lixiaochou077.github.io/images/ws3.png" />   
<img style="border:1px solid #ccc;" src = "http://lixiaochou077.github.io/images/ws4.png" />  

再次重启Developer Tools，在Sources页可以看到本地文件夹信息  
<img style="border:1px solid #ccc;" src = "http://lixiaochou077.github.io/images/ws5.png" />  

此时，再进行需要的调试，修改的代码就会在本地源文件中得到体现。

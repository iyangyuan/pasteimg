pasteimg浏览器中粘贴图片jQuery插件
--------------------------
  
pasteimg是一款可以在浏览器中实现图片粘贴的jQuery插件，兼容Chrome、Firefox、IE11以及其他使用这些内核的浏览器，比如，国内著名的360浏览器。  
  
pasteimg可以识别浏览器中直接复制的图片，也可以识别复制的富文本中的图片。仅仅可以识别在浏览器中复制的内容，操作系统中复制的图片是不能识别的。 
   
pasteimg依赖jQuery，简单易用，引入jQuery和paste.image.js后，调用方式如下：  
  
    //在需要监听粘贴事件的dom元素上调用pasteImage方法
    //调用pasteImage方法需要传入一个callback参数
    //一旦粘贴的内容中发现图片，就会调用callback
    //调用callback时，会传入一个数组，包含了所有的图片
    //本插件会尽可能的将图片转换成base64编码，但受到跨域的限制，如果不能转换，将返回图片的绝对url路径
    $("#container").pasteImage(function(imgs){
      //imgs is array that contain all image, you can do something...
    });
  

配置了gulp和browser-sync。  
说明:
1. 在项目目录运行gulp命令，会打开gulpfile.js中设置的根目录下的index.html。
2. 若访问其他文件，需要自己补充网址。例如：http://localhost:3000/html/[xxx].html

最原始的可以使用window.setTimout()或者window.setInterval()通过不断更新元素的状态位置等来实现动画，前提是画面的更新频率要达到每秒60次才能让肉眼看到流畅的动画效果。

window.requestAnimationFrame()方法的原理，其实跟setTimeout/setInterval差不多，通过递归调用同一方法来不断更新画面以达到动起来的效果，但它优于setTimeout/setInterval的地方在于它是由浏览器专门为动画提供的API，在运行时浏览器会自动优化方法的调用，并且如果页面不是激活状态下的话，动画会自动暂停，有效节省了CPU开销。

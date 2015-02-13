

http://www.phpletter.com/DOWNLOAD/

http://forum.jquery.com/topic/file-upload-ajaxsubmit-sends-response-to-wrong-window-in-ie


java 上传文件 返回json格式数据 ie下面打开下载窗口
原因是返回时 的response.setContentType("application/json; charset=UTF-8");
json的mime为：application/json ie一解析认为是文件，所已提示下载

解决办法 是 返回时 content-type 设置为 text/html 
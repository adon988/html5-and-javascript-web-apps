html5-and-javascript-web-apps
=============================

webKit 是 Mobiel Safari、Android 和chrom 的瀏覽器引擎，只要W3C發布新規格就會加以採用

JSHint   Javascript 除錯  
參考: http://www.jshint.com/#report

http://jas9.blogspot.com/2012/04/html5-polyfillwebshims-lib.html



requireJS 套件:  
簡化js的引用
http://requirejs.org/docs/start.html
1.先下載套件 http://requirejs.org/docs/download.html

2.引用方式 <script data-main="scripts/main" src="scripts/require.js"></script>

scripts資料夾中 存在main.js檔案

3.在main.js中的require JS 
範例一
require(["helper/util"], function(util) {
    //This function is called when scripts/helper/util.js is loaded.
    //If util.js calls define(), then this function is not fired until
    //util's dependencies have loaded, and the util argument will hold
    //the module value for "helper/util".
});
這裡load的是  helper/util.js 

範例二  引用 
require(["jquery", "jquery.alpha", "jquery.beta"], function($) {
    //the jquery.alpha.js and jquery.beta.js plugins have been loaded.
    $(function() {
        $('body').alpha().beta();
    });
});


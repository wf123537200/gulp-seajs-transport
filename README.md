保留原gulp-seajs-transport功能，并且支持手动配置前缀
具体使用方法可参照：
gulp.task("cmd-trs-out", function() {
    return gulp.src("./*",{base:""})// 源文件地址
        .pipe(transport({
            prefix: '/tpl/' // 压缩的模块前缀名
        })) 
        .pipe(uglify())    //压缩
        .pipe(gulp.dest("./dist/"));// 目标地址
});

package.json增加
    "dependencies": {
    // 用这一行代替原来的gulp-seajs-transport
    "gulp-seajs-transport-zak": "",
  },

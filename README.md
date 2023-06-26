# fat-aar-jar
把多个aar或者jar打包为一个aar包

目录结构：



(1) aa1:用于单独打包aar包，执行assembleRelease后会自动拷贝到fat-aar的libs目录

(2) aa2:用于单独打包aar包，执行assembleRelease后会自动拷贝到fat-aar的libs目录

(3) fat-aar：用于把libs下的多个aar包合成一个新的aar包，不包含当前module的代码，执行assembleRelease会自动打合成包，并自动包拷贝到fat-aar-jar/libs目录下，名为：fat-aar.aar

(4) fat-aar-jar：用于把libs下的多个aar包或者jar打包成一个新的aar包，不包含当前module的代码，目前只支持一个aar包+多个jar包的合成包，有多个aar包需要合并的，先在fat-aar打成一个， 再来这里最后打一次， 执行assembleAAR会自动打合成包，并自动包拷贝到app/libs目录下，名为：fat-aar-jar-1.0.0.aar。

(5) app：用于验证和包的效果，运行之前先sync gradle file一次，这样合成包更新才会生效



注意：以上命令在执行过程如果有错误，一般都是缓存引起的，先执行对应module下build的clean即可

使用方法：把fat-aar和fat-aar-jar拷贝到自己的工程中当module引入，编译方法请参见demo。






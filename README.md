# fat-aar-jar
把多个aar或者jar打包为一个aar包

目录结构：
aa1:用于单独打包aar包，并手动拷贝到fat-aar-jar的libs目录
aa2:用于单独打包aar包，并手动拷贝到fat-aar-jar的libs目录
app：用于验证和包的效果

fat-aar-jar：用于把libs下的多个aar包或者jar打包成一个新的aar包，不包含当前module的代码，目前只支持一个aar包+多个jar包的和包，执行assembleAAR会自动
打和包，并自动包拷贝到app/libs目录下，名为：fat-aar-jar-1.0.0.aar，每次打包后需要sync gradle file一次，这样新的aar包才会被更新和识别



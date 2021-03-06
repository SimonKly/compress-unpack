# compress-unpack

### compress-unpack介绍
compress-unpack是文件、文件夹压缩解压工具类，可以支持压缩为如下格式：
- rar
- zip
- tar.gz
- tar

### rar格式的压缩与解压
### zip格式的压缩与解压
### tar.gz格式的压缩与解压
- 压缩
对tar.gz的压缩分为三步：
    - 压缩为tar文件
    - 将tar文件压缩为gz
    - 删除tar文件
- 解压  
对tar.gz的解压分为三步：
    - 解压tar.gz为tar文件 
    - 解压tar文件
    - 删除tar文件

### 解压缩工具类的使用
**压缩、解压zip:**  
- 压缩
```
String sourcePath = "input/springboot-log";
String targetPath = "compress-output/";
CompressTool.compressToZip(sourcePath, targetPath);
```
- 解压
```
String sourcePath = "input/springboot-log.zip";
String targetPath = "unpack-output/";
File file = new File(sourcePath);
UnpackTool.unpackZip(sourcePath, targetPath);
```
**压缩、解压rar:**  
- 解压
```
String sourcePath = "input/学习.rar";
String targetPath = "unpack-output/";
UnpackTool.unpackRar(sourcePath, targetPath);
```
**压缩、解压tar.gz:**
- 解压
```
String sourcePath = "input/springboot-log.tar.gz";
String targetPath = "unpack-output/";
UnpackUtil.unpackTarGz(sourcePath, targetPath);
```
- 压缩
```
String sourcePath = "input/springboot-log";
String targetPath = "compress-output/";
CompressUtil.compressToTarGz(sourcePath, targetPath);
```
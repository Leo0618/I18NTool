>背景：Android国际化多语言的支持，工作不复杂却是个体力活，需要导出默认中文，对应的翻译成其他语言并添加到工程里面，【I18NTool】是一款IDEA插件，适用于IDEA系列开发工具（包括AndroidStudio），目的是能够快速导出导入翻译文件，提供高效运作的效率工具。

### Feature
1. 支持多module的资源文件（moduleA、moduleB...）
2. 支持module下多资源文件（res、res-shop...）
3. 支持strings及arrays
4. 支持配置语言选择、是否全量导表、过滤项等

### Usage (以AndroidStudio为例)
1. 下载并安装插件：I18NTool
2. 打开设置，找到【国际化工具】设置栏，配置相关信息

![配置相关设置项](https://upload-images.jianshu.io/upload_images/2091835-74a9ad88763e5ae9.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 语言选择，目前支持中文繁体、英文、泰语，其他语言后续再增加
- 导出设置，全量导表会将不需要翻译的数据也导出，建议不勾选，只导出需要翻译校正的内容即可
- 导入导出文件存放目录，导表文件Excel存放的目录位置，建议存放在工程项目目录内并受版本控制，导入时会根据此目录自动搜索可导入的文件
- 过滤项设置，目前支持的有：模块名称匹配过滤，字符串Key的前缀匹配过滤，中文字符串内容后缀匹配过滤

3. 一键导出，Tools>国际化工具>翻译导出。执行后会将需要翻译的内容收集到Excel表中并导出到配置的【导入导出文件存放目录】下

![示例-目录结构](https://upload-images.jianshu.io/upload_images/2091835-198a16c5cb0a5765.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![示例-导出结果](https://upload-images.jianshu.io/upload_images/2091835-69625dd9ab4c84bf.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

4. 将Excel表内容由指定人员进行翻译后，保证表的格式模板不变动，放在【导入导出文件存放目录】下

![示例-导入结果](https://upload-images.jianshu.io/upload_images/2091835-2485862a132a9b13.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

5. 一键导入，Tools>国际化工具>翻译导入。若存在可导入文件，默认显示最新导出日期对应的文件，点击OK执行导入，最终会生成配置对应语言的文件目录并修正补足翻译缺失的地方

![示例-一键导入](https://upload-images.jianshu.io/upload_images/2091835-a48ba98e2400fdc0.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![示例-结果.jpg](https://upload-images.jianshu.io/upload_images/2091835-7441bc2f28b242b0.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### Tips
1. 注意若字符串翻译成英文后包含't等内容，需要手动修正，加上转义符\
2. 注意若字符串中包含>或<符合时，会进行转义处理，如："<"转义成&lt加;的形式



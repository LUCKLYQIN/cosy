# 代码示例搜索

阿里云智能编码插件（Alibaba Cloud AI Coding Assistant）提供的代码示例搜索功能，让你在面对不熟悉的功能模块时，无需来回跳转页面，在IDE内即可参考海量优质的开源代码示例，为你打造沉浸式编码体验。

## 前提条件

- 已在IntelliJ IDEA中安装和配置Alibaba Cloud AI Coding Assistant，[如何安装](zh-cn/guide/quickstart.md)。
- 系统要求：Windows 10/Mac OS/Linux

## 通过自然语言搜索

当开发者需要实现不熟悉的功能模块时，通常会通过通用搜索引擎去查找相关的开源方案，但是由于通用搜索引擎提供的结果质量参差不齐，并且无法直接从结果页的标题中快速判断是否是自己需要资料，影响了开发者的查找效率。Cosy为开发者提供了自然语言搜索能力，开发者能通过对功能的文字描述，快速的查找到相关功能的开源实现。

- 支持英文自然语言搜索
  - 在搜索框中输入功能描述，如How to read excel，敲击回车触发，即可搜索到用于 ***读取Excel*** 的代码示例
  - 在搜索框中输入简短关键词，如oss download file，敲击回车触发，即可搜索到用于 ***OSS下载文件*** 的代码示例

如果开发者想进一步筛选自然语言搜索的结果，可以通过联合API搜索进行二次筛选，例如：

- 当开发者想实现”读取Excel“的功能时，开发者可以通过输入”read excel“进行搜索；但是存在很多开源库都能实现该功能，如果开发者想指定使用Apache POI库实现该功能，可以将该库下的某API（如：XSSFWorkbook）追加到搜索条件中，既可搜索出使用了XSSFWorkbook API进行Excel读取的代码示例。

## 通过API名称搜索

当开发者遇到不熟悉的API时，希望查找API相关的使用示例，然而很多API的官方文档都是不完善的，要么仅有Javadoc的简单文字描述，要么只有少量单元测试用例，要么缺少任何示例代码，从而需要开发者花费大量时间去查找API的示例代码。
Cosy为开发者提供了API代码示例的查找能力，开发者只需输入API名称或通过快捷键触发，就能快速查找到引用了该API的开源代码示例。

### 快捷搜索

开发者可以在编码过程中通过鼠标右键选中当前类/接口/方法，然后点击 ***查找代码示例*** 即可一键搜索指定API的代码示例片段。开发者也可以通过快捷键 MacOS `command+shift+s` 或 Windows `ctrl+shift+s` 搜索指定API。

![search_menu_example](https://img.alicdn.com/imgextra/i2/O1CN01LkVxJ71IktqQtmjbh_!!6000000000932-2-tps-852-1022.png ':size=300')

### 搜索条件

开发者可以通过点击右侧菜单栏中的 `代码示例搜索` 唤起搜索工具窗，手动输入API名称进行代码示例搜索，支持的API名称格式如下：

- 类名/接口名/枚举名
  - 如：XSSF能搜出以XSSF为前缀的类名XSSFWorkbook、XSSFRow等
- 包名+类名
  - 如：org.apache.poi能搜出这个包下的所有类/接口/枚举
  - 如：org.apache.poi.xssf.usermodel.XSSFWorkbook能准确搜出apache包下的XSSFWorkbook类
- 方法名
  - 如：createSh能搜出以createSh为前缀的方法名createSheet、CreateShortcut、createShell等
- 类名/接口名+方法名，枚举名+属性名
  - 如：XSSFWorkbook.create能搜出以其为前缀的XSSFWorkbook.createSheet、XSSFWorkbook.createFont、XSSFWorkbook.createCellStyle等
- 包名+类名/接口名+方法名，包名+枚举名+属性名

![search_example](https://img.alicdn.com/imgextra/i3/O1CN01sV74ML1uRcZXp6PRe_!!6000000006034-2-tps-1258-1614.png ':size=500')


## 支持语言

- 目前仅支持Java，后续会扩展JavaScript、Python等语言

## 使用示例

### 通过API名称搜索

[code-search-demo.mp4](https://cosy-aliyun.oss-cn-hangzhou.aliyuncs.com/code-search-demo.mp4 ':include :size=500')

### 通过自然语言搜索

[code-search-demo.mp4](https://aliyun-cosy.oss-cn-hangzhou.aliyuncs.com/cosy_search_demo.mp4 ':include :size=500')

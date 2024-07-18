# miniHtmlChatBot
原生html前端，无需额外服务端程序、无依赖库即可对接类OpenAI API

Read the project introduction in English: [README_en](README_en.md)

## 运行方式
1. 确定用户的首选语言
- 中文：main.html
- 英文：main_en.html
2. 完善API相关参数
- 修改对应html中的`ApiUrl`、`ApiKey`和`ApiModel`（费用自理）
- 如果想使用SiliconFlow（北京硅动科技有限公司）提供的免费API，则只需要到[SiliconFlow官网](https://siliconflow.cn/)完成注册并生成API，填入`ApiKey`处即可
3. 用浏览器直接打开对应的html文件

### 运行效果示例
<img src="https://i.ibb.co/tm0h44R/image.png" alt="运行效果"></img>

## 功能 / 亮点
- 基于`Gradio`的`web_demo`所提供的典型功能：多轮对话、清空历史、重新生成（上一个）结果
- 预置系统提示词选项 + 自定义系统提示词输入
- 多种模型选择功能，可随时切换
- AI生成对话标题（使用时消耗较多token，默认不开启）
- 通过URL参数快速开启对话，可用作自定义搜索引擎，URL组合规则：`[html文件URL]?s=[URL编码后的用户提示词]`
- 单html文件实现，大小<20kB

## 开发初衷
LLM开源模型发布后，一般会附带提供一个`web_demo`用于模型的基本使用，`web_demo`的实现用的最多的方式之一就是`Gradio`。使用`Gradio`当然也能接入AI API，但必须有一个Python后端在某处运行，并且对Python版本有一定的要求，不够方便，不能满足使用手机等设备随时随地接入API的需求。

因此我写了这个项目，用户只需要用浏览器打开本地文件的形式，就可以通过这个前端界面接入AI API。同时，为了提高打开效率，我**没有使用**任何依赖库、前端框架，所有外观、逻辑均使用原生`html / css / javascript`实现。

你也可以将该html作为更复杂的AI APP的搭建起点。

## 鸣谢
- [SiliconFlow](https://siliconflow.cn/)：提供免费API
- [Gradio](https://www.gradio.app/)：提供外观和代码逻辑参考
- [HTMLPAGE](https://htmlpage.cn/)：提供界面设计辅助工具

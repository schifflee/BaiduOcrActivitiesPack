# 百度文字识别活动包

百度AI开放平台提供多种文字识别，如增值税发票、营业执照、驾驶证等，可以用于多种RPA流程，我也在《RPA开发与应用》（即将出版）中详细讲解了如何在UiPath Studio中识别增值税发票。本代码库的目的是打通UiPath和百度文字识别，让开发者能在UiPath Studio中通过简单的拖放和设置把百度文字识别用到相关流程中，从而加速开发过程。

## 开发计划和状态

名称|类型|活动|发布日期|任务状态
---|---|---|---|---
[增值税发票识别](https://ai.baidu.com/tech/ocr_receipts/vat_invoice)|票据|[VatInvoiceActivity](https://github.com/allenlooplee/BaiduOcrActivitiesPack/blob/master/Baidu.AI.Ocr/Baidu.AI.Ocr.Activities/Activities/VatInvoiceActivity.cs)|2020-1-12|完成
[定额发票识别](https://ai.baidu.com/tech/ocr_receipts/quota_invoice)|票据|[QuotaInvoiceActivity](https://github.com/allenlooplee/BaiduOcrActivitiesPack/blob/master/Baidu.AI.Ocr/Baidu.AI.Ocr.Activities/Activities/QuotaInvoiceActivity.cs)|2020-1-13|完成
[出租车票识别](https://ai.baidu.com/tech/ocr_receipts/taxi_receipt)|票据|[TaxiReceiptActivity](https://github.com/allenlooplee/BaiduOcrActivitiesPack/blob/master/Baidu.AI.Ocr/Baidu.AI.Ocr.Activities/Activities/TaxiReceiptActivity.cs)|2020-1-13|完成

*其他文字识别活动将会陆续开发并发布。*

## 安装

![安装百度文字识别活动包](https://github.com/allenlooplee/BaiduOcrActivitiesPack/blob/master/docs/images/Install.PNG)

本活动包目前还在开发当中，如果你想在UiPath Studio中提前体验一下，可以到GitHub Releases下载[v0.1.0 Pre-release](https://github.com/allenlooplee/BaiduOcrActivitiesPack/releases/tag/v0.1.0)，然后到UiPath Studio的Manage Packages安装活动包。

*本活动包也将发布到[UiPath Go](https://go.uipath.com/)。*

## 使用

![使用百度文字识别活动](https://github.com/allenlooplee/BaiduOcrActivitiesPack/blob/master/docs/images/Use.PNG)

安装好本活动包之后，你会在Activities面板上看到相关的活动，把你想使用的文字识别活动拖到Designer面板，然后在Properties面板上指定你想识别的图片就行了，识别结果将以[JObject](https://github.com/JamesNK/Newtonsoft.Json/blob/master/Src/Newtonsoft.Json/Linq/JObject.cs)对象返回。

*注意：所有文字识别活动都要放在BaiduOcrScope中，在使用文字识别活动之前，你需要在[百度AI开放平台](https://ai.baidu.com/)注册账号，创建文字识别应用，获取API Key和Secret Key，并填入BaiduOcrScope的相应属性中。*

## 构建

如果你想自行构建或改进代码，你需要安装以下工具：
1. [Visual Studio 2019](https://visualstudio.microsoft.com/)，安装的时候需要[选中Windows Workflow Foundation](https://docs.microsoft.com/en-us/visualstudio/workflow-designer/developing-applications-with-the-workflow-designer?view=vs-2019#install-windows-workflow-foundation)
2. [UiPath Activity Creator](https://marketplace.visualstudio.com/items?itemName=UiPathLabs.UiPathActivitySet)
3. [UiPath Studio](https://www.uipath.com/start-trial)

Visual Studio用来打开[活动包项目](https://github.com/allenlooplee/BaiduOcrActivitiesPack/blob/master/Baidu.AI.Ocr.sln)，UiPath Studio用来打开[测试项目](https://github.com/allenlooplee/BaiduOcrActivitiesPack/blob/master/tests/Baidu.AI.Ocr.Tests/Main.xaml)。在运行测试项目之前，你需要把文字识别应用的API Key和Secret Key填入BaiduOcrScope活动的相应属性。

## 其他代码库和参考资料
* [百度AI开放平台 .NET SDK](https://github.com/Baidu-AIP/dotnet-sdk)
* [JSON.NET](https://github.com/JamesNK/Newtonsoft.Json)
* [百度文字识别API文档](https://ai.baidu.com/ai-doc/OCR/Ek3h7xypm)
* [Quick Start: The 5 minute activity set](https://docs.uipath.com/integrations/docs/quick-start)
* [Windows Workflow Foundation](https://docs.microsoft.com/en-us/dotnet/framework/windows-workflow-foundation/)

## 许可协议

本代码库遵循[MIT许可协议](https://github.com/allenlooplee/BaiduOcrActivitiesPack/blob/master/LICENSE)，可作商业用途。

# [《实例化需求：团队如何交付正确的软件》](http://product.dangdang.com/22855890.html) 书摘（20150607）

内容简介：         
《实例化需求：团队如何交付正确的软件》是在世界各地调查了多个团队软件交付过程后的经验总结。书中介绍了这些团队如何在很短的周期内说明需求、开发软件，并交付正确的、无缺陷的产品；为团队在实施实例化需求说明时使用的模式、想法和工件创建了一致的语言；展示了案例中的团队用来实现实例化需求说明原则的关键性实践；并在案例分析部分展示了一些团队实施实例化需求说明的历程。     

     
**以下基本上是关键内容摘录，就不特地用引用格式了，2333**    


业务目标——>从目标中获取范围——>范围（用户故事、用例）——>举例说明、协作制定需求说明——>关键实例——>提炼需求说明——>实例化需求说明——>进行自动化验证时不修改需求说明——>可执行的需求——>频繁验证、演进出一个文档系统——>活文档     

OR     

从目标中获取范围     
通过协作制定需求说明     
举例说明     
提炼需求说明     
自动化验证而不修改需求说明     
频繁验证     
演化出文档系统     


- 用户故事：作为……，我想要……，为了……。     


- 流程描述（长句子）			短句子+穿行测试     
例子必须精确、具体，不能抽象，尽量不用“是/否”          
例子必须完成，数据边界必须考虑，各种可能性的替代方案     
例子必须真实不虚构，从客户直接获取     
例子易于理解，太过复杂则应重新抽象和分类     
用户对界面有何需求     


- 实例加工为需求说明     
带实例     
条件     
功能的预期输出，而非系统的实现细节，即关于业务功能而非软件设计     
验收测试     


- 提炼注意事项     
实例精确可测，数量较少的良好的关键实例     
不要脚本，不要用流程式的描述     
不要软件设计，不要与代码紧密耦合（但单元测试、集成测试还是需要的）     
不要用户界面，专注于边缘情况及功能     
用叙述性标题并简短解释目标（想想搜索这个功能时所用的关键字吧）     
需求说明要专注，一条业务规则，一个功能，或过程的一个步骤     
使用“Given-When-Then”语言     
不要明确建立所有依赖，尽量放入自动化层     
不要过度依赖自动化层缺省值，以免受缺省值修改影响     
统一语言（类似DDD）     


- 自动化验证注意事项     
小项目/小模块开始          
事先计划好，适当预留时间     
由开发人员将自动化工具库作为一个单独的产品          
测试要独立、专注，以便于定位问题     
不要使用用户界面测试（点击等）而要以行为为导向测试     

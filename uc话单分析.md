## UC常用类
* CiscoCDR
* FileCollectionParam: 数据处理缓冲类，包裹一个将xml数据解析到对象（FileCollectConfig）的过程
* LocalFileOperator: 本地文件操作类
* FileAnalyseParam: 数据分析处理缓冲类，包裹一个将xml数据解析到对象（FileAnalyseConfig）的过程
* CDROriginal: 原始数据实体类
---
* **OrigiCdrFileParser**：CDR话单文件分析类
* **CmrFileParser**: CMR记录分析类
* SpecallService: 原始话单分析处理服务
* CdrRecorderParser: 识别并分类处理
* CdrValidationManager: CDR文件校验管理类
* BaseCdrFieldValidator: 话单字段有效性校验基类
* NormalBuffer: 缓冲管理类
* CdrFieldConfigParser: CDR字段配置类
* AppResultCountManage: 采集线程处理结果同步计数器
## UC话单字段分析
CallingNumber：主叫号码

## 话单分析处理
### CdrRecorderParser.flow() // 识别并分类处理话单的入口方法
* MissCall: 处理未接来电话单
* Ignore: 处理忽略类型的话单
* Split: 处理需要拆分的话单
* MergerSign: 处理需要合并的话单
* Common: 处理普通的话单

### MergerService // 识别并合并
* MeetingJion.mergerMeeting(); //合并Jion Meeting话单
  CdrRecorderSaver.saveResult(); //保存数据到CDR表
  CDROriginalService.saveResult(); //标记已处理的话单
* Meeting.mergerMeeting(); //合并Meeting话单
* Transferred.mergerTransferred(); //合并呼叫转移(Transferred)话单
* Replaces.mergerReplaces(); //合并(Replaces)话单
  CdrRecorderSaver.saveResult(); //保存数据到CDR表
  CDROriginalService.saveResult(); //标记已处理的话单

### UC字段与Call Manager数据库字段解析
* configParam.getField(int j).getUCFieldName(); // CDR话单中的字段
* configParam.getField(int j).getCMFieldName(); // CM数据库字段
* configParam.getField(j).getCMIndex(); // 字段索引Index

### 数据库表说明
* COLLECTIONLOG: 话单采集日志记录处理


[TOC]
## UC������
* CiscoCDR
* FileCollectionParam: ���ݴ������࣬����һ����xml���ݽ���������FileCollectConfig���Ĺ���
* LocalFileOperator: �����ļ�������
* FileAnalyseParam: ���ݷ����������࣬����һ����xml���ݽ���������FileAnalyseConfig���Ĺ���
* CDROriginal: ԭʼ����ʵ����
---
* **OrigiCdrFileParser**��CDR�����ļ�������
* **CmrFileParser**: CMR��¼������
* SpecallService: ԭʼ���������������
* CdrRecorderParser: ʶ�𲢷��ദ��
* CdrValidationManager: CDR�ļ�У�������
* BaseCdrFieldValidator: �����ֶ���Ч��У�����
* NormalBuffer: ���������
* CdrFieldConfigParser: CDR�ֶ�������
* AppResultCountManage: �ɼ��̴߳�����ͬ��������
## UC�����ֶη���
CallingNumber�����к���

## ������������
### CdrRecorderParser.flow() // ʶ�𲢷��ദ��������ڷ���
* MissCall: ����δ�����绰��
* Ignore: ����������͵Ļ���
* Split: ������Ҫ��ֵĻ���
* MergerSign: ������Ҫ�ϲ��Ļ���
* Common: ������ͨ�Ļ���

### MergerService // ʶ�𲢺ϲ�
* MeetingJion.mergerMeeting(); //�ϲ�Jion Meeting����
  CdrRecorderSaver.saveResult(); //�������ݵ�CDR��
  CDROriginalService.saveResult(); //����Ѵ���Ļ���
* Meeting.mergerMeeting(); //�ϲ�Meeting����
* Transferred.mergerTransferred(); //�ϲ�����ת��(Transferred)����
* Replaces.mergerReplaces(); //�ϲ�(Replaces)����
  CdrRecorderSaver.saveResult(); //�������ݵ�CDR��
  CDROriginalService.saveResult(); //����Ѵ���Ļ���

### UC�ֶ���Call Manager���ݿ��ֶν���
* configParam.getField(int j).getUCFieldName(); // CDR�����е��ֶ�
* configParam.getField(int j).getCMFieldName(); // CM���ݿ��ֶ�
* configParam.getField(j).getCMIndex(); // �ֶ�����Index

### ���ݿ��˵��
* COLLECTIONLOG: �����ɼ���־��¼����

### ���ط���

#### ��������ID��ȡ��Ӫ����Ϣ
`*GatewayCache.getSystemProviderByGetewayID*`
* ���ţ�133,153,180,189,10000,114
* �ƶ���134,135,136,137,138,139,147,150,151,152,157,158,159,182,183,187,188,10086,12580,12590
* ��ͨ��130,131,132,155,156,185,186,10011,10010
* ������*

#### ��������ID��ȡ���żƻ���Ϣ
`*GatewayCache.getCdrDialplanByGetewayID*`
![](/img/cdr_dialplan.png)

#### ��������ID��ȡ������
`*GatewayCache.getRateItemsInfoByGetewayID*`
GatewayRateitem->RateItem
![](/img/rate_items.png)

#### ��������ID��ȡ�������
`*getCdrFilternumByGetewayID*`
GatewayFilternum(GatewayFilternum)->CdrFilternum

#### ��������ID��ȡIP����ǰ׺
`*getIpPreNumbersByGetewayID*`
GatewayIpPreNum(���غ�����ǰ׺��ϵ��)->IpPreNumber
```
17911
17951
17909
```

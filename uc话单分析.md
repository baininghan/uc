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


# (UC)(http://naotu.baidu.com/viewshare.html?shareId=au1mgrpq9bsw)

## ServiceManageListener（系统配置监听器）

### 计费系统

#### CollectiontApp（话单采集服务）

#### SpecallService（原始话单分析处理服务）

#### AccountService（新规则批价服务）

#### Traficc（话单流程分析服务）

#### NewMissCallThread（未接来电服务）

#### CloudCallForwardSearchThread（呼叫转移搜索服务）

#### CloudCallForwardSetThread（呼叫转移设置服务）

### VOIP系统

#### CollectionApp（采集分析）

#### VoipAccountService（批价）

### 后台服务

#### 邮件告警

##### MailAlert（系统告警）

##### CDRCollectionAlert（话单采集告警）

#### SendReport（报表分发）

#### DBClear（数据库清理后台服务线程）

### Voizmate增值应用系统

#### TerminalObserverImpl（设备对象观察者）

#### CallObserverImpl（呼叫控制观察者）

#### ScheduleManager（邮件收取调度线程,用来控制收取邮件的任务分配和频率）

#### AlarmPush（个人提醒服务）

#### NotifyPush（通知服务）

#### GoogleCalendar（谷歌通知服务）

#### SmsAlertService（短信反馈服务）

### DB服务

#### DBBackup（数据库管理服务）

### License服务

#### CheckLicenseService（license检查服务线程）

### 日志服务

#### UClogsService（UC日志服务）

### LDAP服务

#### LdapSynchronize（LDAP服务）

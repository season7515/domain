# QueryTaskDetailHistory {#concept_gfr_tyk_c2b .concept}

QueryTaskDetailHistory：分页查询指定域名任务的详情历史列表。

## 请求参数 {#section_frj_dmm_c2b .section}

公共请求参数，详见[公共参数](intl.zh-CN/API 参考/调用方式/公共参数.md#)。

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是|操作接口名，系统规定参数，取值：QueryTaskDetailHistory。|
|PageSize|Integer|是|分页大小。|
|TaskNo|String|是|任务编号。|
|TaskStatus|Integer|可选|任务状态，枚举值范围：0 等待执行；1 执行中；2 成功；3 失败。|
|DomainName|String|可选|域名。|
|InstanceId|String|可选|域名实例编号。|
|DomainNameCursor|String|可选|域名游标。|
|TaskDetailNoCursor|String|可选|任务详情游标。|

## 返回参数 {#section_qkp_3mm_c2b .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|唯一请求识别码。|
|PageSize|Integer|分页大小。|
|CurrentPageCursor|[TaskDetailHistoryCurrentPageCursorType](#table_h14_nmm_c2b)|当前页游标。|
|NextPageCursor|[TaskDetailHistoryNextPageCursorType](#table_x2j_vmm_c2b)|下一页游标。|
|PrePageCursor|[TaskDetailHistoryPrePageCursorType](#table_e25_2nm_c2b)|上一页游标。|
|Objects|[TaskDetailHistoryType](#table_qrs_pnm_c2b)|任务详情信息。|

|类型|名称|描述|
|:-|:-|:-|
|String|TaskType|任务类型。枚举值范围： -   CHG\_HOLDER 修改所有者信息
-   CHG\_DNS 修改DNS
-   SET\_WHOIS\_PROTECT 设置隐私保护
-   UPDATE\_ADMIN\_CONTACT 修改管理者信息
-   UPDATE\_BILLING\_CONTACT 修改付费者信息
-   UPDATE\_TECH\_CONTACT 修改技术者信息
-   SET\_UPDATE\_PROHIBITED 设置域名安全锁
-   SET\_TRANSFER\_PROHIBITED 设置域名转移锁
-   ORDER\_ACTIVATE 创建注册订单
-   ORDER\_RENEW 创建续费订单
-   ORDER\_REDEEM 创建赎回订单
-   CREATE\_DNSHOST 创建DNS host
-   UPDATE\_DNSHOST 更新DNS host
-   SYNC\_DNSHOST同步DNS host

 |
|String|DomainName|域名。|
|String|InstanceId|域名实例编号。|
|String|TaskStatus|任务状态。可能值： -   WAITING\_EXECUTE 等待执行
-   EXECUTING 执行中
-   EXECUTE\_SUCCESS 执行成功
-   EXECUTE\_FAILURE 执行失败

 |
|String|TaskStatusCode|任务状态码。可能值： -   0 等待执行
-   1 执行中
-   2 执行成功
-   3 执行失败

 |
|String|CreateTime|任务创建时间。|
|String|UpdateTime|最近一次任务详情执行时间。|
|Integer|TryCount|任务详情重试次数。|
|String|TaskNo|任务编号。|
|String|TaskDetailNo|任务详情编号。|
|String|ErrorMsg|任务执行失败消息。|
|String|TaskTypeDescription|任务类型描述。|

|类型|名称|描述|
|:-|:-|:-|
|String|TaskType|任务类型。枚举值范围： -   CHG\_HOLDER 修改所有者信息
-   CHG\_DNS 修改DNS
-   SET\_WHOIS\_PROTECT 设置隐私保护
-   UPDATE\_ADMIN\_CONTACT 修改管理者信息
-   UPDATE\_BILLING\_CONTACT 修改付费者信息
-   UPDATE\_TECH\_CONTACT 修改技术者信息
-   SET\_UPDATE\_PROHIBITED 设置域名安全锁
-   SET\_TRANSFER\_PROHIBITED 设置域名转移锁
-   ORDER\_ACTIVATE 创建注册订单
-   ORDER\_RENEW 创建续费订单
-   ORDER\_REDEEM 创建赎回订单
-   CREATE\_DNSHOST 创建 DNS host
-   UPDATE\_DNSHOST 更新 DNS host
-   SYNC\_DNSHOST同步DNS host

 |
|String|DomainName|域名。|
|String|InstanceId|域名实例编号。|
|String|TaskStatus|任务状态。可能值： -   WAITING\_EXECUTE 等待执行
-   EXECUTING 执行中
-   EXECUTE\_SUCCESS 执行成功
-   EXECUTE\_FAILURE 执行失败

 |
|String|TaskStatusCode|任务状态码。可能值： -   0 等待执行
-   1 执行中
-   2 执行成功
-   3 执行失败

 |
|String|CreateTime|任务创建时间。|
|String|UpdateTime|最近一次任务详情执行时间。|
|Integer|TryCount|任务详情重试次数。|
|String|TaskNo|任务编号。|
|String|TaskDetailNo|任务详情编号。|
|String|ErrorMsg|任务执行失败消息。|
|String|TaskTypeDescription|任务类型描述。|

|类型|名称|描述|
|:-|:-|:-|
|String|TaskType|任务类型。枚举值范围： -   CHG\_HOLDER 修改所有者信息
-   CHG\_DNS 修改DNS
-   SET\_WHOIS\_PROTECT 设置隐私保护
-   UPDATE\_ADMIN\_CONTACT 修改管理者信息
-   UPDATE\_BILLING\_CONTACT 修改付费者信息
-   UPDATE\_TECH\_CONTACT 修改技术者信息
-   SET\_UPDATE\_PROHIBITED 设置域名安全锁
-   SET\_TRANSFER\_PROHIBITED 设置域名转移锁
-   ORDER\_ACTIVATE 创建注册订单
-   ORDER\_RENEW 创建续费订单
-   ORDER\_REDEEM 创建赎回订单
-   CREATE\_DNSHOST 创建DNS host
-   UPDATE\_DNSHOST 更新DNS host
-   SYNC\_DNSHOST 同步DNS host

 |
|String|DomainName|域名。|
|String|InstanceId|域名实例编号。|
|String|TaskStatus|任务状态，可能值： -   WAITING\_EXECUTE 等待执行
-   EXECUTING 执行中
-   EXECUTE\_SUCCESS 执行成功
-   EXECUTE\_FAILURE 执行失败

 |
|String|TaskStatusCode|任务状态，可能值： -   0 等待执行
-   1 执行中
-   2执行成功
-   3 执行失败

 |
|String|CreateTime|任务创建时间。|
|String|UpdateTime|最近一次任务详情执行时间。|
|Integer|TryCount|任务详情重试次数。|
|String|TaskNo|任务编号。|
|String|TaskDetailNo|任务详情编号。|
|String|ErrorMsg|任务执行失败消息。|
|String|TaskTypeDescription|任务类型描述。|

|类型|名称|描述|
|:-|:-|:-|
|String|TaskType|任务类型。枚举值范围： -   CHG\_HOLDER 修改所有者信息
-   CHG\_DNS 修改DNS
-   SET\_WHOIS\_PROTECT 设置隐私保护
-   UPDATE\_ADMIN\_CONTACT 修改管理者信息
-   UPDATE\_BILLING\_CONTACT 修改付费者信息
-   UPDATE\_TECH\_CONTACT 修改技术者信息
-   SET\_UPDATE\_PROHIBITED 设置域名安全锁
-   SET\_TRANSFER\_PROHIBITED 设置域名转移锁
-   ORDER\_ACTIVATE 创建注册订单
-   ORDER\_RENEW 创建续费订单
-   ORDER\_REDEEM 创建赎回订单
-   CREATE\_DNSHOST 创建DNS host
-   UPDATE\_DNSHOST 更新DNS host
-   SYNC\_DNSHOST 同步DNS host

 |
|String|DomainName|域名。|
|String|InstanceId|域名实例编号。|
|String|TaskStatus|任务状态。可能值： -   WAITING\_EXECUTE 等待执行
-   EXECUTING 执行中
-   EXECUTE\_SUCCESS 执行成功
-   EXECUTE\_FAILURE 执行失败

 |
|String|TaskStatusCode|任务状态码。可能值： -   0 等待执行
-   1 执行中
-   2 执行成功
-   3 执行失败

 |
|String|CreateTime|任务创建时间。|
|String|UpdateTime|最近一次任务详情执行时间。|
|Integer|TryCount|任务详情重试次数。|
|String|TaskNo|任务编号。|
|String|TaskDetailNo|任务详情编号。|
|String|ErrorMsg|任务执行失败消息。|
|String|TaskTypeDescription|任务类型描述。|

## 错误码 {#section_jwg_xnm_c2b .section}

|错误代码|描述|HTTP状态码|语义|
|:---|:-|:------|:-|
|ParameterIllegal|Parameter illegal.|400|参数错误。|
|NetworkIOError|Network IO Error.|400|网络I/O异常。|

## 示例 {#section_r31_24m_c2b .section}

**请求示例**

``` {#codeblock_6vr_me6_3q7}
http://domain-intl.aliyuncs.com/?Action=QueryTaskDetailHistory
&PageSize=1
&PageNum=1
&TaskNo=75addb07-28a3-450e-b5ec-test
&<公共请求参数>
```

**返回示例**

-   XML示例

    ``` {#codeblock_orb_p5o_ruo}
    <?xml version='1.0' encoding='UTF-8'?>
    <QueryTaskDetailHistoryResponse>
        <PageSize>2</PageSize>
        <RequestId>548CAE74-88F8-402F-8C12-97E747389C51</RequestId>
    </QueryTaskDetailHistoryResponse>
    ```

-   JSON示例

    ``` {#codeblock_m8s_w9d_bzo}
    {
      "currentPageCursor": {},
      "nextPageCursor": {},
      "objects": [],
      "pageSize": 2,
      "prePageCursor": {},
      "requestId": "CCE5DABB-48DF-403C-A7A1-A8F8B4F530CA"
    }
    ```



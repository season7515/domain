# SaveSingleTaskForCreatingOrderTransfer {#concept_h4f_mzk_c2b .concept}

SaveSingleTaskForCreatingOrderTransfer：提交域名转入任务，任务执行结果请通过查询任务详 [QueryTaskDetailList](cn.zh-CN/API 参考/域名管理接口/QueryTaskDetailList.md#)接口来查询。

## 请求参数 {#section_pvw_wxn_c2b .section}

|参数|类型|是否必选|示例值|描述|
|:-|:-|:---|:--|:-|
|AuthorizationCode|String|是|testCode|域名转入密码。|
|DomainName|String|是|test.com|域名。|
|RegistrantProfileId|Long|是|123456|已经实名认证域名信息模板ID。|
|Lang|String|否|en|接口返回错误信息语言，枚举值范围：zh 中文；en 英文。默认为 en。|
|PermitPremiumTransfer|Boolean|否|false|是否允许溢价词域名转入，默认为false。|
|UserClientIp|String|否|127.0.0.1|用户IP。|

## 返回参数 {#section_ph3_syn_c2b .section}

|参数|类型|示例值|描述|
|:-|:-|:--|:-|
|RequestId|String|40F46D3D-F4F3-4CCB-AC30-2DD20E32E528|唯一请求识别码。|
|TaskNo|String|3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8|任务编号。|

## 示例 {#section_lqw_5yn_c2b .section}

**请求示例**

``` {#codeblock_slt_dpv_bzn}
/?Action=SaveSingleTaskForCreatingOrderTransfer
&AuthorizationCode=testCode
&DomainName=test.com
&RegistrantProfileId=123456
&PermitPremiumTransfer=false
&<公共请求参数>
```

**正常返回示例**

-   XML示例

    ``` {#codeblock_c5g_cs9_2q0}
    <SaveSingleTaskForCreatingOrderTransferResponse>
      <TaskNo>57fbc841-c4e5-4a23-8ed6-315091d0c40e</TaskNo>
      <RequestId>21AF4F6F-1924-408B-BF83-88FEFA9CEF2B</RequestId>
    </SaveSingleTaskForCreatingOrderTransferResponse>
    ```

-   JSON示例

    ``` {#codeblock_m29_dnv_4sg}
    {
        "RequestId":"492D1868-1384-4219-8F8B-7EB44534A72A",
        "TaskNo":"939b6918-be3b-4c4f-b949-93553da52dca"
    }
    ```


**异常返回示例**

-   XML示例

    ``` {#codeblock_ehw_ojq_g2g}
    <Error>
      <RequestId>4149E915-CD99-4C77-9D6D-58A3E58E8135</RequestId>
      <HostId>domain.aliyuncs.com</HostId>
      <Code>TaskIsBeingProcessed</Code>
      <Message>An operation is being processed. Please try again later.</Message>
    </Error>
    ```

-   JSON示例

    ``` {#codeblock_koh_lr3_v6g}
    {
        "Code":"TaskIsBeingProcessed",
        "HostId":"domain.aliyuncs.com",
        "Message":"An operation is being processed. Please try again later.",
        "RequestId":"CF7F1EC6-9BE0-4B96-968A-4982EE813647"
    }
    ```


## 错误码 {#section_nwb_jcr_b2b .section}

[单击查看本产品错误码](cn.zh-CN/API 参考/附录/错误代码表.md#)。


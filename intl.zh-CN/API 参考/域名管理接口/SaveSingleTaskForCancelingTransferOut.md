# SaveSingleTaskForCancelingTransferOut {#concept_cpf_jzk_c2b .concept}

SaveSingleTaskForCancelingTransferOut：提交取消域名转出任务，任务执行结果请通过查询任务详情[QueryTaskDetailList](intl.zh-CN/API 参考/域名管理接口/QueryTaskDetailList.md#)接口来查询。

## 请求参数 {#section_u5j_gsn_c2b .section}

|参数|类型|是否必选|示例值|描述|
|:-|:-|:---|:--|:-|
|DomainName|String|是|test.com|域名。|
|Lang|String|否|en|接口返回错误信息语言，枚举值范围：zh 中文；en 英文。默认为 en。|
|UserClientIp|String|否|127.0.0.1|用户IP。|

## 返回参数 {#section_ggj_4sn_c2b .section}

|参数|类型|示例值|描述|
|:-|:-|:--|:-|
|RequestId|String|40F46D3D-F4F3-4CCB-AC30-2DD20E32E528|唯一请求识别码。|
|TaskNo|String|3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8|任务编号。|

## 示例 {#section_of5_405_b2b .section}

**请求示例**

``` {#codeblock_p3l_nd7_oup}
/?Action=SaveSingleTaskForCancelingTransferOut
&DomainName=test.com
&<公共请求参数>
```

**正常返回示例**

-   XML示例

    ``` {#codeblock_nx9_8ft_poe}
    <SaveSingleTaskForCancelingTransferOutResponse>
      <TaskNo>3bdbaa0e-faa2-4ad2-98f4-bcfeb0237054</TaskNo>
      <RequestId>EEB28AA7-6051-4E71-B2CC-DAAFB2DF6BCA</RequestId>
    </SaveSingleTaskForCancelingTransferOutResponse>e>
    ```

-   JSON示例

    ``` {#codeblock_mji_io2_7z6}
    {
        "RequestId":"492D1868-1384-4219-8F8B-7EB44534A72A",
        "TaskNo":"939b6918-be3b-4c4f-b949-93553da52dca"
    }
    ```


**异常返回示例**

-   XML示例

    ``` {#codeblock_en2_xth_1km}
    <Error>
      <RequestId>4149E915-CD99-4C77-9D6D-58A3E58E8135</RequestId>
      <HostId>domain.aliyuncs.com</HostId>
      <Code>TaskIsBeingProcessed</Code>
      <Message>An operation is being processed. Please try again later.</Message>
    </Error>
    ```

-   JSON示例

    ``` {#codeblock_brj_u7k_3vd}
    {
        "Code":"TaskIsBeingProcessed",
        "HostId":"domain.aliyuncs.com",
        "Message":"An operation is being processed. Please try again later.",
        "RequestId":"CF7F1EC6-9BE0-4B96-968A-4982EE813647"
    }
    ```


## 错误码 {#section_nwb_405_b2b .section}

[单击查看本产品错误码](intl.zh-CN/API 参考/附录/错误代码表.md#)。


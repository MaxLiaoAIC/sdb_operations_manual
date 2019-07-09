"# sdb_operations_manual" 

# Up
``` xml
<?xml version="1.0" encoding="UTF-8"?>
<ns0:ServiceEnvelope xmlns:ns0="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceEnvelope">
    <ns1:ServiceHeader xmlns:ns1="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceHeader">
        <ns1:StandardType></ns1:StandardType>
        <ns1:StandardVersion></ns1:StandardVersion>
        <ns1:ServiceName>csCstmrTpInq</ns1:ServiceName>
        <ns1:ServiceVersion>01</ns1:ServiceVersion>
        <ns1:SourceID>TWMPB</ns1:SourceID>
        <ns1:TransactionID>INEB201907051655089</ns1:TransactionID>
        <ns1:RqTimestamp>2019-07-09T10:56:15.11+08:00</ns1:RqTimestamp>
    </ns1:ServiceHeader>
    <ns1:ServiceBody xmlns:ns1="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceBody">
        <ns2:csCstmrTpInqRq xmlns:ns2="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/BSMF/csCstmrTpInqRq/01">
            <ns2:REQHDR>
                <ns2:TrnNum>INEB201907031655089</ns2:TrnNum>
                <ns2:TrnCode>JCGU028</ns2:TrnCode>
            </ns2:REQHDR>
            <ns2:REQBDY>
                <ns2:Mobile>0912345678</ns2:Mobile>
                <ns2:Count>0000</ns2:Count>
                <ns2:CustName>哈哈</ns2:CustName>
                <ns2:BirthDt>19900102</ns2:BirthDt>
                <ns2:CustId>B101063165</ns2:CustId>
                <ns2:FunCode>Y</ns2:FunCode>
            </ns2:REQBDY>
        </ns2:csCstmrTpInqRq>
    </ns1:ServiceBody>
</ns0:ServiceEnvelope>
```

# down
``` xml 
<?xml version="1.0" encoding="UTF-8"?>
<ns0:ServiceEnvelope xmlns:ns0="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceEnvelope">
    <ns1:ServiceHeader xmlns:ns1="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceHeader">
        <ns1:StandardType/>
        <ns1:StandardVersion/>
        <ns1:TrackingID>iOCPnRKDpXztRkR3vM0YGQg-Aos</ns1:TrackingID>
        <ns1:ServiceName>csCstmrTpInq</ns1:ServiceName>
        <ns1:ServiceVersion>01</ns1:ServiceVersion>
        <ns1:SourceID>TWMPB</ns1:SourceID>
        <ns1:TransactionID>INEB201907051655089</ns1:TransactionID>
        <ns1:RsTimestamp>2019-07-09T18:20:45.365+08:00</ns1:RsTimestamp>
        <ns1:StatusCode>0</ns1:StatusCode>
    </ns1:ServiceHeader>
    <ns1:ServiceBody xmlns:ns0="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceEnvelope" xmlns:ns1="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceBody">
        <ns2:csCstmrTpInqRs xmlns:ns2="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/BSMF/csCstmrTpInqRs/01">
            <ns2:RESHDR>
                <ns2:RspCode>9999</ns2:RspCode>
                <ns2:TrnNum>INEB201907051655089</ns2:TrnNum>
                <ns2:CustId>B101063165</ns2:CustId>
            </ns2:RESHDR>
            <ns2:RESBDY>
                <ns2:BDYREC>
                    <ns2:CustIND>X</ns2:CustIND>
                    <ns2:IDFlag/>
                    <ns2:MobileFlag/>
                    <ns2:OffPhoneFlag/>
                    <ns2:CustName>哈哈</ns2:CustName>
                    <ns2:Mobile>0912345678</ns2:Mobile>
                </ns2:BDYREC>
            </ns2:RESBDY>
            <ns2:RESTLR/>
        </ns2:csCstmrTpInqRs>
    </ns1:ServiceBody>
</ns0:ServiceEnvelope>
```
# AES Key
CC7161BD8FA9955DD391E988995930E572A1E16EDCDDF58AF7A5245E26B48B3E

# AES down
``` xml
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
    <soap:Body>
        <invokeResponse xmlns="http://insp.chinatrust.com.tw/ws/CryptoService">
            <SecurityProviderResponse xmlns="http://insp.chinatrust.com.tw">
                <Header>
                    <SystemCode>0</SystemCode>
                    <TxCode>OB20190709000001</TxCode>
                    <Function>RSADecryptData</Function>
                </Header>
                <Body>
                    <ReturnCode>0</ReturnCode>
                    <ErrorCode>SECPS0000</ErrorCode>
                    <Detail>SUIPSrvRSAUnwrapData OK.</Detail>
                    <PlainText>
                        <Type>HEX</Type>
                        <Value>51304D334D545978516B5134526B45354F5455315245517A4F5446464F5467344F546B314F544D77525455334D6B45785254453252555244524552474E546842526A64424E5449304E5555794E6B49304F45497A52513D3D</Value>
                    </PlainText>
                </Body>
            </SecurityProviderResponse>
        </invokeResponse>
    </soap:Body>
</soap:Envelope>
```
# 綁卡

``` json
{
    "Response": {
        "Header": {
            "ServiceResult": "Y",
            "StatusCode": "I0000",
            "StatusDesc": "作業成功",
            "ResponseTime": "2019/07/09 12:45:21",
            "AdditionalInfo": ""
        },
        "Data": {
            "CardSeq": "CS0000000001364187",
            "WalletStatusCode": "I0000",
            "WalletStatusDesc": "作業成功"
        }
    }
}
```
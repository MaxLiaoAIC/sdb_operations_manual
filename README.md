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
# verify OTP
http://10.242.136.101:8080/api/verifyOtpTest?txCode=OB10907300000001&authCode=6451106&secData=MemoryTokenStore:oRv7ta29Zy

# RSA 上
``` xml 
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
   <SOAP-ENV:Header />
   <SOAP-ENV:Body>
      <ns3:invoke xmlns:ns3="http://insp.chinatrust.com.tw/ws/CryptoService" xmlns:ns2="http://insp.chinatrust.com.tw">
         <ns2:SecurityProvider>
            <ns2:Header>
               <ns2:TxCode>testTrnCode</ns2:TxCode>
               <ns2:Function>RSADecryptData</ns2:Function>
            </ns2:Header>
            <ns2:Body>
               <ns2:BizID>mpb</ns2:BizID>
               <ns2:KeyID>mpbobrsakey2048</ns2:KeyID>
               <ns2:PlainType>HEX</ns2:PlainType>
               <ns2:WrapData>
                  <ns2:Type>HEX</ns2:Type>
                  <ns2:Value>88d10876c84a4ea7b30075c01676cef308671939d06b32eb69ba214fa7da4e9d47a266c387404512bddba5f955aaaf988c3b4ce8f053d8cc1bd05f088b0a202260a636618bca4a9b3d90973376e3b2b0e9238b3a5cab1a0d8a2452db792e96ad155a974264f83950ee3ebc7a98aa3d0406b44beaca743f0bcce1fc71f671a431121740dcf8dc89ccc105b9aca36483117e75fde5390f9acb3901494fa6c190b60d6de6877e004824ddd8bb2e386b5cf2590db2810478556f10fea4c46b75bcefa00c3c195b60713135ccef23d75180dd25621183bf3dfbcffd4e0515b0180010f91933efe3deec21245d32b84911ade851ef6ea6af18b727161a7693444bfb97</ns2:Value>
               </ns2:WrapData>
            </ns2:Body>
         </ns2:SecurityProvider>
      </ns3:invoke>
   </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

# 下
``` xml
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
    <soap:Body>
        <invokeResponse xmlns="http://insp.chinatrust.com.tw/ws/CryptoService">
            <SecurityProviderResponse xmlns="http://insp.chinatrust.com.tw">
                <Header>
                    <SystemCode>0</SystemCode>
                    <TxCode>testTrnCode</TxCode>
                    <Function>RSADecryptData</Function>
                </Header>
                <Body>
                    <ReturnCode>12</ReturnCode>
                    <ErrorCode>SECPS4006</ErrorCode>
                    <Detail>RSAOperation.decrypt CTCB.mpb.mpbobrsakey2048.SIGN.SERVER Exception: Too much data passed to this cipher for current key length and padding. Maximum data size is: 256</Detail>
                </Body>
            </SecurityProviderResponse>
        </invokeResponse>
    </soap:Body>
</soap:Envelope>
```

# sendotp
# up
``` xml
 <?xml version="1.0" encoding="UTF-8" standalone="yes"?><SecurityProvider xmlns="http://insp.chinatrust.com.tw" xmlns:ns2="http://insp.chinatrust.com.tw/ws/CryptoService"><Header><TxCode>OB19070300000001</TxCode><Function>OneTimeSMSOTP</Function></Header><Body><BizID>MPB</BizID><KeyID>SMSOTPKey</KeyID><SessionID>sessionId</SessionID><Method>genOTP</Method><TransID>OTP0001</TransID><PhoneNO>0932219769</PhoneNO><ChannelType>MPB</ChannelType><SMSText></SMSText><SMSTemplateID>OTPSMS_61</SMSTemplateID><MessageType>NBSMSSTOTP</MessageType></Body></SecurityProvider>
 ```
 
# down
``` xml
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<SecurityProviderResponse xmlns="http://insp.chinatrust.com.tw">
    <Header>
        <SystemCode>0</SystemCode>
        <TxCode>OB19070300000001</TxCode>
        <Function>OneTimeSMSOTP</Function>
    </Header>
    <Body>
        <ReturnCode>0</ReturnCode>
        <ErrorCode>HSMCE00</ErrorCode>
        <Detail>genOTP ok.</Detail>
        <SecData>MemoryTokenStore:gmyF1q8Rvn</SecData>
        <Sac>SISA</Sac>
    </Body>
</SecurityProviderResponse>
```

# 20190712
# 取得姓用卡EMS錯誤
```xml
<?xml version="1.0" encoding="UTF-8"?>
<ServiceEnvelope xmlns="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceEnvelope">
   <wstxns1:ServiceHeader xmlns:wstxns1="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceHeader">
      <wstxns1:StandardType />
      <wstxns1:StandardVersion />
      <wstxns1:ServiceName>ccMobPayAvlBndListInq</wstxns1:ServiceName>
      <wstxns1:ServiceVersion>01</wstxns1:ServiceVersion>
      <wstxns1:SourceID>TWMPB</wstxns1:SourceID>
      <wstxns1:RqTimestamp>2019-07-09T10:56:15.11+08:00</wstxns1:RqTimestamp>
   </wstxns1:ServiceHeader>
   <wstxns2:ServiceBody xmlns:wstxns2="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceBody">
      <wstxns3:ccMobPayAvlBndListInqRq xmlns:wstxns3="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/BSMF/ccMobPayAvlBndListInqRq/01">
         <wstxns3:REQHDR>
            <wstxns3:SystemId>JCKZ</wstxns3:SystemId>
            <wstxns3:TrnProg>JCGU176</wstxns3:TrnProg>
         </wstxns3:REQHDR>
         <wstxns3:REQBDY>
            <wstxns3:Channel>INET</wstxns3:Channel>
            <wstxns3:UserId>benLTest</wstxns3:UserId>
            <wstxns3:FunctionCode />
            <wstxns3:LineCnt>1</wstxns3:LineCnt>
            <wstxns3:MaxLineCnt>15</wstxns3:MaxLineCnt>
            <wstxns3:CustNbr>A100049008</wstxns3:CustNbr>
            <wstxns3:NextKeyCpcck>1234567890</wstxns3:NextKeyCpcck>
            <wstxns3:NextKeyApfk>123456</wstxns3:NextKeyApfk>
            <wstxns3:FILLER />
         </wstxns3:REQBDY>
      </wstxns3:ccMobPayAvlBndListInqRq>
   </wstxns2:ServiceBody>
</ServiceEnvelope>
```

```xml
<?xml version="1.0" encoding="UTF-8"?>
<ns0:ServiceEnvelope xmlns:ns0="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceEnvelope">
   <ns1:ServiceHeader xmlns:ns1="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceHeader">
      <ns1:StandardType />
      <ns1:StandardVersion />
      <ns1:TrackingID>onQ6cBWYtKLSxkYWaa0YGrF-Aos</ns1:TrackingID>
      <ns1:ServiceName>ccMobPayAvlBndListInq</ns1:ServiceName>
      <ns1:ServiceVersion>01</ns1:ServiceVersion>
      <ns1:SourceID>TWMPB</ns1:SourceID>
      <ns1:RsTimestamp>2019-07-12T16:56:27.605+08:00</ns1:RsTimestamp>
      <ns1:StatusCode>1</ns1:StatusCode>
   </ns1:ServiceHeader>
   <ns1:ServiceError xmlns:ns1="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceError">
      <ns2:Error xmlns:ns2="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/Common">
         <ns2:ErrorType>SYSTEM</ns2:ErrorType>
         <ns2:ErrorCode>E903</ns2:ErrorCode>
         <ns2:Timestamp>2019-07-12T16:56:27.602+08:00</ns2:Timestamp>
         <ns2:ErrorMessage>The requested ESB service is not implemented (Operation=) at this moment. ProcessStack=CoreServices/BusinessServices/CreditCard/ccMobPayAvlBndListInq/Ver01/JMSStarter.process/ServiceImplEntry&gt;CoreServices/BaseProcesses/SubProcesses/ImplDispatcher.process/SvcImplEntry&gt;CoreServices/BusinessServices/CreditCard/ccMobPayAvlBndListInq/Ver01/ServiceImplEntry.process/Interaction&gt;CoreServices/BaseProcesses/Patterns/SingleRqRs/SingleRqRs01.process/RsTransform</ns2:ErrorMessage>
         <ns2:ErrorContext />
      </ns2:Error>
   </ns1:ServiceError>
</ns0:ServiceEnvelope>
```
# 正確測試電文
88d10876c84a4ea7b30075c01676cef308671939d06b32eb69ba214fa7da4e9d47a266c387404512bddba5f955aaaf988c3b4ce8f053d8cc1bd05f088b0a202260a636618bca4a9b3d90973376e3b2b0e9238b3a5cab1a0d8a2452db792e96ad155a974264f83950ee3ebc7a98aa3d0406b44beaca743f0bcce1fc71f671a431121740dcf8dc89ccc105b9aca36483117e75fde5390f9acb3901494fa6c190b60d6de6877e004824ddd8bb2e386b5cf2590db2810478556f10fea4c46b75bcefa00c3c195b60713135ccef23d75180dd25621183bf3dfbcffd4e0515b0180010f91933efe3deec21245d32b84911ade851ef6ea6af18b727161a7693444bfb97

```xml
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<SecurityProvider xmlns="http://insp.chinatrust.com.tw" xmlns:ns2="http://insp.chinatrust.com.tw/ws/CryptoService">
    <Header>
        <TxCode>OB20190712175931</TxCode>
        <Function>OneTimeSMSOTP</Function>
    </Header>
    <Body>
        <BizID>MPB</BizID>
        <KeyID>SMSOTPKey</KeyID>
        <SecData>MemoryTokenStore:_tx__6AGkX</SecData>
        <SessionID></SessionID>
        <Method>verifyOTP</Method>
        <TransID>123456789</TransID>
        <PhoneNO>0912345678</PhoneNO>
        <AuthCode>3552513</AuthCode>
        <ChannelType>MPB</ChannelType>
        <SMSText></SMSText>
        <SMSTemplateID>OTPSMS_61</SMSTemplateID>
        <MessageType>NBSMSSTOTP</MessageType>
    </Body>
</SecurityProvider>
```
# 密碼傳送錯誤
```xml
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<SecurityProviderResponse xmlns="http://insp.chinatrust.com.tw">
    <Header>
        <SystemCode>0</SystemCode>
        <TxCode>OB20190712180200</TxCode>
        <Function>OneTimeSMSOTP</Function>
    </Header>
    <Body>
        <ReturnCode>20</ReturnCode>
        <ErrorCode>HSMCE23</ErrorCode>
        <Detail>[10020]</Detail>
    </Body>
</SecurityProviderResponse>
# 輸入錯誤sacData

```xml
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<SecurityProviderResponse xmlns="http://insp.chinatrust.com.tw">
    <Header>
        <SystemCode>0</SystemCode>
        <TxCode>OB20190712180539</TxCode>
        <Function>OneTimeSMSOTP</Function>
    </Header>
    <Body>
        <ReturnCode>20</ReturnCode>
        <ErrorCode>HSMCE01</ErrorCode>
        <Detail>ChannelType is illegal.</Detail>
    </Body>
</SecurityProviderResponse>
```

# 輸入錯誤電話號碼
```xml
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<SecurityProviderResponse xmlns="http://insp.chinatrust.com.tw">
    <Header>
        <SystemCode>0</SystemCode>
        <TxCode>OB20190712181513</TxCode>
        <Function>OneTimeSMSOTP</Function>
    </Header>
    <Body>
        <ReturnCode>20</ReturnCode>
        <ErrorCode>HSMCE29</ErrorCode>
        <Detail>&lt;resultcode=0002|errormsg=Illegal Argument. - MOBILENO must be 10 digits|MessageId=null&gt;</Detail>
    </Body>
</SecurityProviderResponse>
```

# 20190716
```xml
<?xml version="1.0" encoding="UTF-8"?>
<ns0:ServiceEnvelope xmlns:ns0="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceEnvelope">
    <ns1:ServiceHeader xmlns:ns1="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceHeader">
        <ns1:StandardType/>
        <ns1:StandardVersion/>
        <ns1:TrackingID>Y4BZEs05y9/lYEvSOV0YHCrEAos</ns1:TrackingID>
        <ns1:ServiceName>ccMobPayAvlBndListInq</ns1:ServiceName>
        <ns1:ServiceVersion>01</ns1:ServiceVersion>
        <ns1:SourceID>TWMPB</ns1:SourceID>
        <ns1:RsTimestamp>2019-07-16T10:50:42.067+08:00</ns1:RsTimestamp>
        <ns1:StatusCode>0</ns1:StatusCode>
    </ns1:ServiceHeader>
    <ns1:ServiceBody xmlns:ns0="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceEnvelope" xmlns:ns1="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceBody">
        <ns2:ccMobPayAvlBndListInqRs xmlns:ns2="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/BSMF/ccMobPayAvlBndListInqRs/01">
            <ns2:RESHDR>
                <ns2:SystemId>JCKZ</ns2:SystemId>
                <ns2:TrnProg>JCGU176</ns2:TrnProg>
            </ns2:RESHDR>
            <ns2:RESBDY>
                <ns2:BDYREC>
                    <ns2:MessageType>0001</ns2:MessageType>
                    <ns2:LineCnt>0002</ns2:LineCnt>
                    <ns2:MaxLineCnt>15</ns2:MaxLineCnt>
                    <ns2:CustNbr>A100049008</ns2:CustNbr>
                    <ns2:NextKeyCpcck>1234567890</ns2:NextKeyCpcck>
                    <ns2:NextKeyApfk/>
                    <ns2:ChiName>TEST</ns2:ChiName>
                    <ns2:Email>TEST@TEST.COM</ns2:Email>
                    <ns2:MobilePhone>0912345678</ns2:MobilePhone>
                    <ns2:BirthDay>19370108</ns2:BirthDay>
                    <ns2:CardNo>5239531003311038</ns2:CardNo>
                    <ns2:CardExpire>0824</ns2:CardExpire>
                    <ns2:CustNo>A100049008</ns2:CustNo>
                    <ns2:CardHolderInd>0</ns2:CardHolderInd>
                    <ns2:BlockCode/>
                    <ns2:AfinityCode>8700</ns2:AfinityCode>
                    <ns2:AfgpBrfName>中華電信聯名卡</ns2:AfgpBrfName>
                    <ns2:OpenFlag>N</ns2:OpenFlag>
                    <ns2:CardKind>C</ns2:CardKind>
                    <ns2:CardType>670</ns2:CardType>
                    <ns2:CardBrade>M</ns2:CardBrade>
                    <ns2:CardGrade>E</ns2:CardGrade>
                    <ns2:CardArt>670870060</ns2:CardArt>
                    <ns2:CardOpnDte>20190527</ns2:CardOpnDte>
                    <ns2:CardFstApplFlg>Y</ns2:CardFstApplFlg>
                    <ns2:CardArmr/>
                    <ns2:DualCode/>
                    <ns2:FILLER/>
                </ns2:BDYREC>
            </ns2:RESBDY>
            <ns2:RESTLR/>
        </ns2:ccMobPayAvlBndListInqRs>
    </ns1:ServiceBody>
</ns0:ServiceEnvelope>
```
# ccCardProfAud

### up
``` xml   
<?xml version="1.0" encoding="UTF-8"?>
<sev:ServiceEnvelope xmlns:sev="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceEnvelope">
	<ServiceHeader xmlns="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceHeader">
		<ServiceName>ccCardProfAud</ServiceName>
		<ServiceVersion>01</ServiceVersion>
		<SourceID>TWMPB</SourceID>
		<TransactionID>TWMPB201908213013055</TransactionID>
		<RqTimestamp>2019-08-21T10:44:43.445+08:00</RqTimestamp>
	</ServiceHeader>
	<sbo:ServiceBody xmlns:sbo="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceBody">
		<ccCardProfAudRq xmlns="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/BSMF/ccCardProfAudRq/01">
			<REQHDR>
				<TrnNum>TWMPB201908213013055</TrnNum>
				<TrnCode>JCGU839</TrnCode>
			</REQHDR>
			<REQBDY>
				<CustId>A112618880</CustId>
				<CustBirthday>19800101</CustBirthday>
				<UserId>NETBANK</UserId>
				<FunctionCode>1</FunctionCode>
			</REQBDY>
		</ccCardProfAudRq>
	</sbo:ServiceBody>
</sev:ServiceEnvelope>
```

### down
``` xml
<ns0:ServiceEnvelope xmlns:ns0="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceEnvelope">
    <ns1:ServiceHeader xmlns:ns1="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceHeader">
        <ns1:TrackingID>hiDAGXp5gUzfCE7pBS0YG7S-Aos</ns1:TrackingID>
        <ns1:ServiceName>ccCardProfAud</ns1:ServiceName>
        <ns1:ServiceVersion>01</ns1:ServiceVersion>
        <ns1:SourceID>TWMPB</ns1:SourceID>
        <ns1:TransactionID>TWMPB201908213013055</ns1:TransactionID>
        <ns1:RsTimestamp>2019-08-21T10:44:43.499+08:00</ns1:RsTimestamp>
        <ns1:StatusCode>0</ns1:StatusCode>
    </ns1:ServiceHeader>
    <ns1:ServiceBody xmlns:ns0="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceEnvelope" xmlns:ns1="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceBody">
        <ns2:ccCardProfAudRs xmlns:ns2="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/BSMF/ccCardProfAudRs/01">
            <ns2:RESHDR>
                <ns2:RspCode>0001</ns2:RspCode>
                <ns2:TrnNum>TWMPB201908213013055</ns2:TrnNum>
                <ns2:CustId>A112618880</ns2:CustId>
            </ns2:RESHDR>
            <ns2:RESBDY>
                <ns2:BDYREC>
                    <ns2:CardNoFlg/>
                    <ns2:CustIdFlg>#</ns2:CustIdFlg>
                    <ns2:CustNameFlg/>
                    <ns2:CustBirthFlg>Y</ns2:CustBirthFlg>
                    <ns2:TelFlg/>
                    <ns2:MobilePhoneNoFlg/>
                    <ns2:AddrCityFlg/>
                    <ns2:AddrFlg/>
                    <ns2:ExpDt/>
                    <ns2:ExpDtFlg/>
                    <ns2:CVV2Flg/>
                    <ns2:AffintyCode/>
                    <ns2:AFGP_BRFName/>
                    <ns2:ErrorDesc>交易成功</ns2:ErrorDesc>
                    <ns2:BirthDt>19800101</ns2:BirthDt>
                    <ns2:MobilNbr>0912345678</ns2:MobilNbr>
                    <ns2:UserId>NETBANK</ns2:UserId>
                    <ns2:FunctionCode>1</ns2:FunctionCode>
                </ns2:BDYREC>
            </ns2:RESBDY>
            <ns2:RESTLR/>
        </ns2:ccCardProfAudRs>
    </ns1:ServiceBody>
</ns0:ServiceEnvelope>	
```

### down error: ACL
``` xml
<?xml version="1.0" encoding="UTF-8"?>
<ns0:ServiceEnvelope xmlns:ns0="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceEnvelope">
   <ns1:ServiceHeader xmlns:ns1="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceHeader">
      <ns1:StandardType />
      <ns1:StandardVersion />
      <ns1:TrackingID />
      <ns1:ServiceName>ccCardProfAud</ns1:ServiceName>
      <ns1:ServiceVersion>01</ns1:ServiceVersion>
      <ns1:SourceID>TWMPB</ns1:SourceID>
      <ns1:ChannelID />
      <ns1:TransactionID>TWMPB201908213013055</ns1:TransactionID>
      <ns1:RsTimestamp>2019-08-23T15:56:05.71+08:00</ns1:RsTimestamp>
      <ns1:StatusCode>1</ns1:StatusCode>
   </ns1:ServiceHeader>
   <ns1:ServiceError xmlns:ns1="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceError">
      <ns2:Error xmlns:ns2="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/Common">
         <ns2:ErrorType>PRIVILEGE</ns2:ErrorType>
         <ns2:ErrorCode>E906</ns2:ErrorCode>
         <ns2:ErrorMessage>AccessManager:The requested service is not authorized for the service client</ns2:ErrorMessage>
      </ns2:Error>
   </ns1:ServiceError>
</ns0:ServiceEnvelope>
```

### 20190905 up
``` xml
<?xml version="1.0" encoding="UTF-8"?>
<ns0:ServiceEnvelope xmlns:ns0="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceEnvelope">
   <ns1:ServiceHeader xmlns:ns1="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceHeader">
      <ns1:StandardType>BSMF</ns1:StandardType>
      <ns1:StandardVersion>01</ns1:StandardVersion>
      <ns1:ServiceName>ccCardProfAud</ns1:ServiceName>
      <ns1:ServiceVersion>01</ns1:ServiceVersion>
      <ns1:SourceID>MPB</ns1:SourceID>
      <ns1:TransactionID>MPB201909041506487</ns1:TransactionID>
      <ns1:RqTimestamp>2019-09-04T15:07:09.11+08:00</ns1:RqTimestamp>
   </ns1:ServiceHeader>
   <ns1:ServiceBody xmlns:ns1="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceBody">
      <ns2:ccCardProfAudRq xmlns:ns2="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/BSMF/ccCardProfAudRq/01">
         <ns2:REQHDR>
            <ns2:TrnNum>MPB201909041506487</ns2:TrnNum>
            <ns2:TrnCode>JCGU839</ns2:TrnCode>
         </ns2:REQHDR>
         <ns2:REQBDY>
            <ns2:ExpDt />
            <ns2:CardNo />
            <ns2:CustId>B101063165</ns2:CustId>
            <ns2:MobilePhoneNo />
            <ns2:TelAreaCode />
            <ns2:TrnDate />
            <ns2:TrnTime />
            <ns2:TelNo />
            <ns2:Addr />
            <ns2:CVV2>XXXXX</ns2:CVV2>
            <ns2:CustBirthday>19900102</ns2:CustBirthday>
            <ns2:FunctionCode>5</ns2:FunctionCode>
            <ns2:AddrCity />
            <ns2:UserId>NETBANK</ns2:UserId>
            <ns2:CustName />
         </ns2:REQBDY>
      </ns2:ccCardProfAudRq>
   </ns1:ServiceBody>
</ns0:ServiceEnvelope>
```

### up success
``` xml
<?xml version="1.0" encoding="UTF-8"?>
<ns0:ServiceEnvelope xmlns:ns0="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceEnvelope">
   <ns1:ServiceHeader xmlns:ns1="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceHeader">
      <ns1:StandardType>BSMF</ns1:StandardType>
      <ns1:StandardVersion>01</ns1:StandardVersion>
      <ns1:TrackingID>b2G7PoARzqN1zUw6b20YH2h-Aos</ns1:TrackingID>
      <ns1:ServiceName>ccCardProfAud</ns1:ServiceName>
      <ns1:ServiceVersion>01</ns1:ServiceVersion>
      <ns1:SourceID>MPB</ns1:SourceID>
      <ns1:TransactionID>MPB201909041506487</ns1:TransactionID>
      <ns1:RsTimestamp>2019-09-05T11:09:48.11+08:00</ns1:RsTimestamp>
      <ns1:StatusCode>0</ns1:StatusCode>
   </ns1:ServiceHeader>
   <ns1:ServiceBody xmlns:ns1="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceBody">
      <ns2:ccCardProfAudRs xmlns:ns2="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/BSMF/ccCardProfAudRs/01">
         <ns2:RESHDR>
            <ns2:RspCode>0001</ns2:RspCode>
            <ns2:TrnNum>MPB201909041506487</ns2:TrnNum>
            <ns2:CustId>B101063165</ns2:CustId>
         </ns2:RESHDR>
         <ns2:RESBDY>
            <ns2:BDYREC>
               <ns2:CardNoFlg />
               <ns2:CustIdFlg>#</ns2:CustIdFlg>
               <ns2:CustNameFlg />
               <ns2:CustBirthFlg>Y</ns2:CustBirthFlg>
               <ns2:TelFlg />
               <ns2:MobilePhoneNoFlg />
               <ns2:AddrCityFlg />
               <ns2:AddrFlg />
               <ns2:ExpDt />
               <ns2:ExpDtFlg />
               <ns2:CVV2Flg />
               <ns2:AffintyCode />
               <ns2:AFGP_BRFName />
               <ns2:ErrorDesc>交易成功</ns2:ErrorDesc>
               <ns2:BirthDt>19900102</ns2:BirthDt>
               <ns2:MobilNbr>0912345678</ns2:MobilNbr>
               <ns2:UserId>NETBANK</ns2:UserId>
               <ns2:FunctionCode>5</ns2:FunctionCode>
            </ns2:BDYREC>
         </ns2:RESBDY>
         <ns2:RESTLR />
      </ns2:ccCardProfAudRs>
   </ns1:ServiceBody>
</ns0:ServiceEnvelope>
```

# ebShrtenUrlAdd 

### up
``` xml
<?xml version="1.0" encoding="UTF-8"?>
<sev:ServiceEnvelope xmlns:sev="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceEnvelope">
                <ns0:ServiceHeader xmlns:ns0="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceHeader">
                <ns0:ServiceName>ebShrtenUrlAdd</ns0:ServiceName>
                <ns0:ServiceVersion>01</ns0:ServiceVersion>
                <ns0:SourceID>EBMWEB</ns0:SourceID>
                <ns0:TransactionID>WB20190823002628718</ns0:TransactionID>
                <ns0:RqTimestamp>2019-08-23T10:05:07.045+08:00</ns0:RqTimestamp>
        </ns0:ServiceHeader>
        <sbo:ServiceBody xmlns:sbo="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceBody">
                <ns0:ebShrtenUrlAddRq xmlns:ns0="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/BSMF/ebShrtenUrlAddRq/01">
                        <ns0:REQHDR>
                                <ns0:TrnNum>WB20190823002628718</ns0:TrnNum>
                                <ns0:TrnCode>eb244028</ns0:TrnCode>
                        </ns0:REQHDR>
                        <ns0:REQBDY>
                                <ns0:DueDt>2019/08/24 10:05:06</ns0:DueDt>
                                <ns0:LongURL>https://ebtest.ctbcbank.com:7777/twrbo/zh_tw/online-branch/digital_account_ib/digital_account_ib0.html?param1=20190823100506554&amp;amp;param2=052277&amp;amp;token=iCv0sMZZpkgFIy8NpkPOP_jKeyE&amp;amp;enterView=0</ns0:LongURL>
                        </ns0:REQBDY>
                </ns0:ebShrtenUrlAddRq>
        </sbo:ServiceBody>
</sev:ServiceEnvelope>

ebShrtenUrlAdd 下行
<?xml version="1.0" encoding="UTF-8"?>
<ns0:ServiceEnvelope xmlns:ns0="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceEnvelope">
    <ns1:ServiceHeader xmlns:ns1="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceHeader">
        <ns1:TrackingID>mkTmIYfCj1VUU-7e3B0YGTp-Aos</ns1:TrackingID>
        <ns1:ServiceName>ebShrtenUrlAdd</ns1:ServiceName>
        <ns1:ServiceVersion>01</ns1:ServiceVersion>
        <ns1:SourceID>EBMWEB</ns1:SourceID>
        <ns1:TransactionID>WB20190823002628718</ns1:TransactionID>
        <ns1:RsTimestamp>2019-08-23T10:05:07.143+08:00</ns1:RsTimestamp>
        <ns1:StatusCode>0</ns1:StatusCode>
    </ns1:ServiceHeader>
    <ns1:ServiceBody xmlns:ns0="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceEnvelope" xmlns:ns1="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceBody">
        <ns2:ebShrtenUrlAddRs xmlns:ns2="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/BSMF/ebShrtenUrlAddRs/01">
            <ns2:RESHDR>
                <ns2:RspCode>0000</ns2:RspCode>
                <ns2:TrnNum>WB20190823002628718</ns2:TrnNum>
            </ns2:RESHDR>
            <ns2:RESBDY>
                <ns2:BDYREC>
                    <ns2:ShortURL>https://ebmwuat.ctbc.tw:8443/AhXcu7</ns2:ShortURL>
                </ns2:BDYREC>
            </ns2:RESBDY>
        </ns2:ebShrtenUrlAddRs>
    </ns1:ServiceBody>
</ns0:ServiceEnvelope>
```

### down ACL error
```xml
<?xml version="1.0" encoding="UTF-8"?>
<ns0:ServiceEnvelope xmlns:ns0="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceEnvelope">
   <ns1:ServiceHeader xmlns:ns1="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceHeader">
      <ns1:StandardType />
      <ns1:StandardVersion />
      <ns1:TrackingID />
      <ns1:ServiceName>ebShrtenUrlAdd</ns1:ServiceName>
      <ns1:ServiceVersion>01</ns1:ServiceVersion>
      <ns1:SourceID>EBMWEB</ns1:SourceID>
      <ns1:ChannelID />
      <ns1:TransactionID>WB20190823002628718</ns1:TransactionID>
      <ns1:RsTimestamp>2019-08-23T16:00:09.391+08:00</ns1:RsTimestamp>
      <ns1:StatusCode>1</ns1:StatusCode>
   </ns1:ServiceHeader>
   <ns1:ServiceError xmlns:ns1="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceError">
      <ns2:Error xmlns:ns2="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/Common">
         <ns2:ErrorType>PRIVILEGE</ns2:ErrorType>
         <ns2:ErrorCode>E906</ns2:ErrorCode>
         <ns2:ErrorMessage>AccessManager:The requested service is not authorized for the service client</ns2:ErrorMessage>
      </ns2:Error>
   </ns1:ServiceError>
</ns0:ServiceEnvelope>
```

### 2019/09/05 UP
``` xml
<?xml version="1.0" encoding="UTF-8"?>
<ns0:ServiceEnvelope xmlns:ns0="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceEnvelope">
   <ns1:ServiceHeader xmlns:ns1="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceHeader">
      <ns1:StandardType>BSMF</ns1:StandardType>
      <ns1:StandardVersion>01</ns1:StandardVersion>
      <ns1:ServiceName>ebShrtenUrlAdd</ns1:ServiceName>
      <ns1:ServiceVersion>01</ns1:ServiceVersion>
      <ns1:SourceID>MPB</ns1:SourceID>
      <ns1:TransactionID>MPB201909041813153</ns1:TransactionID>
      <ns1:RqTimestamp>2019-09-04T18:26:53.11+08:00</ns1:RqTimestamp>
   </ns1:ServiceHeader>
   <ns1:ServiceBody xmlns:ns1="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceBody">
      <ns2:ebShrtenUrlAddRq xmlns:ns2="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/BSMF/ebShrtenUrlAddRq/01">
         <ns2:REQHDR>
            <ns2:TrnNum>INEB201909041813153</ns2:TrnNum>
            <ns2:TrnCode />
         </ns2:REQHDR>
         <ns2:REQBDY>
            <ns2:SendMode />
            <ns2:URLNo />
            <ns2:ClientID>NUMS</ns2:ClientID>
            <ns2:LongURL>http://ebtest.ctbcbank.com:7777/twrbo/zh_tw/loan/hloan/hloan/Uploadfile.html</ns2:LongURL>
            <ns2:Protocol>https://</ns2:Protocol>
            <ns2:TelMobilContact />
            <ns2:CustName />
            <ns2:Copy />
            <ns2:CustShortenerId />
            <ns2:Action />
            <ns2:CustID />
            <ns2:DueDt>2019/09/26 15:26:42</ns2:DueDt>
            <ns2:CustBirth />
            <ns2:AppropDeadLine />
            <ns2:AuthType />
            <ns2:DataSource />
         </ns2:REQBDY>
      </ns2:ebShrtenUrlAddRq>
   </ns1:ServiceBody>
</ns0:ServiceEnvelope>
```

### down success
``` xml
<?xml version="1.0" encoding="UTF-8"?>
<ns0:ServiceEnvelope xmlns:ns0="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceEnvelope">
   <ns1:ServiceHeader xmlns:ns1="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceHeader">
      <ns1:StandardType>BSMF</ns1:StandardType>
      <ns1:StandardVersion>01</ns1:StandardVersion>
      <ns1:TrackingID>0eHyTmMuzq/uakta3Z0YH2ZEAos</ns1:TrackingID>
      <ns1:ServiceName>ebShrtenUrlAdd</ns1:ServiceName>
      <ns1:ServiceVersion>01</ns1:ServiceVersion>
      <ns1:SourceID>MPB</ns1:SourceID>
      <ns1:TransactionID>MPB201909041813153</ns1:TransactionID>
      <ns1:RsTimestamp>2019-09-05T11:03:30.294+08:00</ns1:RsTimestamp>
      <ns1:StatusCode>0</ns1:StatusCode>
   </ns1:ServiceHeader>
   <ns1:ServiceBody xmlns:ns1="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/EMF/ServiceBody">
      <ns2:ebShrtenUrlAddRs xmlns:ns2="http://ns.chinatrust.com.tw/XSD/CTCB/ESB/Message/BSMF/ebShrtenUrlAddRs/01">
         <ns2:RESHDR>
            <ns2:RspCode>0000</ns2:RspCode>
            <ns2:TrnNum>MPB201909041813153</ns2:TrnNum>
         </ns2:RESHDR>
         <ns2:RESBDY>
            <ns2:BDYREC>
               <ns2:ShortURL>https://ebmwuat.ctbc.tw:8443/JsWB8b</ns2:ShortURL>
            </ns2:BDYREC>
         </ns2:RESBDY>
      </ns2:ebShrtenUrlAddRs>
   </ns1:ServiceBody>
</ns0:ServiceEnvelope>
```

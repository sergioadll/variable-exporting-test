{
	"info": {
		"_postman_id": "700d6523-283b-4399-865f-00d2cded7c9d",
		"name": "redcare",
		"schema": "https://schema.getpostman.com/json/collection/v2.1.0/collection.json",
		"_exporter_id": "9322760"
	},
	"item": [
		{
			"name": "get_job_postings",
			"request": {
				"auth": {
					"type": "noauth"
				},
				"method": "POST",
				"header": [
					{
						"key": "Authorization",
						"value": "ISU_Job_Posting@shopapotheke:Workday32!",
						"type": "text"
					}
				],
				"body": {
					"mode": "raw",
					"raw": "<env:Envelope xmlns:env=\"http://schemas.xmlsoap.org/soap/envelope/\"\n    xmlns:xsd=\"http://www.w3.org/2001/XMLSchema\">\n    <env:Header>\n    <wsse:Security\n        env:mustUnderstand=\"1\"\n        xmlns:wsse=\"http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd\"\n        xmlns:wsu=\"http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd\">\n        <wsse:UsernameToken wsu:Id=\"UsernameToken-86F2FCCEFFBB80C4CD14820998755791\">\n            <wsse:Username>ISU_Job_Posting@shopapotheke</wsse:Username>\n            <wsse:Password Type=\"http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-username-token-profile-1.0#PasswordText\">Workday32!</wsse:Password>\n            <wsse:Nonce\n                EncodingType=\"http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-soap-message-security-1.0#Base64Binary\">asdfwrqwarqwr1+oA==\n            </wsse:Nonce>\n            <wsu:Created>2016-12-18T22:24:30.575Z</wsu:Created>\n        </wsse:UsernameToken>\n    </wsse:Security>\n</env:Header>\n    <env:Body>\n        <wd:Get_Job_Postings_Request xmlns:wd=\"urn:com.workday/bsvc\" wd:version=\"v40.1\">\n            \n            <wd:Request_References>\n                \n                <wd:Job_Posting_Reference>\n                    <wd:ID wd:type=\"Job_Posting_ID\">JOB_POSTING-3-1211</wd:ID>\n                </wd:Job_Posting_Reference>\n                \n            </wd:Request_References>\n            \n            <wd:Request_Criteria>\n                <wd:Show_Only_Active_Job_Postings>true</wd:Show_Only_Active_Job_Postings>\n            </wd:Request_Criteria>\n            \n            <wd:Response_Filter>\n                <wd:Page>1</wd:Page>\n                <wd:Count>999</wd:Count>\n            </wd:Response_Filter>\n            \n            <wd:Response_Group>\n                <wd:Include_Reference>true</wd:Include_Reference>\n                <wd:Include_Job_Requisition_Restrictions_Data>true</wd:Include_Job_Requisition_Restrictions_Data>\n                <wd:Include_Job_Requisition_Definition_Data>true</wd:Include_Job_Requisition_Definition_Data>\n                <wd:Include_Qualifications>true</wd:Include_Qualifications>\n                <wd:Include_Job_Requisition_Attachments>false</wd:Include_Job_Requisition_Attachments>\n            </wd:Response_Group>\n            \n        </wd:Get_Job_Postings_Request>\n    </env:Body>\n</env:Envelope>",
					"options": {
						"raw": {
							"language": "xml"
						}
					}
				},
				"url": {
					"raw": "https://wd3-impl-services1.workday.com/ccx/service/shopapotheke/Recruiting/v40.1?wsdl/",
					"protocol": "https",
					"host": [
						"wd3-impl-services1",
						"workday",
						"com"
					],
					"path": [
						"ccx",
						"service",
						"shopapotheke",
						"Recruiting",
						"v40.1"
					],
					"query": [
						{
							"key": "wsdl/",
							"value": null
						}
					]
				}
			},
			"response": []
		}
	]
}
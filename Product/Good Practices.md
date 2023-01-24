# General good practices:

## Variable/Actions Names: 

[ATF DOC Conventions](https://novabase.sharepoint.com/sites/CFCA/SitePages/Pluma-Cheat-Sheet.aspx?xsdata=MDV8MDF8fGY3YzA0M2RlY2U4MjQwODUxZjg5MDhkYWI1YWJkODRjfDRlOTliODVlOWM2MjQ4YzQ4ZTNlZDBkZGE5ODgzMTc5fDF8MHw2MzgwMjIwNDY4OTkyNDkwMzN8R29vZHxWR1ZoYlhOVFpXTjFjbWwwZVZObGNuWnBZMlY4ZXlKV0lqb2lNQzR3TGpBd01EQWlMQ0pRSWpvaVYybHVNeklpTENKQlRpSTZJazkwYUdWeUlpd2lWMVFpT2pFeGZRPT18MXxNVGs2TlRKbFlUQTVZVFF0TVRaak9DMDBNVFUyTFRnek56SXRZakUwWTJOa04yRTNZelF3WHpnMk5HWTFZalV4TFRrME16UXRORFU0WWkxaFptSTFMVGMxWkdRM1l6WXhNelZrWTBCMWJuRXVaMkpzTG5Od1lXTmxjdz09fHw%3D&sdata=YUVaWGdTS0NuNW1JZWE4L2p5NmFvenZFUm1zTkJxSGFPcVBKVXFzN3BLYz0%3D&ovuser=4e99b85e-9c62-48c4-8e3e-d0dda9883179%2CNB26394%40novabase.pt&OR=Teams-HL&CT=1666607891686&clickparams=eyJBcHBOYW1lIjoiVGVhbXMtRGVza3RvcCIsIkFwcFZlcnNpb24iOiIyNy8yMjA5MDQwMDcxMiIsIkhhc0ZlZGVyYXRlZFVzZXIiOmZhbHNlfQ%3D%3D#conventions)
 - Allways use Snake case with a prefix and description in order to make it easier to read
 - [tecnhical prefix] _ [page area/capability] _ [name/description]
 - Examples:
	 - btn_filter_apply 
	 - fld_filter_creation_date
	 - btn_console_related_logs_by
	 - lbl_console_columun_creation_date
		![[Pasted image 20221024105254.png]]

## Scenário Names:
- As a [agent], I want to validate that [scenario quick description]
- Example: 
	- As a UFE user, I want to validate that it is possible to filter by creatioin date.
	- As a UFE user, I want to validate that it is possible to view related logs by Conversation ID.
	- As a UFE user, I want to validate that the Log View page contains the mandatory elements.

## Tags:
ATF feature associated to the Cuccumber Tags, that can be used to specify a group or a single test case.
Here you can find some good uses, and good practices:
- Allways use Snake case
- Add the corresponding tag from azure test plan;
- Use tags to group specific scenarios;
- Use environment tags to indicate that a specific scenario can be exacuted on that environment
- Use tags @sanity or @smoke 
- Use tags @wip [working in progress], and @deprecated;
- Use tags @test_data_dependency for thoese tests that require a specific test data;

## Test Design:
This is a realy important part from our job. Designing a good scenario can avoid a lots of problems and we should give all the importance to this topic.
Here you can find the [ATF recomendations](https://novabase.sharepoint.com/sites/CFCA/SitePages/Conventions.aspx?xsdata=MDV8MDF8fGU5NDI3YjFmYzJiMjQwYTg5Mzk5MDhkYWI1YWJmZjgzfDRlOTliODVlOWM2MjQ4YzQ4ZTNlZDBkZGE5ODgzMTc5fDF8MHw2MzgwMjIwNDc1NTcxOTQ2NDl8R29vZHxWR1ZoYlhOVFpXTjFjbWwwZVZObGNuWnBZMlY4ZXlKV0lqb2lNQzR3TGpBd01EQWlMQ0pRSWpvaVYybHVNeklpTENKQlRpSTZJazkwYUdWeUlpd2lWMVFpT2pFeGZRPT18MXxNVGs2TlRKbFlUQTVZVFF0TVRaak9DMDBNVFUyTFRnek56SXRZakUwWTJOa04yRTNZelF3WHpnMk5HWTFZalV4TFRrME16UXRORFU0WWkxaFptSTFMVGMxWkdRM1l6WXhNelZrWTBCMWJuRXVaMkpzTG5Od1lXTmxjdz09fHw%3D&sdata=cnprdFpzRkd5TlVDUlBBdDNqSENvS2IrQjBsQ2FFSk5BZmVVcTlzWGQyST0%3D&ovuser=4e99b85e-9c62-48c4-8e3e-d0dda9883179%2CNB26394%40novabase.pt&OR=Teams-HL&CT=1666609529289&clickparams=eyJBcHBOYW1lIjoiVGVhbXMtRGVza3RvcCIsIkFwcFZlcnNpb24iOiIyNy8yMjA5MDQwMDcxMiIsIkhhc0ZlZGVyYXRlZFVzZXIiOmZhbHNlfQ%3D%3D), and some good tips about what should be a good test scenário: 
- Use the best practices described above;
- A good test scenario has **one** and just **one** purpose;
- A good test scenario shouldn't be complex;
- A good test scenario can be readable by any colleague;
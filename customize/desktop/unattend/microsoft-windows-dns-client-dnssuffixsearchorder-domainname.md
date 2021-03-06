---
title: DomainName
description: DomainName
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: d3a5be03-d687-4383-90b7-3a18d0ed70c8
ms.mktglfcycl: deploy
ms.sitesec: msdn
author: themar-msft
ms.author: themar
ms.date: 05/02/2017
ms.topic: article


---
# DomainName

`DomainName` specifies the domain name for the search.

> [!Note]
> The child elements do not appear in the **Properties** pane of Windows System Image Manager (Windows SIM) until you add this element to the answer file.

## Child Elements

| Setting                 | Description                                                                           |
|:------------------------|:--------------------------------------------------------------------------------------|
| [Key](microsoft-windows-dns-client-dnssuffixsearchorder-domainname-key.md) | Specifies a unique key for the <code>DomainName</code>. |
| [Value](microsoft-windows-dns-client-dnssuffixsearchorder-domainname-value.md) | Specifies the value of the <code>DomainName</code>. |

This string type does not support empty elements. Do not create an empty value for this setting.

## Parent Hierarchy

[Microsoft-Windows-DNS-Client](microsoft-windows-dns-client.md) | [DNSSuffixSearchOrder](microsoft-windows-dns-client-dnssuffixsearchorder.md) | **DomainName**

## Valid Configuration Passes

specialize

## Applies To

For a list of the supported Windows editions and architectures that this component supports, see [Microsoft-Windows-DNS-Client](microsoft-windows-dns-client.md).

## XML Example

The following XML output shows a DNS domain configuration for Fabrikam.

```XML
   <DNSDomain>fabrikam.com</DNSDomain>
   <DNSSuffixSearchOrder>
      <DomainName wcm:action="add" wcm:keyValue="1">server1.fabrikam.com</DomainName>
      <DomainName wcm:action="add" wcm:keyValue="2">fabrikam.com</DomainName>
   </DNSSuffixSearchOrder>
   <UseDomainNameDevolution>true</UseDomainNameDevolution>
   <Interfaces>
      <Interface wcm:action="add">
         <Identifier>Local Area Connection</Identifier>
         <DNSDomain>fabrikam.com</DNSDomain>
         <DNSServerSearchOrder>
            <IpAddress wcm:action="add" wcm:keyValue="1">192.168.1.1</IpAddress>
            <IpAddress wcm:action="add" wcm:keyValue="2">192.168.1.2</IpAddress>
         </DNSServerSearchOrder>
         <EnableAdapterDomainNameRegistration>true</EnableAdapterDomainNameRegistration>
         <DisableDynamicUpdate>false</DisableDynamicUpdate>
      </Interface>
      <Interface wcm:action="add">
         <Identifier>Local Area Connection 2</Identifier>
         <DNSDomain>fabrikam.com</DNSDomain>
         <DNSServerSearchOrder>
            <IpAddress wcm:action="add" wcm:keyValue="1">192.168.1.1</IpAddress>
            <IpAddress wcm:action="add" wcm:keyValue="2">2001:4898:28:4:213:20ff:fe16:3e96</IpAddress>
         </DNSServerSearchOrder>
         <EnableAdapterDomainNameRegistration>true</EnableAdapterDomainNameRegistration>
        <DisableDynamicUpdate>false</DisableDynamicUpdate>
      </Interface>
   </Interfaces>
```

## Related topics

[DNSSuffixSearchOrder](microsoft-windows-dns-client-dnssuffixsearchorder.md)

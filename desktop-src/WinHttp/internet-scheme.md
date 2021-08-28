---
description: Schémas Internet pris en charge par WinHTTP.
ms.assetid: 31e45879-807e-4dd5-9f99-94a46011e55e
title: INTERNET_SCHEME (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0429d07ef366acdc881a82373194e153ad3c8f367172b7e64221ecf479e7bf3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644019"
---
# <a name="internet_scheme"></a>\_schéma Internet

Schémas Internet pris en charge par WinHTTP.

<dl> <dt>

<span id="INTERNET_SCHEME_HTTP"></span><span id="internet_scheme_http"></span>**\_schéma Internet \_ http**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Schéma Internet HTTP.


</dt> </dl> </dd> <dt>

<span id="INTERNET_SCHEME_HTTPS"></span><span id="internet_scheme_https"></span>**\_https du schéma Internet \_**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Schéma Internet HTTPs (SSL).


</dt> </dl> </dd> <dt>

<span id="INTERNET_SCHEME_FTP"></span><span id="internet_scheme_ftp"></span>**\_FTP de schéma Internet \_**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Schéma Internet FTP. Ce schéma est pris en charge uniquement pour une utilisation dans [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) et [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).


</dt> </dl> </dd> <dt>

<span id="INTERNET_SCHEME_SOCKS"></span><span id="internet_scheme_socks"></span>**\_Socks de schéma Internet \_**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Un schéma d’Internet SOCKS. Ce schéma est pris en charge uniquement pour une utilisation dans l' [**\_ entrée de \_ résultat \_ de proxy WinHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry).


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP, Windows 2000 Professional avec les \[ applications de bureau SP3 uniquement\]<br/>      |
| Serveur minimal pris en charge<br/> | Windows server 2003, Windows 2000 server avec des \[ applications de bureau SP3 uniquement\]<br/>   |
| En-tête<br/>                   | <dl> <dt>WinHTTP. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_entrée des \_ résultats du proxy WinHTTP \_**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> </dl>

 

 





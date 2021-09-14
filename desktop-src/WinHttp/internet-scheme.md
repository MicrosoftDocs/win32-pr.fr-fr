---
description: Schémas Internet pris en charge par WinHTTP.
ms.assetid: 31e45879-807e-4dd5-9f99-94a46011e55e
title: INTERNET_SCHEME (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7b73dcc13b2623e3a6f28d2d49d1965464070f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228336"
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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP, Windows 2000 Professional avec les \[ applications de bureau SP3 uniquement\]<br/>      |
| Serveur minimal pris en charge<br/> | Windows server 2003, Windows 2000 server avec des \[ applications de bureau SP3 uniquement\]<br/>   |
| En-tête<br/>                   | <dl> <dt>WinHTTP. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_entrée des \_ résultats du proxy WinHTTP \_**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> </dl>

 

 





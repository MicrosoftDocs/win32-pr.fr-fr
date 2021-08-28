---
title: IMsRdpClientTransportSettings3 propriété GatewayAuthCookieServerAddr
description: Adresse du serveur pour l’authentification basée sur les cookies.
ms.assetid: e00480cd-2133-42ff-8447-6c4234b56bf9
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayAuthCookieServerAddr
- Services Bureau à distance de la propriété GatewayAuthCookieServerAddr, interface IMsRdpClientTransportSettings3
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings3, propriété GatewayAuthCookieServerAddr
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayAuthCookieServerAddr
- IMsRdpClientTransportSettings3.get_GatewayAuthCookieServerAddr
- IMsRdpClientTransportSettings3.put_GatewayAuthCookieServerAddr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 330a1ddb15d548988c23f8140ce848f7f68be5d1deb17fc51bd88eed23b9eec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000919"
---
# <a name="imsrdpclienttransportsettings3gatewayauthcookieserveraddr-property"></a>IMsRdpClientTransportSettings3 :: GatewayAuthCookieServerAddr, propriété

Adresse du serveur pour l’authentification basée sur les cookies.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_GatewayAuthCookieServerAddr(
  [in]          BSTR bstrProxyAuthCookieServerAddr
);

HRESULT get_GatewayAuthCookieServerAddr(
  [out, retval] BSTR *pbstrProxyAuthCookieServerAddr
);
```



## <a name="property-value"></a>Valeur de la propriété

Nouvelle adresse de serveur pour l’authentification basée sur les cookies.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 






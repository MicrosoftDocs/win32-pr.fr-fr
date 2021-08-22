---
title: IMsRdpClientTransportSettings3 propriété GatewayCredSourceCookie
description: Spécifie si la source d’informations d’identification est basée sur un cookie.
ms.assetid: 039459a3-7a83-444c-a0b4-46ef0dc5ddd0
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayCredSourceCookie
- Services Bureau à distance de la propriété GatewayCredSourceCookie, interface IMsRdpClientTransportSettings3
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings3, propriété GatewayCredSourceCookie
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayCredSourceCookie
- IMsRdpClientTransportSettings3.get_GatewayCredSourceCookie
- IMsRdpClientTransportSettings3.put_GatewayCredSourceCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fae89a3b7694d1ab73c076464b7ac62e6b18bcac6b4877d6156731135ee47a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606944"
---
# <a name="imsrdpclienttransportsettings3gatewaycredsourcecookie-property"></a>IMsRdpClientTransportSettings3 :: GatewayCredSourceCookie, propriété

Spécifie si la source d’informations d’identification est basée sur un cookie. Contient une valeur si la source d’informations d’identification est basée sur un cookie ou zéro dans le cas contraire.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_GatewayCredSourceCookie(
  [in]          ULONG ulProxyCredSourceCookie
);

HRESULT get_GatewayCredSourceCookie(
  [out, retval] ULONG *pulProxyCredSourceCookie
);
```



## <a name="property-value"></a>Valeur de la propriété

Valeur **ULong** qui spécifie si la source d’informations d’identification est basée sur un cookie.

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

 

 






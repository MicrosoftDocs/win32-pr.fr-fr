---
title: IMsRdpClientTransportSettings2 propriété GatewayPreAuthServerAddr
description: Spécifie ou récupère l’adresse Web du serveur de pré-authentification, qui est utilisé pour la fonctionnalité de mot de passe à usage unique de la passerelle Bureau à distance (passerelle Bureau à distance).
ms.assetid: 14edad82-ab19-46fe-b878-d34298763c56
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayPreAuthServerAddr
- Services Bureau à distance de la propriété GatewayPreAuthServerAddr, interface IMsRdpClientTransportSettings2
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings2, propriété GatewayPreAuthServerAddr
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPreAuthServerAddr
- IMsRdpClientTransportSettings2.get_GatewayPreAuthServerAddr
- IMsRdpClientTransportSettings2.put_GatewayPreAuthServerAddr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95d6fe2f397b0d445a6300d68a89b210debd449a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384164"
---
# <a name="imsrdpclienttransportsettings2gatewaypreauthserveraddr-property"></a>IMsRdpClientTransportSettings2 :: GatewayPreAuthServerAddr, propriété

Spécifie ou récupère l’adresse Web du serveur de pré-authentification, qui est utilisé pour la fonctionnalité de mot de passe à usage unique de la passerelle Bureau à distance (passerelle Bureau à distance).

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_GatewayPreAuthServerAddr(
  [in]  BSTR bstrProxyPreAuthServerAddr
);

HRESULT get_GatewayPreAuthServerAddr(
  [out] BSTR *pbstrProxyPreAuthServerAddr
);
```



## <a name="property-value"></a>Valeur de la propriété

Adresse Web du serveur de pré-authentification ; par exemple, l’adresse Web du serveur Microsoft Internet Security and Acceleration (ISA). Spécifiez l’adresse Web en utilisant le format «https://*hostname*. *DomainName*. com/*WebSiteName*» ou «*nom d’hôte* https://. *DomainName*. com/*WebSiteName*».

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista avec SP1<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                    |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings2 est défini comme 67341688-D606-4C73-A5D2-2E0489009319<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 






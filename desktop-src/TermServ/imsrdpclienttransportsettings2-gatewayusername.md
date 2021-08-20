---
title: IMsRdpClientTransportSettings2 propriété GatewayUserName
description: Spécifie ou récupère le nom d’utilisateur fourni au serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: eb5ed12f-e650-4abb-be20-bd5fae44e604
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayUserName
- Services Bureau à distance de la propriété GatewayUserName, interface IMsRdpClientTransportSettings2
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings2, propriété GatewayUserName
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayUserName
- IMsRdpClientTransportSettings2.get_GatewayUserName
- IMsRdpClientTransportSettings2.put_GatewayUserName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b5ba5c9b6d26bc2281f812674276a6f7208d31b33d33750a7a9b226aabfe4b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000939"
---
# <a name="imsrdpclienttransportsettings2gatewayusername-property"></a>IMsRdpClientTransportSettings2 :: GatewayUserName, propriété

Spécifie ou récupère le nom d’utilisateur fourni au serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_GatewayUserName(
  [in]  BSTR proxyUserName
);

HRESULT get_GatewayUserName(
  [out] BSTR *pProxyUserName
);
```



## <a name="property-value"></a>Valeur de la propriété

Nom d’utilisateur fourni pour la connexion au serveur de passerelle Bureau à distance.

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

 

 






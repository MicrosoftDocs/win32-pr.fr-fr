---
title: IMsRdpClientTransportSettings2 propriété GatewayPreAuthRequirement
description: Spécifie ou récupère le paramètre indiquant si la fonctionnalité de mot de passe à usage unique de la passerelle Bureau à distance (passerelle Bureau à distance) est activée.
ms.assetid: cc8f7ebb-16ba-45ed-ba66-de4a339946d0
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayPreAuthRequirement
- Services Bureau à distance de la propriété GatewayPreAuthRequirement, interface IMsRdpClientTransportSettings2
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings2, propriété GatewayPreAuthRequirement
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPreAuthRequirement
- IMsRdpClientTransportSettings2.get_GatewayPreAuthRequirement
- IMsRdpClientTransportSettings2.put_GatewayPreAuthRequirement
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72dd588cd3280128dde654497de359a901182935035213e420831857ab5c9f93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771259"
---
# <a name="imsrdpclienttransportsettings2gatewaypreauthrequirement-property"></a>IMsRdpClientTransportSettings2 :: GatewayPreAuthRequirement, propriété

Spécifie ou récupère le paramètre indiquant si la fonctionnalité de mot de passe à usage unique de la passerelle Bureau à distance (passerelle Bureau à distance) est activée.

Lorsque le mot de passe à usage unique est activé, **GatewayPreAuthRequirement** essaie d’interroger le cookie OTP à partir du magasin de cookies Internet à l’aide de la propriété [**GatewayPreAuthServerAddr**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md) . En cas de réussite, **GatewayPreAuthRequirement** envoie le cookie OTP au serveur pare-feu (par exemple, Microsoft Internet Security and Acceleration \[ ISA \] Server) pour la pré-authentification.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_GatewayPreAuthRequirement(
  [in]  ULONG ulProxyPreAuthRequirement
);

HRESULT get_GatewayPreAuthRequirement(
  [out] ULONG *pulProxyPreAuthRequirement
);
```



## <a name="property-value"></a>Valeur de la propriété

Si la valeur est 1, la fonctionnalité de mot de passe à usage unique est activée. Si la valeur est 0, la fonctionnalité de mot de passe à usage unique est désactivée.

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

 

 






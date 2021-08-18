---
title: IMsRdpClientTransportSettings2 propriété GatewayCredSharing
description: Spécifie ou récupère le paramètre déterminant si Bureau à distance la fonctionnalité de partage des informations d’identification de la passerelle des services Bureau à distance est activée.
ms.assetid: 296dc578-376d-41f6-988a-286fe744959f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayCredSharing
- Services Bureau à distance de la propriété GatewayCredSharing, interface IMsRdpClientTransportSettings2
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings2, propriété GatewayCredSharing
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayCredSharing
- IMsRdpClientTransportSettings2.get_GatewayCredSharing
- IMsRdpClientTransportSettings2.put_GatewayCredSharing
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6d489678006e842a6da82f5d2f9489f84a9a20fd70bfe8f18018aaa6d412c5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974649"
---
# <a name="imsrdpclienttransportsettings2gatewaycredsharing-property"></a>IMsRdpClientTransportSettings2 :: GatewayCredSharing, propriété

Spécifie ou récupère le paramètre déterminant si Bureau à distance la fonctionnalité de partage des informations d’identification de la passerelle des services Bureau à distance est activée. lorsque la fonctionnalité est activée, le contrôle de ActiveX Bureau à distance tente d’utiliser les mêmes informations d’identification pour s’authentifier auprès du serveur hôte de session Bureau à distance (hôte de session bureau à distance) et au serveur de passerelle bureau à distance.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_GatewayCredSharing(
  [in]  ULONG ulProxyCredSharing
);

HRESULT get_GatewayCredSharing(
  [out] ULONG *pulProxyCredSharing
);
```



## <a name="property-value"></a>Valeur de la propriété

Si la valeur est 1, le partage des informations d’identification est activé. Si la valeur est zéro, le partage des informations d’identification est désactivé.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Remarques

cette propriété est utilisée par le contrôle ActiveX pour implémenter une invite unique pour le partage des informations d’identification entre le serveur hôte de Session bureau à distance et le serveur de passerelle bureau à distance. Le partage des informations d’identification ne prend pas en charge le partage de mot de passe basé sur le Web avec [**GatewayPassword**](imsrdpclienttransportsettings2-gatewaypassword.md) ou [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md).

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

 

 






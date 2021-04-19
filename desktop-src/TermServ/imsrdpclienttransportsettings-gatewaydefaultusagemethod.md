---
title: IMsRdpClientTransportSettings propriété GatewayDefaultUsageMethod
description: Méthode d’utilisation par défaut pour la passerelle des services Bureau à Bureau à distance.
ms.assetid: 7014538d-550a-4246-ad32-406ef67fb112
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayDefaultUsageMethod
- Services Bureau à distance de la propriété GatewayDefaultUsageMethod, interface IMsRdpClientTransportSettings
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings, propriété GatewayDefaultUsageMethod
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayDefaultUsageMethod
- IMsRdpClientTransportSettings.get_GatewayDefaultUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b8417da30f9a692e6e233174a33f4b03682a5bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513766"
---
# <a name="imsrdpclienttransportsettingsgatewaydefaultusagemethod-property"></a>IMsRdpClientTransportSettings :: GatewayDefaultUsageMethod, propriété

Méthode d’utilisation par défaut pour la passerelle des services Bureau à Bureau à distance.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_GatewayDefaultUsageMethod(
  [out] ULONG *pulProxyDefaultUsageMethod
);
```



## <a name="property-value"></a>Valeur de la propriété

Pointeur vers la méthode d’utilisation par défaut pour la passerelle des services Bureau à distance. Retourne une Union des paramètres utilisateur définis par [**put \_ GatewayUsageMethod ()**](imsrdpclienttransportsettings-gatewayusagemethod.md)et des paramètres de stratégie de groupe. Si aucun paramètre utilisateur n’a été défini par **put \_ GatewayUsageMethod ()**, **\_ GatewayDefaultUsageMethod ()** retourne la valeur par défaut de la **\_ \_ \_ détection du mode proxy TSC**.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                         |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                   |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings est défini en tant que 720298C0-A099-46f5-9F82-96921BAE4701<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 






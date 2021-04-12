---
title: IMsRdpClientTransportSettings propriété GatewayProfileUsageMethod
description: Spécifie s’il faut utiliser les paramètres par défaut de passerelle des services Bureau à distance Bureau à distance.
ms.assetid: ce774790-31ad-40ba-ba8f-e81b0dbda175
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayProfileUsageMethod
- Services Bureau à distance de la propriété GatewayProfileUsageMethod, interface IMsRdpClientTransportSettings
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings, propriété GatewayProfileUsageMethod
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayProfileUsageMethod
- IMsRdpClientTransportSettings.get_GatewayProfileUsageMethod
- IMsRdpClientTransportSettings.put_GatewayProfileUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a12a9836e89348d1eb7ccdf680b23e2695c938
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384584"
---
# <a name="imsrdpclienttransportsettingsgatewayprofileusagemethod-property"></a>IMsRdpClientTransportSettings :: GatewayProfileUsageMethod, propriété

Spécifie s’il faut utiliser les paramètres par défaut de passerelle des services Bureau à distance Bureau à distance.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_GatewayProfileUsageMethod(
  [in]  ULONG ulProxyProfileMethod
);

HRESULT get_GatewayProfileUsageMethod(
  [out] ULONG *pulProxyProfileUsageMethod
);
```



## <a name="property-value"></a>Valeur de la propriété

Méthode d’utilisation du profil de la passerelle des services Bureau à distance. Ce paramètre peut prendre les valeurs suivantes.

<dt>

<span id="TSC_PROXY_PROFILE_MODE_DEFAULT"></span><span id="tsc_proxy_profile_mode_default"></span>

<span id="TSC_PROXY_PROFILE_MODE_DEFAULT"></span><span id="tsc_proxy_profile_mode_default"></span>**TSC \_ MODE de profil du PROXY \_ \_ \_ par défaut** (0 (0x0))


</dt> <dd>

Utilisez le mode de profil par défaut, tel que spécifié par l’administrateur.

</dd> <dt>

<span id="TSC_PROXY_PROFILE_MODE_EXPLICIT"></span><span id="tsc_proxy_profile_mode_explicit"></span>

<span id="TSC_PROXY_PROFILE_MODE_EXPLICIT"></span><span id="tsc_proxy_profile_mode_explicit"></span>**TSC \_ MODE de profil du PROXY \_ \_ \_ explicite** (1 (0x1))


</dt> <dd>

Utilisez des paramètres explicites, comme spécifié par l’utilisateur.

</dd> </dl>

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

 

 






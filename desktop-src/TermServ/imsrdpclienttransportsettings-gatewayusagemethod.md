---
title: IMsRdpClientTransportSettings propriété GatewayUsageMethod
description: Spécifie quand utiliser un serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: 0644c413-9ff7-42c1-a38e-e1ce546972ff
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayUsageMethod
- Services Bureau à distance de la propriété GatewayUsageMethod, interface IMsRdpClientTransportSettings
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings, propriété GatewayUsageMethod
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayUsageMethod
- IMsRdpClientTransportSettings.get_GatewayUsageMethod
- IMsRdpClientTransportSettings.put_GatewayUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f07bc10c67d01f957e588d1b50085e57b0fa10b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509090"
---
# <a name="imsrdpclienttransportsettingsgatewayusagemethod-property"></a>IMsRdpClientTransportSettings :: GatewayUsageMethod, propriété

Spécifie quand utiliser un serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_GatewayUsageMethod(
  [in]  ULONG ulProxyMethod
);

HRESULT get_GatewayUsageMethod(
  [out] ULONG *pulProxyUsageMethod
);
```



## <a name="property-value"></a>Valeur de la propriété

Variable **ULong** qui spécifie la méthode d’utilisation du serveur de passerelle Bureau à distance. Ce paramètre peut prendre les valeurs suivantes.

<dt>

<span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>

<span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>**TSC \_ \_Mode proxy \_ aucune \_ directe** (0 (0x0))


</dt> <dd>

N’utilisez pas de serveur de passerelle Bureau à distance. Dans l’interface utilisateur du client Connexion Bureau à distance (RDC), la case à cocher **ignorer le serveur de passerelle Bureau à distance pour les adresses locales** est désactivée.

</dd> <dt>

<span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>

<span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>**TSC \_ \_Mode proxy \_ direct** (1 (0x1))


</dt> <dd>

Utilisez toujours un serveur de passerelle Bureau à distance. Dans l’interface utilisateur du client RDC, la case à cocher **ignorer le serveur de passerelle Bureau à distance pour les adresses locales** est désactivée.

</dd> <dt>

<span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>

<span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>**TSC \_ \_ \_ Détection en mode proxy** (2 (0X2))


</dt> <dd>

Utilisez un serveur de passerelle Bureau à distance s’il est impossible d’établir une connexion directe au serveur hôte de session Bureau à distance. Dans l’interface utilisateur du client RDC, la case à cocher **ignorer le serveur de passerelle Bureau à distance pour les adresses locales** est activée.

</dd> <dt>

<span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>

<span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>**TSC \_ \_Mode proxy \_ par défaut** (3 (0x3))


</dt> <dd>

Utilisez les paramètres par défaut du serveur de passerelle Bureau à distance.

</dd> <dt>

<span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>

<span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>**TSC \_ \_Mode proxy \_ aucune \_ détection** (4 (0x4))


</dt> <dd>

N’utilisez pas de serveur de passerelle Bureau à distance. Dans l’interface utilisateur du client RDC, la case à cocher **ignorer le serveur de passerelle Bureau à distance pour les adresses locales** est activée.

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

 

 






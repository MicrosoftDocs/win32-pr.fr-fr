---
title: IMsRdpClientAdvancedSettings propriété LoadBalanceInfo
description: Spécifie le cookie d’équilibrage de charge qui sera placé dans le paquet de demande de connexion X. 224 dans la séquence de connexion du protocole du serveur de l’hôte de session Bureau à distance (hôte de session Bureau à distance).
ms.assetid: 25f12a2e-00a2-42a8-afd3-81efcd94da94
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété LoadBalanceInfo
- Services Bureau à distance de la propriété LoadBalanceInfo, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété LoadBalanceInfo
- Services Bureau à distance de la propriété LoadBalanceInfo, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété LoadBalanceInfo
- Services Bureau à distance de la propriété LoadBalanceInfo, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété LoadBalanceInfo
- Services Bureau à distance de la propriété LoadBalanceInfo, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété LoadBalanceInfo
- Services Bureau à distance de la propriété LoadBalanceInfo, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété LoadBalanceInfo
- Services Bureau à distance de la propriété LoadBalanceInfo, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété LoadBalanceInfo
- Services Bureau à distance de la propriété LoadBalanceInfo, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété LoadBalanceInfo
- Services Bureau à distance de la propriété LoadBalanceInfo, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété LoadBalanceInfo
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.LoadBalanceInfo
- IMsRdpClientAdvancedSettings.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.put_LoadBalanceInfo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efe7ca9b9ed68f3327779177e706ee5a943c9e6580e2b789e2b96e74ee9f0b4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353038"
---
# <a name="imsrdpclientadvancedsettingsloadbalanceinfo-property"></a>IMsRdpClientAdvancedSettings :: LoadBalanceInfo, propriété

Spécifie le cookie d’équilibrage de charge qui sera placé dans le paquet de demande de connexion X. 224 dans la séquence de connexion du protocole du serveur de l’hôte de session Bureau à distance (hôte de session Bureau à distance).

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_LoadBalanceInfo(
  [in]  BSTR newLBInfo
);

HRESULT get_LoadBalanceInfo(
  [out] BSTR *pLBInfo
);
```



## <a name="property-value"></a>Valeur de la propriété

Pointeur vers le nouveau cookie. Pour plus d’informations, consultez la section Notes.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Remarques

Les informations d’équilibrage de charge sont utilisées par les routeurs d’équilibrage de charge pour choisir le meilleur serveur pour le client lors de l’utilisation de batteries de serveurs hôtes de session Bureau à distance. Le serveur hôte de session Bureau à distance n’utilise pas ces informations et l’ignore.

Le cookie utilise la syntaxe suivante, qui respecte la casse :

**Cookie : MSTS =**_IpAddressAndPortNumber_*_\\ r \\ n_*

Où *IpAddressAndPortNumber* est l’adresse IP et le numéro de port, dans l’ordre d’octet du réseau.

Par exemple, le cookie utilisé pour accéder à l’adresse IP de 172.31.249.216, le numéro de port 3389 est le suivant :

**Cookie : MSTS = 3640205228.15629.0000 \\ r \\ n**

Les quatre derniers zéros sont facultatifs et sont réservés. La dernière virgule décimale est obligatoire, tout comme le retour chariot et le saut de ligne de fin. La longueur de la chaîne, en caractères, doit être un multiple pair de 2. par conséquent, ajoutez un espace si nécessaire.

Si aucun cookie n’est fourni, la valeur par défaut est **cookie : mstshash =**_username_*_\\ r \\ n_*.

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                        |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                  |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 






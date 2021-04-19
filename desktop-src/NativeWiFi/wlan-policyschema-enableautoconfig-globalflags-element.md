---
description: Spécifie si les ordinateurs utilisent le service de configuration automatique intégré (AutoConfig) pour gérer les connexions sans fil.
ms.assetid: c255e0a0-65ae-44a8-95cb-1a000394109d
title: enableAutoConfig (globalFlags), élément (LAN_policy) pour WLAN
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- enableAutoConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5105b8e634aa5affa8648b763a82bbd60cbaec17
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106531177"
---
# <a name="enableautoconfig-globalflags-element-lan_policy-for-wlan"></a>enableAutoConfig (globalFlags), élément (LAN_policy) pour WLAN 

L’élément **enableAutoConfig** (globalFlags) spécifie si les machines utilisent le service de configuration automatique intégré (AutoConfig) pour gérer les connexions sans fil. Lorsque **enableAutoConfig** a la valeur false, les ordinateurs ne doivent pas utiliser la configuration automatique pour gérer les connexions sans fil, et le service de configuration automatique répond uniquement aux demandes d’activation du service. Lorsque **enableAutoConfig** a la valeur true, les machines peuvent utiliser le service de configuration automatique.

Cet élément est obligatoire. Lorsqu’un profil est créé par le service de configuration automatique, cet élément a la valeur par défaut TRUE.

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

L’élément **enableAutoConfig** est défini par l’élément [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**globalFlags (WLANPolicy)**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 





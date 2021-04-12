---
description: Spécifie si les réseaux refusés s’affichent dans l’Assistant Connexion à un réseau.
ms.assetid: d0a13a80-2532-4383-8946-2536cc1f5e12
title: Élément showDeniedNetwork (globalFlags)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- showDeniedNetwork
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 33049dad00e5fda22e3f739d3dc200a282481a8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527801"
---
# <a name="showdeniednetwork-globalflags-element"></a>Élément showDeniedNetwork (globalFlags)

L’élément **showDeniedNetwork** (globalFlags) spécifie si les réseaux refusés s’affichent dans l’Assistant **connexion à un réseau** . Les réseaux peuvent être refusés par la stratégie de groupe ou par les paramètres utilisateur. Lorsque **showDeniedNetwork** a la valeur true, les réseaux refusés s’affichent dans l’Assistant **connexion à un réseau** . dans le cas contraire, les réseaux refusés n’apparaissent pas dans l’Assistant.

Cet élément est obligatoire. Lorsqu’un profil est créé par le service de configuration automatique, cet élément prend la valeur par défaut FALSe.

``` syntax
<xs:element name="showDeniedNetwork"
    type="boolean"
 />
```

L’élément **showDeniedNetwork** est défini par l’élément [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) .

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

 

 





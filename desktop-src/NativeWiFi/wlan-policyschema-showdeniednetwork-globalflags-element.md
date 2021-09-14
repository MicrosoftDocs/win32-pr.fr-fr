---
description: spécifie si les réseaux refusés s’affichent dans le Connecter à un assistant réseau.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110393"
---
# <a name="showdeniednetwork-globalflags-element"></a>Élément showDeniedNetwork (globalFlags)

l’élément **showDeniedNetwork** (globalFlags) spécifie si les réseaux refusés s’affichent dans le **Connecter à un assistant réseau** . Les réseaux peuvent être refusés par la stratégie de groupe ou par les paramètres utilisateur. lorsque **showDeniedNetwork** a la valeur TRUE, les réseaux refusés s’affichent dans le **Connecter à un assistant réseau** . dans le cas contraire, les réseaux refusés n’apparaissent pas dans l’Assistant.

Cet élément est obligatoire. Lorsqu’un profil est créé par le service de configuration automatique, cet élément prend la valeur par défaut FALSe.

``` syntax
<xs:element name="showDeniedNetwork"
    type="boolean"
 />
```

L’élément **showDeniedNetwork** est défini par l’élément [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



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

 

 





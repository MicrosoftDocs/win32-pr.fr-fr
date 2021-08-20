---
description: Spécifie un type de réseau.
ms.assetid: fe3044ab-6e93-48f8-b8cb-fdf984987232
title: Élément networkType (networkItemType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 57616d6701ab4663fa6757ddec5df4886ec02faaf5088f61b6cb466ca834ec81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684389"
---
# <a name="networktype-networkitemtype-element"></a>Élément networkType (networkItemType)

L’élément networkType (networkItemType) spécifie un type de réseau. Il existe deux types de réseaux : les réseaux d’infrastructure (ESS) et les réseaux ad hoc (IBSS).

``` syntax
<xs:element name="networkType"
    type="networkTypeType"
 />
```

L’élément **networkType** est défini par le type complexe [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**networkItemType**](wlan-policyschema-networkitemtype-complextype.md)
</dt> <dt>

**Éléments parents immédiats possibles dans l’instance de schéma**
</dt> <dt>

[**réseau (allowList)**](wlan-policyschema-network-allowlist-element.md)
</dt> <dt>

[**réseau (de blocage)**](wlan-policyschema-network-blocklist-element.md)
</dt> </dl>

 

 





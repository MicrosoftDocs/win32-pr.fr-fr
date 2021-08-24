---
description: Spécifie l’identificateur SSID (Service Set Identifier) d’un réseau sans fil.
ms.assetid: 103808f2-9e5f-4605-b42a-337a13455294
title: Élément networkName (networkItemType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkName
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8c21d5dac057aaf20461e3b27bf6e23f66ec19ae3515045665d277ea4413566a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779919"
---
# <a name="networkname-networkitemtype-element"></a>Élément networkName (networkItemType)

L’élément networkName (networkItemType) spécifie l’identificateur SSID (Service Set Identifier) d’un réseau sans fil.

``` syntax
<xs:element name="networkName"
    type="networkNameType"
 />
```

L’élément **networkName** est défini par le type complexe [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) .

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

 

 





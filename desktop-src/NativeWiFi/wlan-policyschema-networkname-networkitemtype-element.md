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
ms.openlocfilehash: da635c392a29419e7b151cc2c4fb080ff7d3fca9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867909"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



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

 

 





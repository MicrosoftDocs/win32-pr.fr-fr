---
description: Définit un réseau bloqué.
ms.assetid: ccf24d45-cae0-4eb7-951a-004a5f71e04a
title: Élément de réseau (de blocage)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- network
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 893c557ca5c20dd73f10f2a31d3b416d76116deb206f5d04420d35443d902130
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117984459"
---
# <a name="network-blocklist-element"></a>Élément de réseau (de blocage)

L’élément réseau (de blocage) définit un réseau bloqué. Un ordinateur ne peut pas se connecter à un réseau bloqué.

``` syntax
<xs:element name="network"
    type="networkItemType"
 />
```

L’élément **réseau** est défini [**par l’élément de la**](wlan-policyschema-blocklist-networkfilter-element.md) en-dessus.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**Noires**](wlan-policyschema-blocklist-networkfilter-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**Blocage (networkFilter)**](wlan-policyschema-blocklist-networkfilter-element.md)
</dt> </dl>

 

 





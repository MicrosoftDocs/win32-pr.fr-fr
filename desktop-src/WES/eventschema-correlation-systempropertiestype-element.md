---
title: Élément correlation (SystemPropertiesType)
description: Identificateurs d’activité que les consommateurs peuvent utiliser pour regrouper des événements connexes.
ms.assetid: 63982f37-3581-4b11-ac14-b95bc52541cb
keywords:
- Élément de corrélation EventLog
topic_type:
- apiref
api_name:
- Correlation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fc301c43bbc8ba834949ae2a5056fb4359b5c8db3125da3d1729b18ac7aa1b73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120357"
---
# <a name="correlation-systempropertiestype-element"></a>Élément correlation (SystemPropertiesType)

Identificateurs d’activité que les consommateurs peuvent utiliser pour regrouper des événements connexes.

``` syntax
<xs:element name="Correlation">
    <xs:complexType>
        <xs:attribute name="ActivityID"
            type="GUIDType"
            use="optional"
         />
        <xs:attribute name="RelatedActivityID"
            type="GUIDType"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

L’élément **Correlation** est défini par le type complexe [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .

## <a name="attributes"></a>Attributs



| Nom              | Type                                                | Description                                                                                                                                                                                  |
|-------------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ActivityID        | [**GUIDType**](eventschema-guidtype-simpletype.md) | Identificateur global unique qui identifie l’activité en cours. Les événements qui sont publiés avec cet identificateur font partie de la même activité.<br/>                              |
| RelatedActivityID | [**GUIDType**](eventschema-guidtype-simpletype.md) | Identificateur global unique qui identifie l’activité à laquelle le contrôle a été transféré. Les événements connexes ont alors cet identificateur comme identificateur ActivityID.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**Système (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 






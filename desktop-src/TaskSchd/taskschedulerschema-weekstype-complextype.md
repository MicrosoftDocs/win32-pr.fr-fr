---
title: Type complexe weeksType
description: Définit l’élément enfant et les informations de séquencement de l’élément week.
ms.assetid: c9e8814c-b8f9-426d-943d-ca3efa5d914b
keywords:
- Planificateur de tâches de type complexe weeksType
topic_type:
- apiref
api_name:
- weeksType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 876d798acdf1f8684fc4f2cecac8e77bceb73dddd0036f2117d4bb55a77a71ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757986"
---
# <a name="weekstype-complex-type"></a>Type complexe weeksType

Définit l’élément enfant et les informations de séquencement de l’élément [**week**](taskschedulerschema-week-weekstype-element.md) .

``` syntax
<xs:complexType name="weeksType">
    <xs:sequence>
        <xs:element name="Week"
            type="weekType"
            minOccurs="0"
            maxOccurs="5"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                    | Type                                                        | Description                                             |
|------------------------------------------------------------|-------------------------------------------------------------|---------------------------------------------------------|
| [**Week**](taskschedulerschema-week-weekstype-element.md) | [**weekType**](taskschedulerschema-weektype-simpletype.md) | Spécifie la semaine d’exécution de la tâche.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 






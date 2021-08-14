---
title: Type complexe principalsType
description: Définit l’élément enfant de l’élément principal.
ms.assetid: a501534b-eb0f-480f-a2c9-d2015262a9a7
keywords:
- Planificateur de tâches de type complexe principalsType
topic_type:
- apiref
api_name:
- principalsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fa2aecd8ea71769b51792fcc5bd26ceca11309f43697037964a900d45c0d8254
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131740"
---
# <a name="principalstype-complex-type"></a>Type complexe principalsType

Définit l’élément enfant de l’élément [**principal**](taskschedulerschema-principals-tasktype-element.md) .

``` syntax
<xs:complexType name="principalsType">
    <xs:sequence>
        <xs:element name="Principal"
            type="principalType"
            maxOccurs="1"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                  | Type                                                                   | Description                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principal**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Spécifie les informations d’identification de sécurité pour un principal.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 






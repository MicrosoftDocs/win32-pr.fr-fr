---
title: Type complexe idleTriggerType
description: Définit le type de base pour l’élément IdleTrigger.
ms.assetid: 05beabb7-2e6f-4df1-809a-9f64a578d80a
keywords:
- Planificateur de tâches de type complexe idleTriggerType
topic_type:
- apiref
api_name:
- idleTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 97868d5b13f224bc55661b681246be29f3a4a20b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228767"
---
# <a name="idletriggertype-complex-type"></a>Type complexe idleTriggerType

Définit le type de base pour l’élément [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) .

``` syntax
<xs:complexType name="idleTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
         />
    </xs:complexContent>
</xs:complexType>
```

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types complexes de schéma Planificateur de tâches](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 






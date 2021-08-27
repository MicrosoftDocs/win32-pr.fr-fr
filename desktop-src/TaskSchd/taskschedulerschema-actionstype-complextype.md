---
title: Type complexe actionsType
description: Définit les éléments enfants et l’attribut de l’élément actions.
ms.assetid: 01577b65-4bfa-4b9f-b9b9-6b2b0dbd582a
keywords:
- Planificateur de tâches de type complexe actionsType
topic_type:
- apiref
api_name:
- actionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d84cab2f0977a3b5bf980f594f1b26b543d8e5e7de000959488e874e640dc9d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010929"
---
# <a name="actionstype-complex-type"></a>Type complexe actionsType

Définit les éléments enfants et l’attribut de l’élément [**actions**](taskschedulerschema-actions-tasktype-element.md) .

``` syntax
<xs:complexType name="actionsType">
    <xs:sequence>
        <xs:group
            maxOccurs="32"
            ref="actionGroup"
         />
    </xs:sequence>
    <xs:attribute name="Context"
        type="IDREF"
        use="optional"
     />
</xs:complexType>
```

## <a name="attributes"></a>Attributs



| Nom    | Type  | Description                                                                                          |
|---------|-------|------------------------------------------------------------------------------------------------------|
| Contexte | IDREF | Identificateur principal du utilisé qui est le contexte de sécurité pour les actions de la tâche.<br/> |



## <a name="requirements"></a>Configuration requise



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

 

 






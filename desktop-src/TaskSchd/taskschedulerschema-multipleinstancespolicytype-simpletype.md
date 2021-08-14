---
title: Type simple multipleInstancesPolicyType
description: Définit les constantes de stratégie d’instance pour l’élément MultipleInstancesPolicy (settingsType).
ms.assetid: 6e3f83b0-b71e-49c9-9c27-5a37f996746b
keywords:
- Planificateur de tâches de type simple multipleInstancesPolicyType
topic_type:
- apiref
api_name:
- multipleInstancesPolicyType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e8e847e268486e58bc36bd1bcf9f454b2d8af7b7664d0372613c40c818f932f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758508"
---
# <a name="multipleinstancespolicytype-simple-type"></a>Type simple multipleInstancesPolicyType

Définit les constantes de stratégie d’instance pour l’élément [**MultipleInstancesPolicy (settingsType)**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) .

``` syntax
<xs:simpleType name="multipleInstancesPolicyType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="Parallel"
         />
        <xs:enumeration
            value="Queue"
         />
        <xs:enumeration
            value="IgnoreNew"
         />
        <xs:enumeration
            value="StopExisting"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valeurs d’énumération

Le type simple **multipleInstancesPolicyType** définit les valeurs suivantes.



| Valeur        | Description                                                                                     |
|--------------|-------------------------------------------------------------------------------------------------|
| Parallèle     | Démarre une nouvelle instance pendant l’exécution d’une instance existante.<br/>                           |
| File d'attente        | Démarre une nouvelle instance de la tâche une fois que toutes les autres instances de la tâche sont terminées.<br/>      |
| IgnoreNew    | Par défaut. Ne démarre pas une nouvelle instance si une instance existante de la tâche est en cours d’exécution.<br/> |
| StopExisting | Arrête une instance existante de la tâche avant de démarrer une nouvelle instance.<br/>                |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types simples de schéma Planificateur de tâches](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 






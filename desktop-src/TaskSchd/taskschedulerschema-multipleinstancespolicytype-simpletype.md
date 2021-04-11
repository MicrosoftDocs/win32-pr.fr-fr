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
ms.openlocfilehash: 29a3523ef16224836ada474fb32265084453479c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942343"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types simples de schéma Planificateur de tâches](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 






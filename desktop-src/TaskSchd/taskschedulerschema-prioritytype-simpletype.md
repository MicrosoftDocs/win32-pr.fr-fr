---
title: Type simple priorityType
description: Définit les valeurs minimales et maximales de l’élément Priority (settingsType).
ms.assetid: 44e97d78-f035-4db9-a557-f24960518628
keywords:
- Planificateur de tâches de type simple priorityType
topic_type:
- apiref
api_name:
- priorityType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 05b3c6d04adf557242438c813dab4f10d48cdb9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033103"
---
# <a name="prioritytype-simple-type"></a>Type simple priorityType

Définit les valeurs minimales et maximales de l’élément [**Priority (settingsType)**](taskschedulerschema-priority-settingstype-element.md) .

``` syntax
<xs:simpleType name="priorityType">
    <xs:restriction
        base="byte"
    >
        <xs:enumeration
            value="0"
         />
        <xs:enumeration
            value="10"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valeurs d’énumération

Le type simple **priorityType** définit les valeurs suivantes.



| Valeur | Description                         |
|-------|-------------------------------------|
| 0     | Entier minimal autorisé.<br/> |
| 10    | Entier maximal autorisé.<br/> |



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

 

 






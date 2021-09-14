---
title: type simple guidType (Planificateur de tâches)
description: Définit le modèle pour les GUID valides.
ms.assetid: 1aa3f08b-4b3e-4e72-8ac4-d859a8da4c32
keywords:
- Planificateur de tâches de type simple guidType
topic_type:
- apiref
api_name:
- guidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 75b95d5b8ad7a4158dbe449fb28cf3324499488f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228827"
---
# <a name="guidtype-simple-type-task-scheduler"></a>type simple guidType (Planificateur de tâches)

Définit le modèle pour les GUID valides.

``` syntax
<xs:simpleType name="guidType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\{([0-9a-fA-F]){8}(\-[0-9a-fA-F]{4}){3}\-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modèles

Le type simple **guidType** est une **chaîne** qui est limitée par le modèle suivant :

-   `\{([0-9a-fA-F]){8}(\-[0-9a-fA-F]{4}){3}\-[0-9a-fA-F]{12}\}`

    Nombre 128 bits unique.

## <a name="requirements"></a>Spécifications



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

 

 






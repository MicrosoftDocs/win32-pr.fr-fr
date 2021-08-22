---
title: Type simple dayOfMonthType
description: Définit les valeurs possibles pour la spécification d’un jour du mois.
ms.assetid: 13497cf4-e1e5-4d54-9dff-0fe89be1fed8
keywords:
- Planificateur de tâches de type simple dayOfMonthType
topic_type:
- apiref
api_name:
- dayOfMonthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 45c3d3d549f2d84c292ad1dbdf3c03965bd6e4265559b57c41016811834167a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119309351"
---
# <a name="dayofmonthtype-simple-type"></a>Type simple dayOfMonthType

Définit les valeurs possibles pour la spécification d’un jour du mois.

``` syntax
<xs:simpleType name="dayOfMonthType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="[1-9]|[1-2][0-9]|3[0-1]|Last"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modèles

Le type simple **dayOfMonthType** est une **chaîne** qui est limitée par le modèle suivant :

-   `[1-9]|[1-2][0-9]|3[0-1]|Last`

    Spécifie le 1er au 31 du mois, ou toujours le dernier jour du mois.

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

 

 






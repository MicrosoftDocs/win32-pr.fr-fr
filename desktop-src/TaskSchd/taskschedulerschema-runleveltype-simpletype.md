---
title: Type simple runLevelType
description: Définit les valeurs possibles pour l’élément RunLevel (principalType).
ms.assetid: d6b73dc5-97ac-4f94-99c1-c241a25cc252
keywords:
- Planificateur de tâches de type simple runLevelType
topic_type:
- apiref
api_name:
- runLevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ce534008ce0138293a773e4f5fa4a5270a2d4b27aad54dd062eafe286ab8ba6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991069"
---
# <a name="runleveltype-simple-type"></a>Type simple runLevelType

Définit les valeurs possibles pour l’élément [**runlevel (principalType)**](taskschedulerschema-runlevel-principaltype-element.md) .

``` syntax
<xs:simpleType name="runLevelType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="LeastPrivilege"
         />
        <xs:enumeration
            value="HighestAvailable"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valeurs d’énumération

Le type simple **runLevelType** définit les valeurs suivantes.



| Valeur            | Description                                               |
|------------------|-----------------------------------------------------------|
| LeastPrivilege   | Les tâches sont exécutées avec le moins de privilèges (LUA).<br/> |
| HighestAvailable | Les tâches sont exécutées avec les privilèges les plus élevés.<br/>     |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 






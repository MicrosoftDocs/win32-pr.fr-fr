---
title: Type simple nonEmptyStringType
description: Définit les valeurs utilisées pour une chaîne de texte non vide.
ms.assetid: cb3b1ca6-4531-467c-a27a-b27a62233514
keywords:
- Planificateur de tâches de type simple nonEmptyString
topic_type:
- apiref
api_name:
- nonEmptyString
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab9c9fa84c510fc4e67f6f63664a58d6d4093709
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384908"
---
# <a name="nonemptystringtype-simple-type"></a>Type simple nonEmptyStringType

Définit les valeurs utilisées pour une chaîne de texte non vide.

``` syntax
<xs:simpleType name="nonEmptyString">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valeurs d’énumération

Le type simple **nonEmptyString** définit la valeur suivante.



| Valeur | Description                                            |
|-------|--------------------------------------------------------|
| 1     | La chaîne contient au moins un caractère.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 






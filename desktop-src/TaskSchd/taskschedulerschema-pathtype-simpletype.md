---
title: Type simple pathType
description: Définit le nombre minimal et maximal de caractères pour une chaîne qui définit un chemin d’accès de fichier.
ms.assetid: 09908f75-ba7b-4e31-877e-80fabea6bd27
keywords:
- Planificateur de tâches de type simple pathType
topic_type:
- apiref
api_name:
- pathType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 289e91b3d7139001bfab22c81bfb0f9e9871033f6296286373c5bde18fdc366d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758378"
---
# <a name="pathtype-simple-type"></a>Type simple pathType

Définit le nombre minimal et maximal de caractères pour une chaîne qui définit un chemin d’accès de fichier. Le chemin d’accès ne peut pas être une chaîne vide et doit être inférieur à 260 caractères.

``` syntax
<xs:simpleType name="pathType">
    <xs:restriction
        base="nonEmptyString"
    >
        <xs:maxLength
            value="260"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 






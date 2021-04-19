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
ms.openlocfilehash: 4a75ef7d85eba2aa39e0c3c768fec0908c7ea16b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106516100"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 






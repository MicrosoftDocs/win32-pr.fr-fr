---
description: Définit le type utilisé pour spécifier des valeurs valides pour la couleur de certains éléments dans un fichier journal XML.
ms.assetid: 10a19f28-d0aa-4126-b3f5-fde35fc5fdb0
title: Type simple ColorType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ColorType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 883c34f42f8d31f3581599445b398b93676d416b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513349"
---
# <a name="colortype-simple-type"></a>Type simple ColorType

Définit le type utilisé pour spécifier des valeurs valides pour la couleur de certains éléments dans un fichier journal XML.

``` syntax
<xs:simpleType name="ColorType">
    <xs:restriction
        base="string"
     />
</xs:simpleType>
```

## <a name="remarks"></a>Notes

Une couleur peut être une valeur RVB hexadécimale au format \# RRGGBB. Il doit correspondre à l’expression régulière suivante : \# \[ 0-9A-FA-F \] {6} . Par exemple : « \# 4a79B5 ».

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                     |



 

 





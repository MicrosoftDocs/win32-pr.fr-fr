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
ms.openlocfilehash: 92b4f8db5626ec34c66c769f86afe1eac9d37940dce0374b1340430d3e62939d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009079"
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

## <a name="remarks"></a>Remarques

Une couleur peut être une valeur RVB hexadécimale au format \# RRGGBB. Il doit correspondre à l’expression régulière suivante : \# \[ 0-9A-FA-F \] {6} . Par exemple : « \# 4a79B5 ».

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                     |



 

 





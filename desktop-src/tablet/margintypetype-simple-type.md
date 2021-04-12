---
description: Définit le type qui contient des valeurs valides pour l’attribut de type de l’élément Margin.
ms.assetid: 5448ead5-0249-4cc7-9f2a-d2181e2af734
title: Type simple MarginTypeType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MarginTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4e8a09e98611fabc54a029c9cac9cb37dfc1373f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210292"
---
# <a name="margintypetype-simple-type"></a>Type simple MarginTypeType

Définit le type qui contient des valeurs valides pour l’attribut de **type** de l' [élément Margin](margin-element.md).

``` syntax
<xs:simpleType name="MarginTypeType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="Left|Right"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modèles

Le type simple **MarginTypeType** est une **chaîne** qui est limitée par le modèle suivant :

-   `Left|Right`

## <a name="remarks"></a>Notes

Les valeurs valides pour l’attribut de **type** de l' [élément Margin](margin-element.md) sont « Left » et « Right ».

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                     |



 

 





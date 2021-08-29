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
ms.openlocfilehash: b1996b99729e177f7012db097644807a2bf7052f231e089052d5244b20d016ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031687"
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

## <a name="remarks"></a>Remarques

Les valeurs valides pour l’attribut de **type** de l' [élément Margin](margin-element.md) sont « Left » et « Right ».

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                     |



 

 





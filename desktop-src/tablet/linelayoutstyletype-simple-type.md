---
description: Définit les valeurs valides pour l’attribut style de l’élément LineLayout.
ms.assetid: b257f0da-1bee-4d1b-9829-70f91cdcabe0
title: Type simple LineLayoutStyleType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LineLayoutStyleType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d2aa0a42ca2f295cdcccad05931ba651d4018ba377d8d10f09f85b82dcaaea8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031837"
---
# <a name="linelayoutstyletype-simple-type"></a>Type simple LineLayoutStyleType

Définit les valeurs valides pour l’attribut **style** de l' [élément LineLayout](linelayout-element.md).

``` syntax
<xs:simpleType name="LineLayoutStyleType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="None|Solid|Dash|Dot|DashDot|DashDotDot|Double"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modèles

Le type simple **LineLayoutStyleType** est une chaîne qui est limitée par le modèle suivant :

-   `None|Solid|Dash|Dot|DashDot|DashDotDot|Double`

## <a name="remarks"></a>Remarques

Les valeurs valides pour l’attribut **style** de l' [élément LineLayout](linelayout-element.md) sont les suivantes :

-   Aucun
-   Unie
-   Tiret
-   Points
-   Tiret-point
-   Tiret-point-point
-   Double

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                     |



 

 





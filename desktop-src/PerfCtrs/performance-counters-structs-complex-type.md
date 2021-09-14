---
description: Définit une liste de structures qui contiennent des valeurs de compteur.
ms.assetid: 6f6b33ed-6440-456c-8379-61a37798c95f
title: Type complexe structs
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c36de698d1e0eb136f17034e0740851fc751d157
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127218313"
---
# <a name="structs-complex-type"></a>Type complexe structs

Définit une liste de structures qui contiennent des valeurs de compteur.

``` syntax
<xs:complexType name="structs">
    <xs:choice
        minOccurs="1"
        maxOccurs="unbounded"
    >
        <xs:element name="struct"
            type="man:struct"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément    | Type                                                           | Description                                                      |
|------------|----------------------------------------------------------------|------------------------------------------------------------------|
| **modélis** | [**homme : struct**](performance-counters-struct-complex-type.md) | Nom d’une structure qui contient des valeurs de compteur.<br/> |



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





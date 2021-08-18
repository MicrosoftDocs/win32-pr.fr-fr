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
ms.openlocfilehash: 0dfa7f72ee537d857f19301aa4df906d94b0bf7ba9e3f7a76bdb6ab82c84dfd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119314419"
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



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





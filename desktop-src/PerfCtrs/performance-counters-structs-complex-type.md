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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106542941"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





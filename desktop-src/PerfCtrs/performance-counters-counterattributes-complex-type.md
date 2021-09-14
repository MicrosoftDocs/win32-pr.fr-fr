---
description: Définit une liste qui contient jusqu’à cinq attributs de compteur.
ms.assetid: d710c3d2-2886-4f1a-bd27-f11451d2f3c6
title: Type complexe counterAttributes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bfcb94b131e1343565d5763ae2ea4d95e53f1eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127218484"
---
# <a name="counterattributes-complex-type"></a>Type complexe counterAttributes

Définit une liste qui contient jusqu’à cinq attributs de compteur.

``` syntax
<xs:complexType name="counterAttributes">
    <xs:choice
        minOccurs="1"
        maxOccurs="5"
    >
        <xs:element name="counterAttribute"
            type="man:counterAttribute"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément              | Type                                                                               | Description                                                                                                |
|----------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| **counterAttribute** | [**homme : counterAttribute**](performance-counters-counterattribute-complex-type.md) | Attribut de compteur qui spécifie le mode d’affichage des données de compteur dans une application consommateur.<br/> |



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





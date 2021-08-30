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
ms.openlocfilehash: be740abacc9a10674b98e2c2088f647dfaa26c7cd99c7e55efbfe968731a9a54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119775419"
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



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





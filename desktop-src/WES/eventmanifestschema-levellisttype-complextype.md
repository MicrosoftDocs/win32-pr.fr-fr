---
title: Type complexe LevelListType
description: Définit une liste de niveaux de gravité qui spécifient le niveau de détail d’un événement.
ms.assetid: 82102f8a-271e-4c3d-9b0a-1e20eaa87497
keywords:
- LevelListType type complexe EventLog
topic_type:
- apiref
api_name:
- LevelListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8087913cacac67f0c7487b5eb41f404ebdc205765c693bdfda9f86995a809493
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124299"
---
# <a name="levellisttype-complex-type"></a>Type complexe LevelListType

Définit une liste de niveaux de gravité qui spécifient le niveau de détail d’un événement.

``` syntax
<xs:complexType name="LevelListType">
    <xs:sequence>
        <xs:element name="level"
            type="LevelType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                          | Type                                                           | Description                                                                                 |
|------------------------------------------------------------------|----------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**niveau**](eventmanifestschema-level-levellisttype-element.md) | [**LevelType**](eventmanifestschema-leveltype-complextype.md) | Définit une valeur de gravité qui détermine le niveau de détail des événements lors de la journalisation.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 






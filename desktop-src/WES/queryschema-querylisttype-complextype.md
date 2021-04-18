---
title: Type complexe QueryListType
description: Définit une liste de requêtes qui peuvent contenir un ensemble de sélecteurs et de suppressions utilisés pour inclure des événements dans ou exclure des événements du jeu de résultats.
ms.assetid: 3b9944e8-5913-4a77-a8fd-7efa43f3063f
keywords:
- QueryListType type complexe EventLog
topic_type:
- apiref
api_name:
- QueryListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58cc6e83fb681f6244288088ea217097dd109c23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509315"
---
# <a name="querylisttype-complex-type"></a>Type complexe QueryListType

Définit une liste de requêtes qui peuvent contenir un ensemble de sélecteurs et de suppressions utilisés pour inclure des événements dans ou exclure des événements du jeu de résultats.

``` syntax
<xs:complexType name="QueryListType">
    <xs:sequence
        maxOccurs="unbounded"
    >
        <xs:element name="Query"
            type="QueryType"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                  | Type                                                   | Description                                                                                                                     |
|----------------------------------------------------------|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**Query**](queryschema-query-querylisttype-element.md) | [**Affectée**](queryschema-querytype-complextype.md) | Définit un ensemble de sélecteurs et de suppressions utilisés pour inclure des événements dans ou exclure des événements du jeu de résultats.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 






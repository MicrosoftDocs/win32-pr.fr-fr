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
ms.openlocfilehash: e1692427538dcd500cd4190839ffcc148c7358e0aee7f5a27b4906192a0810b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904159"
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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 






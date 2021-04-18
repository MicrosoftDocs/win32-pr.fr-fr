---
title: Type complexe headerFieldType
description: Définit les éléments utilisés pour créer un champ d’en-tête dans un message électronique.
ms.assetid: 66036875-1116-46eb-b2f5-8c8ad8373ab1
keywords:
- Planificateur de tâches de type complexe headerFieldType
topic_type:
- apiref
api_name:
- headerFieldType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ddbc0ae22c6baf3fd288cbe2ead19dac506afee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512155"
---
# <a name="headerfieldtype-complex-type"></a>Type complexe headerFieldType

Définit les éléments utilisés pour créer un champ d’en-tête dans un message électronique.

``` syntax
<xs:complexType name="headerFieldType">
    <xs:all>
        <xs:element name="Name"
            type="nonEmptyString"
         />
        <xs:element name="Value"
            type="string"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                            | Type                                                                    | Description                                                            |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Nom**](taskschedulerschema-name-headerfieldtype-element.md)   | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Spécifie le nom du champ d’en-tête dans un message électronique.<br/> |
| [**Valeur**](taskschedulerschema-value-headerfieldtype-element.md) | **string**                                                              | Spécifie la valeur d’un champ d’en-tête dans un message électronique.<br/>  |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 






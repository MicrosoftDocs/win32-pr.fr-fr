---
title: Type complexe TypeListType
description: Définit les types utilisés dans le manifeste.
ms.assetid: e7ce0ecf-3bd0-49ab-82c7-dc28fd0e59a2
keywords:
- TypeListType type complexe EventLog
topic_type:
- apiref
api_name:
- TypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 61cec902684d7426a5951c12c4b319ae1ce29923
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192908"
---
# <a name="typelisttype-complex-type"></a>Type complexe TypeListType

Définit les types utilisés dans le manifeste.

``` syntax
<xs:complexType name="TypeListType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="xmlTypes"
            type="XmlTypeListType"
         />
        <xs:element name="inTypes"
            type="InputTypeListType"
         />
        <xs:any
            processContents="lax"
            namespace="##other"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                               | Type                                                                           | Description                                                                                                 |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**intypés**](eventmanifestschema-intypes-typelisttype-element.md)   | [**InputTypeListType**](eventmanifestschema-inputtypelisttype-complextype.md) | Définit une liste de types de données d’entrée.<br/>                                                              |
| [**xmlTypes**](eventmanifestschema-xmltypes-typelisttype-element.md) | [**XmlTypeListType**](eventmanifestschema-xmltypelisttype-complextype.md)     | Définit une liste de types de sortie que le service utilise pour déterminer comment restituer un type de données d’entrée.<br/> |



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 






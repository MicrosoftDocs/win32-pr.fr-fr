---
title: Élément String (StringTableType)
description: Définit une chaîne localisée.
ms.assetid: 845476a9-bcf4-4821-824c-06c9a9f64649
keywords:
- élément String EventLog
topic_type:
- apiref
api_name:
- string
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 82eae0fa7007790995617b2c26bc5aff2bca720fb689b9ac468ef551d3400e05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136172"
---
# <a name="string-stringtabletype-element"></a>Élément String (StringTableType)

Définit une chaîne localisée.

``` syntax
<xs:element name="string">
    <xs:complexType>
        <xs:attribute name="id"
            type="string"
            use="required"
         />
        <xs:attribute name="value"
            type="string"
            use="required"
         />
        <xs:attribute name="stringType"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

L’élément **String** est défini par le type complexe [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md) .

## <a name="attributes"></a>Attributs



| Nom       | Type   | Description                                                                           |
|------------|--------|---------------------------------------------------------------------------------------|
| id         | string | Identificateur qui identifie de façon unique la chaîne dans la table de chaînes.<br/> |
| stringType | string | Non utilisé.<br/>                                                                  |
| value      | string | La chaîne localisée.<br/>                                                      |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**stringTable (LocalizationType)**](eventmanifestschema-stringtable-localizationtype-element.md)
</dt> </dl>

 

 






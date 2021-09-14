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
ms.openlocfilehash: c46fc43366d6472e8047b529d847eefd5369c263
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008525"
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

 

 






---
title: Élément xmlType (XmlTypeListType)
description: Définit un type XML.
ms.assetid: 4443963f-f47a-4371-87d8-58f508ba15d6
keywords:
- élément de journal de l’élément xmlType
topic_type:
- apiref
api_name:
- xmlType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5aa37214c5efc0dee9e788ad10ed2f437e3df19f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192879"
---
# <a name="xmltype-xmltypelisttype-element"></a>Élément xmlType (XmlTypeListType)

Définit un type XML.

``` syntax
<xs:element name="xmlType">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="XmlType"
            >
                <xs:attribute name="name"
                    type="QName"
                    use="required"
                 />
                <xs:attribute name="value"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="symbol"
                    type="string"
                    use="required"
                 />
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

L’élément **xmlType** est défini par le type complexe [**XmlTypeListType**](eventmanifestschema-xmltypelisttype-complextype.md) .

## <a name="attributes"></a>Attributs



| Nom   | Type      | Description                                                                                                                                                                                                                                                |
|--------|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name   | **QName** | Nom du type de sortie.<br/>                                                                                                                                                                                                                    |
| symbole | string    | Symbole à utiliser pour référencer le type de sortie dans votre application. Le [**compilateur de message (MC.exe)**](message-compiler--mc-exe-.md) utilise le symbole pour créer une constante pour le type de sortie dans le fichier d’en-tête généré par le compilateur.<br/> |
| value  | string    | Valeur entière qui identifie de façon unique le type de sortie dans la liste des types de sortie que vous définissez.<br/>                                                                                                                                          |



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**xmlTypes (TypeListType)**](eventmanifestschema-xmltypes-typelisttype-element.md)
</dt> </dl>

 

 






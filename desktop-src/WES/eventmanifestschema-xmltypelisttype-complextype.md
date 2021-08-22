---
title: Type complexe XmlTypeListType
description: Définit une liste de types de sortie que le service utilise pour déterminer comment restituer un type de données d’entrée.
ms.assetid: d90b32cc-a0b5-44d1-8083-781aa5e10783
keywords:
- XmlTypeListType type complexe EventLog
topic_type:
- apiref
api_name:
- XmlTypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e30ca23a0e4ab0168ff7479a5246acfb4b34e3a43bc62886d988d5f54549672b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119620319"
---
# <a name="xmltypelisttype-complex-type"></a>Type complexe XmlTypeListType

Définit une liste de types de sortie que le service utilise pour déterminer comment restituer un type de données d’entrée.

``` syntax
<xs:complexType name="XmlTypeListType">
    <xs:sequence>
        <xs:element name="xmlType"
            minOccurs="0"
            maxOccurs="unbounded"
        >
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
                            type="CSymbolType"
                            use="required"
                         />
                    </xs:extension>
                </xs:complexContent>
            </xs:complexType>
        </xs:element>
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                | Type | Description                      |
|------------------------------------------------------------------------|------|----------------------------------|
| [**xmlType**](eventmanifestschema-xmltype-xmltypelisttype-element.md) |      | Définit un type XML. <br/> |



## <a name="attributes"></a>Attributs



| Nom   | Type                                                              | Description                                                                                                                                                                                                                                                |
|--------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name   | **QName**                                                         | Nom du type de sortie.<br/>                                                                                                                                                                                                                    |
| symbole | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Symbole à utiliser pour référencer le type de sortie dans votre application. Le [**compilateur de message (MC.exe)**](message-compiler--mc-exe-.md) utilise le symbole pour créer une constante pour le type de sortie dans le fichier d’en-tête généré par le compilateur.<br/> |
| value  | string                                                            | Valeur entière qui identifie de façon unique le type de sortie dans la liste des types de sortie que vous définissez.<br/>                                                                                                                                          |



## <a name="remarks"></a>Remarques

le \\ fichier include \\Winmeta.xml, inclus dans le SDK Windows, contient une liste de types de sortie prédéfinis.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 






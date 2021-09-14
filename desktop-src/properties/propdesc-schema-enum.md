---
description: Utilisé pour assigner du texte énuméré à des valeurs discrètes.
ms.assetid: c8cc040e-fcce-43a0-98c1-db2b2c616ac3
title: enum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b615697e669f8d02e0530a1763309cfe74113467
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235529"
---
# <a name="enum"></a>enum

Utilisé pour assigner du texte énuméré à des valeurs discrètes. N’importe quel nombre de ces éléments peut exister sous un [enumeratedList](./propdesc-schema-enumeratedlist.md). Par programme, elles sont représentées en tant qu’objets IPropertyEnumType, dont la méthode [**IPropertyEnumType :: GetEnumType**](/windows/win32/api/propsys/nf-propsys-ipropertyenumtype-getenumtype) retourne PET \_ DISCRETEVALUE.

## <a name="syntax"></a>Syntaxe


```
<!-- enum -->
<xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="image" minOccurs="0" maxOccurs="1"/>
        </xs:sequence>
        <xs:attribute name="value" type="xs:string" use="required"/>
        <xs:attribute name="text" type="xs:string" use="required"/>
        <xs:attribute name="mnemonics" type="xs:string"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                         | Éléments enfants |
|--------------------------------------------------------|----------------|
| [enumeratedList](./propdesc-schema-enumeratedlist.md) | Aucun           |



 

## <a name="attributes"></a>Attributs



| Attribut | Description                                                                                                                                                                                                          |
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| value     | Public. Obligatoire. Valeur discrète (chaîne ou nombre) à laquelle assigner le texte énuméré.                                                                                                                           |
| text      | Public. Obligatoire. Texte utilisé pour afficher la valeur énumérée. La syntaxe autorise une chaîne d’affichage directe ou une référence à une chaîne d’affichage indirecte ; Utilisez la chaîne d’affichage indirecte afin qu’elle puisse être localisée. |
| mnémoniques | **Windows 7 et versions ultérieures.** Public. Optionnel. Liste de valeurs mnémoniques qui peuvent être utilisées pour faire référence à la propriété dans les requêtes de recherche. La liste est délimitée par le \| caractère «».                                     |



 

 

 

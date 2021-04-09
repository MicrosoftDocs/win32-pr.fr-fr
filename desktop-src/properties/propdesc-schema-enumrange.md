---
description: Assigne un texte d’énumération à une plage de valeurs. Chaque élément enumRange spécifie une valeur minimale et s’étend jusqu’à la valeur minimale de l’élément suivant, ou jusqu’à ce qu’il n’y ait plus d’éléments enumRange.
ms.assetid: 00c56c2d-6693-4b09-b28a-21d69930bf35
title: enumRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 964835c376c5496d23e8d277409575758002a0d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951607"
---
# <a name="enumrange"></a>enumRange

Assigne un texte d’énumération à une plage de valeurs. Chaque élément [enumRange]() spécifie une valeur minimale et s’étend jusqu’à la valeur minimale de l’élément suivant, ou jusqu’à ce qu’il n’y ait plus d’éléments enumRange.

## <a name="syntax"></a>Syntaxe

``` syntax
<!-- enumRange -->
<xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="image" minOccurs="0" maxOccurs="1"/>
        </xs:sequence>
            <xs:attribute name="minValue" type="xs:integer" use="required"/>
            <xs:attribute name="setValue" type="xs:integer"/>
            <xs:attribute name="text" type="xs:string"/>
            <xs:attribute name="name" type="canonical-name"/> <!--Maximum of 64 characters-->
            <xs:attribute name="mnemonics" type="xs:string"/> 
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                         | Éléments enfants |
|--------------------------------------------------------|----------------|
| [enumeratedList](./propdesc-schema-enumeratedlist.md) | aucun           |



 

## <a name="attributes"></a>Attributs



| Attribut | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| minValue  | Public. Obligatoire. Valeur minimale de la plage.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| setValue  | Public. Optionnel. Lorsqu’un utilisateur sélectionne cette énumération à partir d’un contrôle de propriété ListBox, cette valeur discrète est affectée en tant que valeur de propriété.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| text      | Public. Optionnel. Texte utilisé pour afficher la valeur énumérée. La syntaxe autorise une chaîne d’affichage directe ou une référence à une chaîne d’affichage indirecte ; Utilisez la chaîne d’affichage indirecte afin qu’elle puisse être localisée.                                                                                                                                                                                                                                                                                                                                                                                                   |
| mnémoniques | **Windows 7 et versions ultérieures.** Public. Optionnel. Liste de valeurs mnémoniques qui peuvent être utilisées pour faire référence à la propriété dans les requêtes de recherche. La liste est délimitée par le \| caractère «».                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| name      | Obligatoire. Nom de propriété canonique, unique au système ; par exemple, System. Rating. Cet attribut est limité à 64 caractères. Le nom respecte la casse et doit utiliser la syntaxe suivante : Publisher. application. PropertyName. Les méthodes suivantes retournent cette valeur : [**IExplorerCommand :: GetCanonicalName**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getcanonicalname), [**IPropertyDescription :: GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname), [**IPropertyDescription2 :: GetCanonicalName**](/windows/desktop/api/Propsys/nn-propsys-ipropertydescription2)et [**IPropertyUI :: GetCanonicalName**](/previous-versions/windows/desktop/legacy/dd758076(v=vs.85)). |



 

 

 

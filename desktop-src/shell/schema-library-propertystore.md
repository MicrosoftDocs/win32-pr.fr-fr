---
description: L' <propertyStore> élément spécifie un ensemble d’une ou plusieurs propriétés utilisées par cette bibliothèque. Cet élément est facultatif et n’a pas d’attributs.
ms.assetid: 19532C1F-686F-4c14-8BA8-0043E77BE594
title: Élément propertyStore (schéma de bibliothèque)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0ff30972a358916e715ff1b374a555c6db24ee6d512d114bcf47f57ac8a1954
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452974"
---
# <a name="propertystore-element-library-schema"></a>Élément propertyStore (schéma de bibliothèque)

L' <propertyStore> élément spécifie un ensemble d’une ou plusieurs propriétés utilisées par cette bibliothèque. Cet élément est facultatif et n’a pas d’attributs.

## <a name="syntax"></a>Syntaxe

``` syntax
<!-- propertyStore -->
<xs:element name="propertyStore" minOccurs="0">
    <xs:complexType>
        <xs:complexContent>
            <!-- properties are extensions of propertyStoreType -->
            <xs:extension base="propertyStoreType"/>        
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                                               | Éléments enfants                                                   |
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Élément libraryDescription (schéma de bibliothèque)](schema-librarydescription.md) | [Property, élément (schéma de bibliothèque)](schema-library-property.md) |



 

## <a name="remarks"></a>Remarques

L' <propertyStore> élément peut avoir un ou plusieurs <property> éléments enfants.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Schéma de description de la bibliothèque](library-schema-entry.md)
</dt> <dt>

[Schéma de la description du connecteur de recherche](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 

---
description: L' &lt; &gt; élément propertyStore spécifie un ensemble d’une ou plusieurs propriétés utilisées par cette bibliothèque. Cet élément est facultatif et n’a pas d’attributs.
ms.assetid: 19532C1F-686F-4c14-8BA8-0043E77BE594
title: Élément propertyStore (schéma de bibliothèque)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 089e87e6e7bdfa568ffa2e8903f6347cb6dc7b3d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880425"
---
# <a name="propertystore-element-library-schema"></a>Élément propertyStore (schéma de bibliothèque)

L' &lt; &gt; élément propertyStore spécifie un ensemble d’une ou plusieurs propriétés utilisées par cette bibliothèque. Cet élément est facultatif et n’a pas d’attributs.

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

L' &lt; &gt; élément propertyStore peut avoir un ou plusieurs &lt; &gt; éléments enfants Property.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Schéma de description de la bibliothèque](library-schema-entry.md)
</dt> <dt>

[Schéma de la description du connecteur de recherche](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 

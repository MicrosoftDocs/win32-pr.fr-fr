---
description: Spécifie un alias de tri ou une liste d’alias de tri en spécifiant un élément qui contient une propriété de tri ou une liste de propriétés de tri.
ms.assetid: 4c514197-0df0-49c6-b39e-8a2a7cefa93d
title: aliasInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 052409864617bdaba7acbf9ae561752c83d18395
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521361"
---
# <a name="aliasinfo"></a>aliasInfo

Spécifie un alias de tri ou une liste d’alias de tri en spécifiant un élément qui contient une propriété de tri ou une liste de propriétés de tri. Il ne doit y avoir qu’un seul élément [aliasInfo]() pour chaque élément [PropertyDescription](./propdesc-schema-propertydescription.md) . Pour les propriétés qui définissent canGroupBy = true, à moins qu’une propriété de tri secondaire ne soit spécifiée ( aliasInfo/@additionalSortByAliases = prop : example), l’utilisateur peut connaître un comportement inattendu lors de la modification de l’ordre de tri dans une vue regroupée par la propriété. Plus précisément, l’ordre des groupes change, mais l’ordre des éléments dans les groupes ne l’est pas.

## <a name="syntax"></a>Syntaxe


```
<!-- aliasInfo -->
<xs:element name="aliasInfo">
    <xs:complexType>
        <xs:attribute name="sortByAlias" type="canonical-name"/>
        <xs:attribute name="additionalSortByAliases" type="proplist"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                                   | Éléments enfants |
|------------------------------------------------------------------|----------------|
| [propertyDescription](./propdesc-schema-propertydescription.md) | None           |



 

## <a name="attributes"></a>Attributs



| Attribut               | Description                                                                                                                                                            |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| sortByAlias             | Public. Optionnel. Nom canonique de la propriété à utiliser pour le tri. Cette chaîne est de type canonique.                                            |
| additionalSortByAliases | Public. Optionnel. Liste délimitée par des points-virgules des propriétés supplémentaires à utiliser lors du tri. Les propriétés sont appliquées au tri dans la séquence à laquelle elles sont fournies. |



 

 

 

---
description: Spécifie un alias de tri ou une liste d’alias de tri en spécifiant un élément qui contient une propriété de tri ou une liste de propriétés de tri.
ms.assetid: 4c514197-0df0-49c6-b39e-8a2a7cefa93d
title: aliasInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 087323df682a2f74164c530f18a9c4da8405930304186288a3d84635bb06ab55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118970968"
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
| [propertyDescription](./propdesc-schema-propertydescription.md) | Aucun           |



 

## <a name="attributes"></a>Attributs



| Attribut               | Description                                                                                                                                                            |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| sortByAlias             | Public. Facultatif. Nom canonique de la propriété à utiliser pour le tri. Cette chaîne est de type canonique.                                            |
| additionalSortByAliases | Public. Facultatif. Liste délimitée par des points-virgules des propriétés supplémentaires à utiliser lors du tri. Les propriétés sont appliquées au tri dans la séquence à laquelle elles sont fournies. |



 

 

 

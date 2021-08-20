---
description: Contient des informations de mise en forme pour les lignes horizontales utilisées pour le papier à lettres dans une note du journal.
ms.assetid: e3c9e7a8-8de6-4871-b386-2186883f2ee7
title: Élément horizontal
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97b66e8557d73570ce1a0b7eb7217c02435c51a6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482685"
---
# <a name="horizontal-element"></a>Élément horizontal

Contient des informations de mise en forme pour les lignes horizontales utilisées pour le papier à lettres dans une note du journal.

## <a name="definition"></a>Définition

``` syntax
<xs:element name="Horizontal" type="HorizontalType" minOccurs="0" />
```

## <a name="parent-elements"></a>Éléments parents

[**LineLayout**](linelayout-element.md)

## <a name="child-elements"></a>Éléments enfants

Aucun.

## <a name="attributes"></a>Attributs




| Attribut | Type | Obligatoire | Description | Valeurs possibles | 
|-----------|------|----------|-------------|-----------------|
| <strong>Style</strong> | SimpleType <a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> | Obligatoire | Spécifie le type de ligne à dessiner. | <ul><li>Aucun</li><li>Unie</li><li>Tiret</li><li>Points</li><li>Tiret-point</li><li>Tiret-point-point</li><li>Double</li></ul> | 
| <strong>Couleur</strong> | <a href="colortype-simple-type.md"><strong>ColorType</strong></a> , simpleType | Facultatif | Couleur de l’élément. | Valeur RVB hexadécimale. Correspond à l’expression régulière suivante : # [0-9A-zA-Z] {6} . Par exemple, #4a79B5.<br /> | 
| <strong>SpacingBefore</strong> | <strong>xs:nonNegativeInteger</strong> | Facultatif | Espacement avant l’élément. | Entier non négatif. | 
| <strong>SpacingBetween</strong> | <strong>xs:nonNegativeInteger</strong> | Facultatif | Espacement entre cet élément et les éléments environnants. | Entier non négatif. | 




 

## <a name="element-information"></a>Informations sur les éléments



|  Élément     | Valeur                                                     |
|--------------|-------------------------------------------------------------------|
| Type d'élément | [**ComplexType HorizontalType**](horizontaltype-complex-type.md) |
| Espace de noms    | urn : schemas-microsoft-com : TabletPC : RichInk                        |
| Nom du schéma  | Lecteur de journal                                                    |



 

 

 





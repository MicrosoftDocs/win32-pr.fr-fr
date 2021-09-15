---
description: Contient les informations qui décrivent le composant vertical des lignes du papier à lettres utilisé par la note du journal. Utilisé, par exemple, lorsque la note contient des lignes de grille.
ms.assetid: af6f485e-13df-41bb-b57a-10d8393b83e7
title: Élément vertical
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6f05ab8a2160dbf6b987177957e8285385fe4db
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312885"
---
# <a name="vertical-element"></a>Élément vertical

Contient les informations qui décrivent le composant vertical des lignes du papier à lettres utilisé par la note du journal. Utilisé, par exemple, lorsque la note contient des lignes de grille.

## <a name="definition"></a>Définition

``` syntax
<xs:element name="Vertical" type="VerticalType" minOccurs="0" />
```

## <a name="parent-elements"></a>Éléments parents

[**LineLayout**](linelayout-element.md)

## <a name="child-elements"></a>Éléments enfants

Aucun.

## <a name="attributes"></a>Attributs




| Attribut | Type | Obligatoire | Description | Valeurs possibles | 
|-----------|------|----------|-------------|-----------------|
| <strong>Style</strong> | SimpleType <a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> | Obligatoire | Spécifie le type de ligne à dessiner. | <ul><li>None</li><li>Unie</li><li>Tiret</li><li>Points</li><li>Tiret-point</li><li>Tiret-point-point</li><li>Double</li></ul> | 
| <strong>Couleur</strong> | <a href="colortype-simple-type.md"><strong>ColorType</strong></a> , simpleType | Facultatif | Couleur de l’élément. | Valeur RVB hexadécimale. Correspond à l’expression régulière suivante : # [0-9A-zA-Z] {6} . Par exemple, #4a79B5.<br /> | 
| <strong>SpacingBefore</strong> | <strong>xs:nonNegativeInteger</strong> | Facultatif | Espacement avant l’élément. | Entier non négatif. | 
| <strong>SpacingBetween</strong> | <strong>xs:nonNegativeInteger</strong> | Facultatif | Espacement entre cet élément et les éléments environnants. | Entier non négatif. | 




 

## <a name="element-information"></a>Informations sur les éléments



|  Élément     | Valeur                                                         |
|--------------|---------------------------------------------------------------|
| Type d'élément | ComplexType [**VerticalType**](verticaltype-complex-type.md) |
| Espace de noms    | urn : schemas-microsoft-com : TabletPC : RichInk                    |
| Nom du schéma  | Lecteur de journal                                                |



 

 

 





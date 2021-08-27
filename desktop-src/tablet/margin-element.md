---
description: Définit les lignes de marge dessinées sur la page.
ms.assetid: c3047706-affd-4feb-9d48-cfb4c7dd6fa0
title: Élément Margin
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c264c2470d070353d1fd19340a161cf765bc05
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478665"
---
# <a name="margin-element"></a>Élément Margin

Définit les lignes de marge dessinées sur la page.

## <a name="definition"></a>Définition

``` syntax
<xs:complexType name="MarginType">
   <xs:attribute name="Style" use="required" type="LineLayoutStyleType" />
   <xs:attribute name="Color" type="ColorType" />
   <xs:attribute name="Type" type="MarginTypeType" />
   <xs:attribute name="Spacing" type="xs:positiveInteger" />
</xs:complexType>
```

## <a name="parent-elements"></a>Éléments parents

Aucun.

## <a name="child-elements"></a>Éléments enfants

Aucun..

## <a name="attributes"></a>Attributs




| Attribut | Type | Obligatoire | Description | Valeurs possibles | 
|-----------|------|----------|-------------|-----------------|
| <strong>Style</strong> | SimpleType <a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> | Obligatoire | Spécifie le type de ligne à dessiner. | <ul><li>Aucun</li><li>Unie</li><li>Tiret</li><li>Points</li><li>Tiret-point</li><li>Tiret-point-point</li><li>Double</li></ul> | 
| <strong>Couleur</strong> | <a href="colortype-simple-type.md"><strong>ColorType</strong></a> , simpleType | Facultatif | Couleur de l’élément. | Valeur RVB hexadécimale. Correspond à l’expression régulière suivante : # [0-9A-zA-Z] {6} . Par exemple, #4a79B5.<br /> | 
| <strong>Type</strong> | SimpleType <a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a> | Facultatif | Indique la marge de gauche ou de droite. | <ul><li>Gauche</li><li>Right</li></ul> | 
| <strong>Espacement</strong> | <strong>xs:nonNegativeInteger</strong> | Facultatif | Espacement entre les bords des pages et des marges. | Entier non négatif. | 




 

## <a name="element-information"></a>Informations sur les éléments



|  Élément     | Valeur                                                     |
|--------------|-----------------------------------------------------------|
| Type d'élément | ComplexType [**MarginType**](margintype-complex-type.md) |
| Espace de noms    | urn : schemas-microsoft-com : TabletPC : RichInk                |
| Nom du schéma  | Lecteur de journal                                            |



 

 

 





---
description: Contient des informations de titre sur la note du journal.
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Titre, élément
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05661be8566cf4136194af4e08d8f9774d3413dc
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473135"
---
# <a name="title-element"></a>Titre, élément

Contient des informations de titre sur la note du journal.

## <a name="definition"></a>Définition

``` syntax
<xs:element name="Title" type="TitleType" minOccurs="0" />
```

## <a name="parent-elements"></a>Éléments parents

[**Stationery**](stationery-element.md)

## <a name="child-elements"></a>Éléments enfants

[**Partie titlearea**](titlearea-element.md)

## <a name="attributes"></a>Attributs




| Attribut | Type | Obligatoire | Description | Valeurs possibles | 
|-----------|------|----------|-------------|-----------------|
| <strong>Style</strong> | <strong>xs:string</strong> | Obligatoire | Spécifie le type de bordure entourant le titre de la note. | <ul><li>Aucun</li><li>SolidSquare</li><li>OutlineSquare</li><li>SolidRoundRect</li><li>OutlineRoundRect</li><li>SolidRoundRectDottedBaseline</li></ul> | 
| <strong>DateStyle</strong> | <strong>xs:string</strong> | Obligatoire | Définit si le titre contient une date ou non. | <ul><li>Aucun</li><li>Court</li></ul> | 
| <strong>Couleur</strong> | <a href="colortype-simple-type.md"><strong>ColorType, simpleType</strong></a> | Facultatif | Spécifie la couleur de l'arrière-plan. | Voir <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>. | 




 

## <a name="element-information"></a>Informations sur les éléments



| Élément      | Valeur                                                   |
|--------------|---------------------------------------------------------|
| Type d'élément | ComplexType [**TitleType**](titletype-complex-type.md) |
| Espace de noms    | urn : schemas-microsoft-com : TabletPC : RichInk              |
| Nom du schéma  | Lecteur de journal                                          |



 

 

 




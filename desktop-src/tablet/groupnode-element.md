---
description: Contient un ensemble d’éléments&\# 8212 ; Paragraph, InkWord, Drawing, text, image ou Flag&\# 8212 ; qui sont regroupés dans la note du journal.
ms.assetid: 59ee3037-7178-41c8-84d5-d5c68fa2cf9b
title: Élément, nœud
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ee141691ef58d14e6c08a49544e9cf3ecf7540b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516887"
---
# <a name="groupnode-element"></a>Élément, nœud

Contient un ensemble d’éléments ([**paragraphe**](paragraph-element.md), [**InkWord**](inkword-element.md), [**dessin**](drawing-element.md), [**texte**](text-element.md), [**image**](image-element.md)ou [**indicateur**](flag-element.md)) regroupés dans la note du journal.

## <a name="definition"></a>Définition

``` syntax
<xs:element name="GroupNode" type="GroupNodeType" />
```

## <a name="parent-elements"></a>Éléments parents

[**Content**](content-element--journal-reader.md)

## <a name="child-elements"></a>Éléments enfants

[**Paragraph**](paragraph-element.md)

[**InkWord**](inkword-element.md)

[**Schéma**](drawing-element.md)

[**Texte**](text-element.md)

[**Image**](docimage-element.md)

[**Indicateur**](flag-element.md)

## <a name="attributes"></a>Attributs



| Attribut  | Type                      | Obligatoire | Description                                                                             | Valeurs possibles           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Obligatoire | Distance entre l’origine et le point le plus à gauche dans le cadre englobant de l’élément. | N’importe quel entier.              |
| **Top**    | **xs:integer**            | Obligatoire | Distance entre l’origine et le point le plus élevé dans le cadre englobant de l’élément.  | N’importe quel entier.              |
| **Width**  | **xs:nonNegativeInteger** | Obligatoire | Largeur de la zone englobante pour l’élément.                                          | Entier non négatif. |
| **Height** | **xs:nonNegativeInteger** | Obligatoire | Hauteur du rectangle englobant pour l’élément.                                         | Entier non négatif. |



 

## <a name="element-information"></a>Informations sur les éléments



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| Type d'élément | ComplexType [**GroupNodeType**](groupnodetype-complex-type.md) |
| Espace de noms    | urn : schemas-microsoft-com : TabletPC : RichInk                      |
| Nom du schéma  | Lecteur de journal                                                  |



 

 

 




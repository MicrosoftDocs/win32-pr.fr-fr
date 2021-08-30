---
description: Contient un ensemble d’éléments&\# 8212 ; Paragraph, InkWord, Drawing, text, image ou Flag&\# 8212 ; qui sont regroupés dans la note du journal.
ms.assetid: 59ee3037-7178-41c8-84d5-d5c68fa2cf9b
title: Élément, nœud
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1dd4258628fbd40c19f8cb1acf3fd0bacbc5557abb967b879dcb78031736288
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008589"
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

[**Dessin**](drawing-element.md)

[**Financière**](text-element.md)

[**Image**](docimage-element.md)

[**Activé**](flag-element.md)

## <a name="attributes"></a>Attributs



| Attribut  | Type                      | Obligatoire | Description                                                                             | Valeurs possibles           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Obligatoire | Distance entre l’origine et le point le plus à gauche dans le cadre englobant de l’élément. | N’importe quel entier.              |
| **Top**    | **xs:integer**            | Obligatoire | Distance entre l’origine et le point le plus élevé dans le cadre englobant de l’élément.  | N’importe quel entier.              |
| **Width**  | **xs:nonNegativeInteger** | Obligatoire | Largeur de la zone englobante pour l’élément.                                          | Entier non négatif. |
| **Height** | **xs:nonNegativeInteger** | Obligatoire | Hauteur du rectangle englobant pour l’élément.                                         | Entier non négatif. |



 

## <a name="element-information"></a>Informations sur les éléments



|  Élément     | Valeur                                                     |
|--------------|-----------------------------------------------------------------|
| Type d'élément | ComplexType [**GroupNodeType**](groupnodetype-complex-type.md) |
| Espace de noms    | urn : schemas-microsoft-com : TabletPC : RichInk                      |
| Nom du schéma  | Lecteur de journal                                                  |



 

 

 




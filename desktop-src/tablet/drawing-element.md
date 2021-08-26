---
description: Contient le contenu qui a été classifié par l’analyseur ou par l’utilisateur en tant que dessin.
ms.assetid: 566542f3-b824-442d-9d8b-0064ebcf9b68
title: Élément Drawing
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d44eab0f9feec4b80369a365663917ca1aea0f211bba70dd4b99e9161316c662
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936589"
---
# <a name="drawing-element"></a>Élément Drawing

Contient le contenu qui a été classifié par l’analyseur ou par l’utilisateur en tant que dessin.

## <a name="definition"></a>Définition

``` syntax
<xs:element name="Drawing" type="DrawingType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Éléments parents

[**Content**](content-element--journal-reader.md)

[**, Nœud**](groupnode-element.md)

## <a name="child-elements"></a>Éléments enfants

[**ScalarTransform**](scalartransform-element.md)

[**CanReClassify**](canreclassify-element.md)

[**InkClass**](inkclass-element.md)

[**InkObject**](inkobject-element.md)

## <a name="attributes"></a>Attributs



| Attribut  | Type                      | Obligatoire | Description                                                                             | Valeurs possibles           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Obligatoire | Distance entre l’origine et le point le plus à gauche dans le cadre englobant de l’élément. | N’importe quel entier.              |
| **Top**    | **xs:integer**            | Obligatoire | Distance entre l’origine et le point le plus élevé dans le cadre englobant de l’élément.  | N’importe quel entier.              |
| **Width**  | **xs:nonNegativeInteger** | Obligatoire | Largeur de la zone englobante pour l’élément.                                          | Entier non négatif. |
| **Height** | **xs:nonNegativeInteger** | Obligatoire | Hauteur du rectangle englobant pour l’élément.                                         | Entier non négatif. |



 

## <a name="element-information"></a>Informations sur les éléments



|  Élément     | Valeur                                                     |
|--------------|-------------------------------------------------------------|
| Type d'élément | ComplexType [**DrawingType**](drawingtype-complex-type.md) |
| Espace de noms    | urn : schemas-microsoft-com : TabletPC : RichInk                  |
| Nom du schéma  | Lecteur de journal                                              |



 

 

 




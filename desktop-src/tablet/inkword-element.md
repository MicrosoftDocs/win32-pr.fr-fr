---
description: Contient des informations sur un mot manuscrit donné dans la note du journal, notamment la position, les alternatives et les données d’encre réelles.
ms.assetid: 1e197716-bf6c-4a28-ae66-38aa59d7371d
title: Élément InkWord
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8dc9baea7cda0346e82c11331c45f453e61f192
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432391"
---
# <a name="inkword-element"></a>Élément InkWord

Contient des informations sur un mot manuscrit donné dans la note du journal, notamment la position, les alternatives et les données d’encre réelles.

## <a name="definition"></a>Définition

``` syntax
<xs:element name="InkWord" type="InkWordType" />
```

## <a name="parent-elements"></a>Éléments parents

[**, Nœud**](groupnode-element.md)

[**Spline**](line-element.md)

## <a name="child-elements"></a>Éléments enfants

[**ScalarTransform**](scalartransform-element.md)

[**AlternateList**](alternatelist-element.md)

[**CanReClassify**](canreclassify-element.md)

[**Garantir**](confidence-element.md)

[**InkObject**](inkobject-element.md)

## <a name="attributes"></a>Attributs



| Attribut  | Type                      | Obligatoire | Description                                                                             | Valeurs possibles           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Obligatoire | Distance entre l’origine et le point le plus à gauche dans le cadre englobant de l’élément. | N’importe quel entier.              |
| **Top**    | **xs:integer**            | Obligatoire | Distance entre l’origine et le point le plus élevé dans le cadre englobant de l’élément.  | N’importe quel entier.              |
| **Width**  | **xs:nonNegativeInteger** | Obligatoire | Largeur de la zone englobante pour l’élément.                                          | Entier non négatif. |
| **Height** | **xs:nonNegativeInteger** | Obligatoire | Hauteur du rectangle englobant pour l’élément.                                         | Entier non négatif. |



 

> [!WARNING]
> Le mappage de coordonnées internes du mot d’encre est l’unité métrique anglaise et un multiplicateur de 2,54 doit être utilisé par votre application pour convertir les valeurs de largeur et de hauteur en unités HIMETRIC utilisées par les API de la plateforme Tablet PC.

 

## <a name="element-information"></a>Informations sur les éléments



|  Élément     | Valeur                                                     |
|--------------|-------------------------------------------------------------|
| Type d'élément | ComplexType [**InkWordType**](inkwordtype-complex-type.md) |
| Espace de noms    | urn : schemas-microsoft-com : TabletPC : RichInk                  |
| Nom du schéma  | Lecteur de journal                                              |



 

 

 




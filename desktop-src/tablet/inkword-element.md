---
description: Contient des informations sur un mot manuscrit donné dans la note du journal, notamment la position, les alternatives et les données d’encre réelles.
ms.assetid: 1e197716-bf6c-4a28-ae66-38aa59d7371d
title: Élément InkWord
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 179fb5e2bcce2e01f684f0b39d662e8538c7d27e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536682"
---
# <a name="inkword-element"></a>Élément InkWord

Contient des informations sur un mot manuscrit donné dans la note du journal, notamment la position, les alternatives et les données d’encre réelles.

## <a name="definition"></a>Définition

``` syntax
<xs:element name="InkWord" type="InkWordType" />
```

## <a name="parent-elements"></a>Éléments parents

[**, Nœud**](groupnode-element.md)

[**Lignes**](line-element.md)

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



|              |                                                             |
|--------------|-------------------------------------------------------------|
| Type d'élément | ComplexType [**InkWordType**](inkwordtype-complex-type.md) |
| Espace de noms    | urn : schemas-microsoft-com : TabletPC : RichInk                  |
| Nom du schéma  | Lecteur de journal                                              |



 

 

 




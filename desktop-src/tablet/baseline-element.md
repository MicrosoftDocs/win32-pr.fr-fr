---
description: Fournit des informations (x, y) pour les points de départ et de fin de la ligne de base d’un paragraphe dans le document journal. L’espace de coordonnées utilisé pour ces valeurs est HIMETRIC.
ms.assetid: ff6a97ad-0e48-4128-8f94-24802b6ddc05
title: Élément de ligne de base
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d97e5bd5aecf6833ef4e0bc5b3298442c911838ed714740448ae82305dd00eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118046193"
---
# <a name="baseline-element"></a>Élément de ligne de base

Fournit des informations (x, y) pour les points de départ et de fin de la ligne de base d’un paragraphe dans le document journal. L’espace de coordonnées utilisé pour ces valeurs est **HIMETRIC**.

## <a name="definition"></a>Définition

``` syntax
<xs:element name="Baseline" type="BaseLineType" />
```

## <a name="parent-elements"></a>Éléments parents

[**ParagraphLineMetrics**](paragraphlinemetrics-element.md)

## <a name="child-elements"></a>Éléments enfants

Aucun.

## <a name="attributes"></a>Attributs



| Attribut  | Type                      | Obligatoire | Description                                                      | Valeurs possibles           |
|------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| **StartX** | **xs:nonNegativeInteger** | Obligatoire | Valeur X du point marquant le début de la ligne de base. | Entier non négatif. |
| **Démarrer** | **xs:nonNegativeInteger** | Obligatoire | Valeur Y du point marquant le début de la ligne de base. | Entier non négatif. |
| **EndX**   | **xs:nonNegativeInteger** | Obligatoire | Valeur X du point marquant la fin de la ligne de base.       | Entier non négatif. |



 

## <a name="element-information"></a>Informations sur les éléments



|                  | Valeur                                                         |
|------------------|---------------------------------------------------------------|
| **Type d’élément** | ComplexType [**BaselineType**](baselinetype-complex-type.md) |
| **Espace de noms**    | urn : schemas-microsoft-com : TabletPC : RichInk                    |
| **Nom du schéma**  | Lecteur de journal                                                |



 

 

 




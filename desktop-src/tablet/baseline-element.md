---
description: Fournit des informations (x, y) pour les points de départ et de fin de la ligne de base d’un paragraphe dans le document journal. L’espace de coordonnées utilisé pour ces valeurs est HIMETRIC.
ms.assetid: ff6a97ad-0e48-4128-8f94-24802b6ddc05
title: Élément Baseline
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bc64f332608b4bd0281ae2a7f29db96101e9d2e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530349"
---
# <a name="baseline-element"></a>Élément Baseline

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



 

 

 




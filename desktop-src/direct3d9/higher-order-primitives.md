---
description: Direct3D 9 prend en charge les points, lignes, triangles et primitives de grille.
ms.assetid: 474e8bee-336d-491f-afa0-f0186a8d19c7
title: Higher-Order primitives (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67767dd955fa5c0c5c21315d7c1c510de422870c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126998620"
---
# <a name="higher-order-primitives-direct3d-9"></a>Higher-Order primitives (Direct3D 9)

Direct3D 9 prend en charge les points, lignes, triangles et primitives de grille. Ils ont été étendus pour prendre en charge l’interpolation d’ordre supérieur au-delà de la linéarité. Alors que les triangles et les lignes ont une étendue spatiale, jusqu’à ce qu’ils aient été affichés à la fois à l’aide d’une interpolation linéaire. Dans Direct3D 9, Direct3D prend en charge le rendu de ces types primitifs à l’aide d’une commande plus élevée, jusqu’à quintaux, interpolation. En outre, un nouveau type de primitive Quad est désormais pris en charge. Ce nouveau type peut également être rendu avec une interpolation d’ordre supérieur. Cette fonctionnalité est principalement pilotée par les exigences relatives à l’animation et au rendu des caractères. Il peut également être utilisé pour d’autres surfaces, telles que le sol ou l’eau.

Les primitives d’ordre supérieur prennent en charge l’interpolation d’ordre supérieur lorsqu’elles sont transmises à l’API sous forme de listes, de bandes, de ventilateurs ou de maillages indexés. Cela est possible en utilisant des informations supplémentaires encodées dans les vertex eux-mêmes. Par exemple, les vecteurs normaux peuvent être utilisés pour définir des plans tangents aux sommets pour activer l’interpolation cubique. La plupart des implémentations prennent en charge l’interpolation d’ordre supérieur par pavage en triangles planaires. L’étape de pavage est appliquée logiquement avant l’étape du nuanceur de sommets. Étant donné que l’API vertex shader n’impose pas de sémantique sur ses données d’entrée, un mécanisme spécial est fourni pour identifier le composant de flux de vertex qui représente la position et éventuellement le vecteur normal. Tous les autres composants sont interpolés en conséquence.

Cette section présente les primitives d’ordre supérieur et explique comment elles peuvent être utilisées dans vos applications. Les informations sont réparties dans les rubriques suivantes.

-   [Amélioration de la qualité grâce à l’amélioration de la résolution](#improved-quality-through-resolution-enhancement)
-   [Mappage direct à partir des outils de Spline-Based](#direct-mapping-from-spline-based-tools)

## <a name="improved-quality-through-resolution-enhancement"></a>Amélioration de la qualité grâce à l’amélioration de la résolution

Les primitives actuelles ne sont pas idéales pour représenter des surfaces lissées. Les méthodes d’interpolation d’ordre supérieur, telles que les polynômes cubiques, permettent des calculs plus précis dans le rendu des formes courbées. Cela permet d’augmenter le réalisme en réduisant ou en éliminant les artefacts de facettes visibles sur les bords silhouettes ou sur l’éclairage de surface spéculaire. En outre, lorsque le pavage se produit sur la puce, les triangles fractionnés n’ont pas d’impact sur la bande passante du bus. Dans de nombreux cas, une petite quantité de pavage peut apporter des améliorations en matière de qualité d’image avec un impact minime sur les performances.

Direct3D 9 offre un moyen simple d’appliquer une amélioration de la résolution au contenu créé par les outils et les pipelines d’art basés sur Polygon existants. L’application n’a besoin que de fournir un niveau de pavage souhaité et transmet les données à l’aide d’une syntaxe de triangle standard qui comprend des vecteurs normaux.

## <a name="direct-mapping-from-spline-based-tools"></a>Mappage direct à partir des outils de Spline-Based

De nombreux outils de création actuels prennent en charge des primitives d’ordre supérieur pour permettre des opérations de modélisation plus puissantes que celles couramment fournies pour les maillages de triangles planaires. Lorsqu’ils sont utilisés efficacement, afin que le nombre de correctifs générés soit raisonnable, ces outils peuvent produire du contenu qui peut être rendu directement par l’API. Pour répondre à cette exigence, un nouveau point d’entrée interprète le flux de données de vertex entrant comme un tableau de points de contrôle 2D et le tessellates à la résolution souhaitée.

-   [Utilisation de primitives Higher-Order (Direct3D 9)](using-higher-order-primitives.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Pipeline de vertex](vertex-pipeline.md)
</dt> </dl>

 

 




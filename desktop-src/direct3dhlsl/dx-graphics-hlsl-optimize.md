---
title: Optimisation des nuanceurs HLSL
description: Cette section décrit les stratégies à usage général que vous pouvez utiliser pour optimiser vos nuanceurs. Vous pouvez appliquer ces stratégies aux nuanceurs écrits dans n’importe quel langage, sur n’importe quelle plateforme.
ms.assetid: 014b9cb3-a489-48d7-8174-b97de168bf3a
keywords:
- langage de nuanceur de haut niveau
- HLSL, performances
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 06d3bb806e98e489020aa1755ef2a6c952459d86
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228174"
---
# <a name="optimizing-hlsl-shaders"></a>Optimisation des nuanceurs HLSL

Cette section décrit les stratégies à usage général que vous pouvez utiliser pour optimiser vos nuanceurs. Vous pouvez appliquer ces stratégies aux nuanceurs écrits dans n’importe quel langage, sur n’importe quelle plateforme.

-   [Savoir où effectuer les calculs des nuanceurs](#know-where-to-perform-shader-calculations)
-   [Ignorer les instructions inutiles](#skip-unnecessary-instructions)
-   [Variables et interpolations de Pack](#pack-variables-and-interpolants)
-   [Réduire la complexité des nuanceurs](#reduce-shader-complexity)
-   [Rubriques connexes](#related-topics)
-   [Rubriques connexes](#related-topics)

## <a name="know-where-to-perform-shader-calculations"></a>Savoir où effectuer les calculs des nuanceurs

Les nuanceurs vertex effectuent des opérations qui incluent l’extraction des sommets et la transformation de matrice des données de vertex. En règle générale, les nuanceurs de vertex sont exécutés une fois par vertex.

Les nuanceurs de pixels effectuent des opérations qui incluent l’extraction des données de texture et l’exécution de calculs d’éclairage. En règle générale, les nuanceurs de pixels sont exécutés une fois par pixel pour un élément de géométrie donné.

En général, le nombre de pixels dans une scène, les nuanceurs de pixels s’exécutent plus souvent que les nuanceurs de vertex.

Lorsque vous concevez des algorithmes de nuanceur, gardez à l’esprit les points suivants :

-   Effectuez des calculs sur le nuanceur de sommets, si possible. Un calcul effectué sur un nuanceur de pixels est beaucoup plus onéreux qu’un calcul effectué sur un nuanceur de sommets.
-   Envisagez d’utiliser des calculs par vertex pour améliorer les performances dans des situations telles que des maillages denses. Pour les maillages denses, les calculs par vertex peuvent produire des résultats qui ne se distinguent pas visuellement des résultats produits par des calculs par pixel.

## <a name="skip-unnecessary-instructions"></a>Ignorer les instructions inutiles

En HLSL, la fonctionnalité de branchement dynamique permet de limiter le nombre d’instructions exécutées. Par conséquent, la création de branche dynamique peut accélérer la durée d’exécution du nuanceur. Si la géométrie ou les pixels ne sont pas affichés, utilisez la branche dynamique pour quitter le nuanceur ou pour limiter les instructions. Par exemple, si un pixel n’est pas allumé, il n’y a aucun point dans l’exécution de l’algorithme d’éclairage.

Le tableau suivant répertorie certains cas où vous pouvez tester des conditions dans votre nuanceur et utiliser la branche dynamique pour ignorer les instructions inutiles. La table n’est pas exhaustive. Au lieu de cela, elle est destinée à vous donner des idées pour l’optimisation de votre code.



| Condition à vérifier                                    | Réponse dans le nuanceur       |
|-------------------------------------------------------|------------------------------|
| La vérification alpha détermine qu’un pixel ne sera pas visible. | Ignorez le reste du nuanceur. |
| Le pixel ou la géométrie est entièrement buée.                | Ignorez le reste du nuanceur. |
| Les pondérations de la peau sont égales à zéro.                                | Ignore les segments.                  |
| L’atténuation légère est égale à zéro.                            | Ignorer l’éclairage.               |
| Terme Lambert non positif.                         | Ignorer l’éclairage.               |



 

## <a name="pack-variables-and-interpolants"></a>Variables et interpolations de Pack

Gardez à l’esprit l’espace requis pour les données de nuanceur. Compressez autant d’informations que possible dans une variable ou une interpolation. Parfois, les informations de deux variables peuvent être empaquetées dans l’espace mémoire d’une variable unique.

## <a name="reduce-shader-complexity"></a>Réduire la complexité des nuanceurs

N’oubliez pas que vos nuanceurs sont petits et simples. En général, les nuanceurs avec moins d’instructions s’exécutent plus rapidement que les nuanceurs avec davantage d’instructions. Il est également plus facile de déboguer et d’optimiser des nuanceurs plus petits et moins complexes.

## <a name="related-topics"></a>Rubriques connexes

[Guide de programmation pour HLSL](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation pour HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 





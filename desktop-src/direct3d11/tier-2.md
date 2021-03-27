---
title: Niveau 2
description: Cette section décrit le support de niveau 2.
ms.assetid: 4A4AEF13-2F0F-482E-9262-256C257ED85A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58fa6e8ff3dba5780e3507bb2da5273e327a30e1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842494"
---
# <a name="tier-2"></a>Niveau 2

Cette section décrit le support de niveau 2.

-   Matériel au niveau de la fonctionnalité 11,1 minimum.
-   Toutes les fonctionnalités du niveau précédent (sans limitations spécifiques au [niveau 1](tier-1.md) ), ainsi que les ajouts apportés aux éléments suivants :
-   Les instructions du nuanceur pour le déverrouillage du LOD et les commentaires d’État mappés sont disponibles. Pour plus d’informations, consultez [exposition des ressources en mosaïque HLSL](hlsl-tiled-resources-exposure.md).
-   Les lectures à partir de vignettes non mappées retournent 0 dans tous les composants non manquants du format, et la valeur par défaut pour les composants manquants.
-   Les écritures dans les vignettes non mappées sont arrêtées du passage à la mémoire, mais elles peuvent se trouver dans les caches que les lectures ultérieures vers la même adresse peuvent ou non être levées.
-   Le filtrage de texture avec un encombrement qui chevauche les vignettes **null** et non **null** contribue à 0 (avec des valeurs par défaut pour les composants de format manquants) pour les texels sur les vignettes **null** dans l’opération de filtre globale. Un matériel précoce ne répond pas à cette exigence et retourne 0 (avec des valeurs par défaut pour les composants de format manquants) pour le résultat de filtre complet si des texels (avec une pondération différente de zéro) tombent sur une vignette **null** . Aucun autre matériel ne sera autorisé à manquer l’obligation d’inclure tous les texels (avec une pondération différente de zéro) dans l’opération de filtre.
-   Les accès texels **null** entraînent l’opération [**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) sur les commentaires d’État pour qu’une texture lue retourne la valeur false. C’est quelle que soit la façon dont le résultat de l’accès à la texture peut obtenir un masque d’écriture dans le nuanceur et le nombre de composants dans le format de texture (la combinaison peut faire apparaître que la texture n’a pas besoin d’être accessible).
-   Contraintes d’alignement pour les formes de mosaïques standard : les des mipmaps qui remplissent au moins une vignette standard dans toutes les dimensions sont assurés d’utiliser la mosaïque standard, le reste étant considéré comme une **unité** dans n vignettes (n signalées à l’application). L’application peut mapper les N vignettes dans des emplacements arbitrairement disjoints dans un pool de mosaïques, mais doit mapper tout ou aucune des vignettes compressées. La compression MIP est un ensemble unique de vignettes compressées par tranche de tableau.
-   Le filtrage de réduction min/max est pris en charge. Pour plus d’informations sur le filtrage de réduction min/max, consultez [fonctionnalités d’échantillonnage de texture des ressources en mosaïque](tiled-resources-texture-sampling-features.md).
-   Les ressources en mosaïque avec un des mipmaps inférieur à la taille de mosaïque standard dans une dimension ne sont pas autorisées à avoir une taille de tableau supérieure à 1.
-   Limitations sur la façon dont les vignettes sont accessibles lorsqu’il existe des mappages en double, décrits dans [limitations d’accès aux vignettes avec des mappages dupliqués](tile-access-limitations-with-duplicate-mappings-.md), continuez à appliquer.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Niveaux de fonctionnalités des ressources en mosaïque](tiled-resources-features-tiers.md)
</dt> </dl>

 

 
---
title: Fonctionnalités d’échantillonnage de texture des ressources en mosaïque
description: Cette section décrit les fonctionnalités d’échantillonnage de texture des ressources en mosaïque.
ms.assetid: E56737CE-C468-4D3C-84EE-E8EB2AB6F505
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd46c96219e54aea6990e91de8e340fdca5e32b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728725"
---
# <a name="tiled-resources-texture-sampling-features"></a>Fonctionnalités d’échantillonnage de texture des ressources en mosaïque

Cette section décrit les fonctionnalités d’échantillonnage de texture des ressources en mosaïque.

## <a name="requirements-of-tiled-resources-texture-sampling-features"></a>Spécifications des fonctionnalités d’échantillonnage de texture des ressources en mosaïque

Les fonctionnalités d’échantillonnage de texture décrites ici nécessitent un niveau de prise en charge des ressources en mosaïque de niveau [2](tier-2.md) .

## <a name="shader-feedback-about-mapped-areas"></a>Commentaires du nuanceur sur les zones mappées

Toute instruction de nuanceur qui lit et/ou écrit dans une ressource en mosaïque entraîne l’enregistrement des informations d’État. Cet État est exposé sous la forme d’une valeur de retour supplémentaire facultative sur chaque instruction d’accès aux ressources qui passe dans un registre temporaire 32 bits. Le contenu de la valeur de retour est opaque. Autrement dit, la lecture directe par le programme Shader n’est pas autorisée. Toutefois, vous pouvez utiliser la fonction [**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) pour extraire les informations d’État.

## <a name="fully-mapped-check"></a>Vérification entièrement mappée

La fonction [**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) interprète l’état retourné par un accès à la mémoire et indique si toutes les données en cours d’accès ont été mappées dans la ressource. **CheckAccessFullyMapped** retourne true (0xFFFFFFFF) si les données ont été mappées ou false (0x00000000) si les données n’ont pas été mappées.

Pendant les opérations de filtre, parfois, le poids d’une Texel donnée finit par 0,0. Par exemple, un échantillon linéaire avec des coordonnées de texture qui se trouvent directement sur un centre de Texel : 3 les autres éléments texels (qui peuvent varier en fonction du matériel) contribuent au filtre, mais avec un poids de 0. Ces texels de poids 0 ne contribuent pas du tout au résultat du filtre. par conséquent, s’ils se trouvent sur des vignettes **null** , ils ne sont pas comptabilisés comme un accès non mappé. Notez que la même garantie s’applique aux filtres de texture qui incluent plusieurs niveaux MIP ; Si les texels de l’un des des mipmaps ne sont pas mappés mais que le poids de ces texels est 0, ces texels ne sont pas comptabilisés comme un accès non mappé.

Lors de l’échantillonnage à partir d’un format qui a moins de 4 composants (tels que le \_ format dxgi \_ R8 \_ UNORM), les texels qui se trouvent sur des vignettes **null** entraînent le signalement d’un accès mappé **null** , quels que soient les composants que le nuanceur examine réellement dans le résultat. Par exemple, la lecture de R8 \_ UNORM et le masquage du résultat de lecture dans le nuanceur avec. GBA/. YZW ne semblent pas avoir besoin de lire la texture. Toutefois, si l’adresse Texel est une vignette mappée **null** , l’opération est toujours comptabilisée comme un accès de mappage **null** .

Le nuanceur peut vérifier l’État et poursuivre les actions à entreprendre en cas d’échec. Par exemple, un cours d’action peut enregistrer « échecs » (par exemple, via UAV Write) et/ou émettre une autre lecture ancrée à un LOD plus grossiste connu pour être mappé. Une application peut souhaiter effectuer un suivi des accès réussis afin d’obtenir une idée de la partie de l’ensemble mappé de vignettes ayant fait l’objet d’un accès.

L’une des complications pour la journalisation est qu’il n’existe aucun mécanisme pour signaler le jeu exact de vignettes qui aurait été accédé. L’application peut effectuer des suppositions prudentes en se basant sur les coordonnées qu’elle utilisait pour l’accès, ainsi que l’utilisation de l’instruction LOD (par exemple, [**tex2Dlod**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-tex2dlod)) qui retourne ce que représente le calcul du LOD matériel.

Une autre compliquation est que beaucoup d’accès seront sur les mêmes vignettes, si bien qu’un grand nombre d’enregistrements redondants se produira et éventuellement de contention de mémoire. Cela peut être pratique si le matériel peut avoir la possibilité de ne pas prendre en compte les accès de vignette s’ils ont été signalés ailleurs auparavant. L’état de ce suivi peut peut-être être réinitialisé à partir de l’API (probablement au niveau des limites de cadre).

## <a name="per-sample-minlod-clamp"></a>Clamp MinLOD par exemple

Pour aider les nuanceurs à éviter les zones dans les ressources en mosaïque mipmapped qui sont connues pour être non mappées, la plupart des instructions de nuanceur qui impliquent l’utilisation d’un échantillonneur (filtrage) ont un nouveau mode qui permet au nuanceur de passer un paramètre de pincement float32 MinLOD supplémentaire à l’échantillon de texture. Cette valeur se trouve dans l’espace de nombre mipmap de la vue, par opposition à la ressource sous-jacente.

Le matériel exécute [**Max**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-max)(FShaderMinLODClamp, fComputedLOD) à la même place dans le calcul LOD dans lequel la bride MinLOD par ressource se produit, ce qui est également un **nombre max**().

Si le résultat de l’application de la bride LOD par échantillon et de tout autre clamp LOD défini dans l’échantillonneur est un jeu vide, le résultat est le même que le résultat de l’accès hors limites en tant que bride minLOD par ressource : 0 pour les composants dans le format de surface et les valeurs par défaut pour les composants manquants.

L’instruction LOD (par exemple, [**tex2Dlod**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-tex2dlod)), qui met à jour la clamp minLOD par exemple décrite ici, retourne à la fois un LOD ancré et non ancré. Le LOD ancré renvoyé à partir de cette instruction LOD reflète tout le verrouillage, y compris la bride par ressource, mais pas une bride par échantillon. Par exemple, la bride est contrôlée et connue du nuanceur, de sorte que l’auteur du nuanceur peut appliquer manuellement cette bride à la valeur de retour de l’instruction LOD, si vous le souhaitez.

## <a name="minmax-reduction-filtering"></a>Filtrage de réduction min/max

Les applications peuvent choisir de gérer leurs propres structures de données qui les informent de ce à quoi ressemblent les mappages pour une ressource en mosaïque. Il peut s’agir, par exemple, d’une surface qui contient un Texel pour contenir des informations sur chaque vignette d’une ressource en mosaïque. Il est possible de stocker le premier LOD qui est mappé à un emplacement de mosaïque donné. En échantillonnant soigneusement cette structure de données de la même façon que la ressource en mosaïque est destinée à être échantillonnée, il est possible de découvrir ce que le LOD minimal qui est entièrement mappé pour un encombrement de filtre de texture entier est. Pour faciliter ce processus, Direct3D 11,2 introduit un nouveau mode d’échantillonnage à usage général, le filtrage min/max.

L’utilitaire de filtrage min/max pour le suivi LOD peut être utile à d’autres fins, telles que, peut-être le filtrage des surfaces de profondeur.

Le filtrage de réduction min/max est un mode sur les échantillonneurs qui extrait le même jeu de texels qu’un filtre de texture normal peut extraire. Mais au lieu de fusionner les valeurs pour produire une réponse, elle retourne la valeur min () ou Max () des texels extraits, en fonction du composant (par exemple, le minimum de toutes les valeurs R, séparément du nombre minimal de toutes les valeurs G, etc.).

Les opérations min/max suivent les règles de précision arithmétiques Direct3D. L’ordre des comparaisons n’a pas d’importance.

Pendant les opérations de filtre qui ne sont pas min/max, parfois, le poids d’une Texel donnée finit par 0,0. Par exemple, un échantillon linéaire avec des coordonnées de texture qui se trouvent directement sur un centre de Texel-3 autres éléments de Texel (dont ils sont susceptibles de varier en fonction du matériel) contribuent au filtre, mais avec un poids de 0. Pour l’un de ces texels, qui serait 0 poids sur un filtre non-min/max, si le filtre est min/max, ces texels ne contribuent toujours pas au résultat (et les poids n’affectent pas les opérations de filtre min/max).

La liste complète des modes de filtre est indiquée dans l’énumération de [**\_ filtre d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_filter) avec les valeurs minimale et maximale dans les valeurs d’énumération.

La prise en charge de cette fonctionnalité dépend de la prise en charge de [niveau 2](tier-2.md) pour les ressources en mosaïque.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accès du pipeline aux ressources en mosaïque](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 
---
title: Niveau 1
description: Cette section décrit la prise en charge de niveau 1.
ms.assetid: 8E2907D2-EFCB-4F97-9B40-6835A65D3DE5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4111fa48dafa7f38a26d5ca09f95898eacef6f55
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918551"
---
# <a name="tier-1"></a>Niveau 1

Cette section décrit la prise en charge de niveau 1.

-   Matériel au niveau de la fonctionnalité 11,0 minimum.
-   Aucune prise en charge de la surface.
-   Aucune prise en charge de Texture1D ou Texture3D.
-   Aucun exemple de prise en charge de l’anticrénelage (MSAA) à 2, 8 ou 16. Seul 4x est requis, à l’exception des formats 128 BPP.
-   Aucun modèle de Swizzle standard (la disposition dans les mosaïques de 64 Ko et la compression MIP tail est à la disposition du fabricant du matériel).
-   Limitations sur la façon dont les vignettes sont accessibles lorsqu’il existe des mappages en double, décrits dans [limitations d’accès aux vignettes avec des mappages dupliqués](tile-access-limitations-with-duplicate-mappings-.md).

### <a name="limitations-affecting-tier-1-only"></a>Limitations affectant uniquement le niveau 1

-   Les ressources en mosaïque peuvent avoir des mappages **null** , mais leur lecture ou leur écriture génère des résultats indéfinis, y compris les appareils supprimés. Les applications peuvent contourner ce risque en mappant une page factice unique à toutes les zones vides. Soyez prudent si vous écrivez et rendez sur une page mappée à plusieurs emplacements cibles de rendu, car l’ordre des écritures n’est pas défini.
-   Les instructions du nuanceur pour le déverrouillage du LOD et les commentaires d’État mappés ne sont pas disponibles. Pour plus d’informations, consultez [exposition des ressources en mosaïque HLSL](hlsl-tiled-resources-exposure.md).
-   Contraintes d’alignement pour les formes de mosaïques standard : il est garanti uniquement que les MIPS (à partir du plus fins) dont les dimensions sont tous des multiples de la taille de mosaïque standard prennent en charge les formes de mosaïque standard et peuvent avoir des vignettes individuelles mappées/non mappées arbitrairement. Le premier mipmap dans une ressource en mosaïque qui a une dimension qui n’est pas un multiple de la taille de la mosaïque standard, ainsi que toutes les des mipmaps plus grossières, peut avoir une forme de mosaïque non standard, qui se raccorde à N 64 en mosaïques pour cet ensemble de mips à la fois (N signalé à l’application). Ces vignettes N sont considérées comme une seule unité, qui doit être entièrement mappée ou entièrement démappée par l’application à un moment donné, bien que les mappages de chacune des vignettes puissent se trouver dans des emplacements de jointure arbitraire dans un pool de mosaïques.
-   Les ressources en mosaïque avec des des mipmaps non pas un multiple de taille de mosaïque standard dans toutes les dimensions ne sont pas autorisées à avoir une taille de tableau supérieure à 1.
-   Pour basculer entre les vignettes de référencement dans un pool de mosaïques via une ressource de [mémoire tampon](overviews-direct3d-11-resources-buffers.md) pour référencer les mêmes vignettes via une ressource de [texture](overviews-direct3d-11-resources-textures.md) , ou vice-versa, l’appel le plus récent à [**UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) ou [**CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) qui définit les mappages à ces vignettes de pool de mosaïques doit être pour la même dimension de ressource (tampon et texture \* ) que la dimension Dans le cas contraire, le comportement n’est pas défini, y compris le risque de réinitialisation de l’appareil. Ainsi, par exemple, appeler **UpdateTileMappings** pour définir des mappages de vignettes pour une mémoire tampon, puis **UpdateTileMappings** aux mêmes vignettes dans le pool de mosaïques via une ressource [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) , alors l’accès aux vignettes via la mémoire tampon n’est pas valide. Les opérations de contournement sont la redéfinition des mappages de vignettes pour une ressource lors du basculement entre la mémoire tampon et la texture (ou vice versa) partageant des vignettes ou simplement jamais de partager des vignettes dans un pool de mosaïques entre les ressources de mémoire tampon et les ressources de texture.
-   Le filtrage de réduction min/max n’est pas pris en charge. Pour plus d’informations sur le filtrage de réduction min/max, consultez [fonctionnalités d’échantillonnage de texture des ressources en mosaïque](tiled-resources-texture-sampling-features.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Niveaux de fonctionnalités des ressources en mosaïque](tiled-resources-features-tiers.md)
</dt> </dl>

 

 
---
title: Restrictions d’accès aux vignettes avec des mappages en double
description: Cette section décrit les limitations d’accès aux vignettes avec des mappages en double.
ms.assetid: 7A498E0D-9151-4A89-B7C3-C4F476457D17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0909b0d10e286e5f774f6893b692abdeb19d3ef7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028732"
---
# <a name="tile-access-limitations-with-duplicate-mappings"></a>Restrictions d’accès aux vignettes avec des mappages en double

Cette section décrit les limitations d’accès aux vignettes avec des mappages en double.

## <a name="copying-tiled-resources-with-overlapping-source-and-destination"></a>Copie de ressources en mosaïque avec la source et la destination qui se chevauchent

Si les vignettes de la zone source et de destination d’une opération de copie \* ont des mappages dupliqués dans la zone de copie qui auraient été chevauchés même si les deux ressources n’étaient pas des ressources en mosaïque et que l’opération de copie \* prend en charge les copies qui se chevauchent, l’opération de copie \* se comportera comme si la source était copiée dans un emplacement temporaire avant Toutefois, si le chevauchement n’est pas évident (comme les ressources source et de destination diffèrent, mais que les mappages de partage ou les mappages sont dupliqués sur une surface donnée), les résultats de l’opération de copie sur les vignettes partagées ne sont pas définis.

## <a name="copying-to-tiled-resource-with-duplicated-tiles-in-destination-area"></a>Copie vers une ressource en mosaïque avec des vignettes dupliquées dans la zone de destination

La copie vers une ressource en mosaïque avec des vignettes en double dans la zone de destination produit des résultats non définis dans ces vignettes, sauf si les données elles-mêmes sont identiques ; différentes vignettes peuvent écrire les vignettes dans des ordres différents.

## <a name="uav-accesses-to-duplicate-tiles-mappings"></a>UAV accède aux mappages de vignettes dupliquées

Supposons qu’une vue d’accès non ordonnée (UAV) sur une ressource en mosaïque possède des mappages de vignettes en double dans sa zone ou avec d’autres ressources liées au pipeline. Le classement des accès à ces vignettes dupliquées n’est pas défini si elle est effectuée par différents threads, tout comme n’importe quel ordre d’accès mémoire à UAVs en général n’est pas ordonné.

## <a name="rendering-after-tile-mapping-changes-or-content-updates-from-outside-mappings"></a>Rendu après modification du mappage des vignettes ou mises à jour du contenu à partir des mappages externes

Si les mappages de vignette d’une ressource en mosaïque ont changé ou que le contenu des vignettes de pool en mosaïque mappées a été modifié par le biais de mappages d’une autre ressource en mosaïque, et la ressource en mosaïque va être rendue via la vue de la cible de rendu ou la vue du stencil de profondeur, l’application doit effacer (à l’aide des API de suppression de fonction fixe) ou copier entièrement à l’aide des API de copie \* /Update \* les vignettes qui ont changé dans la zone rendue (mappée ou non). Si une application ne peut pas être effacée ou copiée dans ces cas de figure, les structures d’optimisation matérielle de la vue de cible de rendu donnée ou de la vue du stencil de profondeur sont obsolètes, ce qui entraîne un rendu du garbage collector sur un matériel et une incohérence sur différents matériels. Ces structures de données d’optimisation masquées utilisées par le matériel peuvent être locales à des mappages individuels et ne pas être visibles par d’autres mappages dans la même mémoire.

L’opération [**ID3D11DeviceContext1 :: Clearview**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-clearview) prend en charge l’effacement des vues de cible de rendu avec des rectangles. Pour le matériel qui prend en charge les ressources en mosaïque, **Clearview** doit également prendre en charge l’effacement des vues de stencil de profondeur avec des rectangles, pour des surfaces de profondeur uniquement (sans stencil). Cette opération permet aux applications d’effacer uniquement la zone nécessaire d’une surface.

Si une application doit conserver le contenu existant de la mémoire des zones d’une ressource en mosaïque dans laquelle les mappages ont changé, cette application doit contourner l’exigence évidente. L’application peut effectuer cette opération en enregistrant d’abord le contenu dans lequel les mappages de vignettes ont changé (en les copiant sur une surface temporaire, par exemple, à l’aide de [**ID3D11DeviceContext2 :: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles)), en émettant la commande Clear requise, puis en recopiant le contenu. Bien que cela accomplisse la tâche de préservation du contenu de surface pour le rendu incrémentiel, l’inconvénient est que les performances de rendu suivantes sur la surface peuvent être affectées, car les optimisations de rendu peuvent être perdues.

Si une vignette est mappée en plusieurs ressources en mosaïque en même temps et que le contenu de la mosaïque est manipulé par quelque moyen que ce soit (rendu, copie, etc.) via l’une des ressources en mosaïque, si la même vignette doit être restituée par le biais d’une autre ressource en mosaïque, la vignette doit être effacée en premier, comme décrit précédemment.

## <a name="rendering-to-tiles-shared-outside-render-area"></a>Rendu sur des vignettes partagées en dehors de la zone de rendu

Supposons qu’une zone d’une ressource en mosaïque soit rendue et que les vignettes du pool de mosaïques référencées par la zone de rendu soient également mappées à depuis l’extérieur de la zone de rendu (y compris via d’autres ressources en mosaïque, en même temps ou non). Il n’est pas garanti que les données rendues à ces vignettes s’affichent correctement quand elles sont consultées via les autres mappages, même si la disposition de mémoire sous-jacente est compatible. Ce fait est dû à des structures de données d’optimisation qui peuvent être utilisées en local pour les mappages individuels des surfaces pouvant être rendues et non visibles par d’autres mappages vers le même emplacement de mémoire. Vous pouvez contourner cette restriction en copiant le mappage rendu à tous les autres mappages dans la même mémoire que celle qui est accessible (ou en effaçant cette mémoire ou en copiant d’autres données vers celle-ci si l’ancien contenu n’est plus nécessaire). Bien que cette solution semble redondante, elle permet à tous les autres mappages de la même mémoire de comprendre correctement comment accéder à son contenu, et au moins l’économie de mémoire qui consiste à avoir une seule sauvegarde de mémoire physique reste intacte. En outre, lorsque vous basculez entre l’utilisation de différentes ressources en mosaïque qui partagent des mappages (sauf lecture uniquement), vous devez appeler l’API [**ID3D11DeviceContext2 :: TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) dans entre les commutateurs.

## <a name="rendering-to-tiles-shared-within-render-area"></a>Rendu des vignettes partagées dans la zone de rendu

Si une zone d’une ressource en mosaïque est rendue dans et dans la zone de rendu, plusieurs mosaïques sont mappées au même emplacement du pool de mosaïques, les résultats de rendu ne sont pas définis sur ces vignettes.

## <a name="data-compatibility-across-tiled-resources-sharing-tiles"></a>Compatibilité des données sur des ressources en mosaïque partageant des vignettes

Supposons que plusieurs ressources en mosaïque ont des mappages aux mêmes emplacements de pool de mosaïques et que chaque ressource est utilisée pour accéder aux mêmes données. Ce scénario n’est valide que si les autres règles relatives à l’évitement des problèmes avec les structures d’optimisation matérielle sont évitées, les appels appropriés à [**ID3D11DeviceContext2 :: TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) sont effectués et les ressources en mosaïque sont compatibles les unes avec les autres. Ce dernier est décrit ici en ce qui concerne les ressources en mosaïque partageant des vignettes pour être incompatibles. Les conditions d’incompatibilité d’accès aux mêmes données sur les mappages de vignettes dupliquées sont l’utilisation de différentes dimensions ou de différents formats de surface, ou de différences en présence d’indicateurs de liaison de cible de rendu ou de stencil de profondeur sur les ressources. L’écriture dans la mémoire avec un type de mappage produit des résultats non définis si, par la suite, vous lisez ou effectuez le rendu via un mappage à partir d’une ressource incompatible. Si les autres mappages de partage de ressources sont d’abord initialisés avec de nouvelles données (en recyclant la mémoire à un autre usage), l’opération de lecture ou de rendu suivante est correcte, car les données ne sont pas réparties sur les interprétations non compatibles. Toutefois, vous devez appeler l’API **TiledResourceBarrier** quand vous basculez entre l’accès aux mappages non compatibles comme celui-ci.

Si l’indicateur de liaison de la cible de rendu ou du stencil de profondeur n’est défini sur aucune des ressources partageant les mappages entre eux, il y a beaucoup moins de restrictions. Tant que les types de format et de surface (par exemple, Texture2D) sont identiques, les vignettes peuvent être partagées. Les différents formats compatibles sont des cas tels que \* les surfaces BC et la taille équivalente non compressée 32 bits ou 16 bits par composant, comme BC6H et R32G32B32A32. Un grand nombre de formats de 32 bits par élément peuvent également être associés à R32 \_ \* (R10G10B10A2 \_ \* , R8G8B8A8 \_ \* , B8G8R8A8 \_ \* , B8G8R8X8 \_ \* , R16G16 \_ \* ); cette opération a toujours été autorisée pour les ressources qui ne sont pas en mosaïque.

Le partage entre les vignettes compressées et non compressées est parfait si les formats sont compatibles et les vignettes sont remplies avec une couleur unie.

Enfin, si rien n’est courant concernant les ressources partageant les mappages de vignette, sauf qu’aucun n’a de cibles de rendu ou d’indicateurs de liaison de stencil de profondeur, seule la mémoire remplie avec 0 peut être partagée en toute sécurité ; le mappage apparaît comme un décodage de 0 pour la définition du format de ressource donné (en général, il s’agit simplement de 0).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accès du pipeline aux ressources en mosaïque](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 





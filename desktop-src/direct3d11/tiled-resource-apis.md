---
title: API de ressources en mosaïque
description: Les API décrites dans cette section fonctionnent avec les ressources en mosaïque et le pool de mosaïques.
ms.assetid: 02DCF9BA-F9EA-4176-AD6F-AA620CE968BA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0d97f5272f4f96db56e6e89b871951de035105
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379664"
---
# <a name="tiled-resource-apis"></a>API de ressources en mosaïque

Les API décrites dans cette section fonctionnent avec les ressources en mosaïque et le pool de mosaïques.

-   [Affectation de vignettes à partir d’un pool de mosaïques à une ressource](#assigning-tiles-from-a-tile-pool-to-a-resource)
-   [Interrogation de la mosaïque et du support des ressources](#querying-resource-tiling-and-support)
-   [Copie de données en mosaïque](#copying-tiled-data)
-   [Redimensionnement du pool de mosaïques](#resizing-tile-pool)
-   [Barrière des ressources en mosaïque](#tiled-resource-barrier)
-   [Rubriques connexes](#related-topics)

## <a name="assigning-tiles-from-a-tile-pool-to-a-resource"></a>Affectation de vignettes à partir d’un pool de mosaïques à une ressource

Les API [**ID3D11DeviceContext2 :: UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) et [**ID3D11DeviceContext2 :: CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) manipulent et interrogent les mappages de vignettes. Les appels de mise à jour affectent uniquement les vignettes identifiées dans l’appel, tandis que d’autres sont laissés comme défini précédemment.

Toute vignette donnée à partir d’un pool de mosaïques peut être mappée à plusieurs emplacements dans une ressource, voire à plusieurs ressources. Ce mappage comprend des vignettes dans une ressource qui ont une mise en page choisie par l’implémentation ([compression mipmap](mipmap-packing.md)) où plusieurs des mipmaps sont regroupés dans une seule vignette. Le résultat est que si les données sont écrites dans la vignette via un mappage, mais lues via un mappage configuré différemment, les résultats ne sont pas définis. Une utilisation soigneuse de cette flexibilité peut toujours être utile pour une application, comme le partage d’une vignette entre des ressources qui ne seront pas utilisées simultanément, où le contenu de la vignette est toujours initialisé par le même mappage de ressources, car il sera lu par la suite. De même, une vignette mappée pour contenir les des mipmaps compressés de plusieurs ressources différentes avec les mêmes dimensions de surface fonctionnera correctement. les données apparaîtront de la même façon dans les deux mappages.

Les modifications apportées aux affectations de vignettes pour une ressource peuvent être effectuées à tout moment dans un contexte immédiat ou différé.

## <a name="querying-resource-tiling-and-support"></a>Interrogation de la mosaïque et du support des ressources

Pour interroger la mosaïque des ressources, utilisez [**ID3D11Device2 :: GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling).

Pour la prise en charge de la mosaïque des ressources, utilisez [**ID3D11Device2 :: CheckMultisampleQualityLevels1**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-checkmultisamplequalitylevels1).

## <a name="copying-tiled-data"></a>Copie de données en mosaïque

Toutes les méthodes dans Direct3D pour déplacer des données autour du travail avec des ressources en mosaïque comme si elles n’étaient pas en mosaïque, à l’exception du fait que les écritures dans les zones non mappées sont supprimées et que les lectures des zones non mappées produisent 0. Si une opération de copie implique l’écriture à plusieurs reprises dans le même emplacement de mémoire, car plusieurs emplacements de la ressource de destination sont mappés à la même mémoire de vignettes, les écritures obtenues dans les vignettes multimappées sont non déterministes et non reproductibles. Autrement dit, les accès se produisent dans le même ordre que celui où se trouve le matériel pour exécuter la copie.

Direct3D 11,2 introduit des méthodes pour ces méthodes supplémentaires pour copier :

-   Copie entre les vignettes d’une ressource en mosaïque (avec une granularité de mosaïque de 64 Ko) et (vers/à partir de) une mémoire tampon dans la mémoire de l’unité de traitement graphique (GPU) (ou ressource intermédiaire)- [ **ID3D11DeviceContext2 :: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles)
-   Copier à partir de la mémoire fournie par l’application vers des vignettes dans une ressource en mosaïque- [ **ID3D11DeviceContext2 :: UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)

Ces méthodes Swizzle/deswizzle en fonction des besoins, et permettent à une vignette de D3D11 de \_ \_ copier \_ aucun \_ indicateur de remplacement lorsque l’appelant promet la mémoire de destination n’est pas référencée par le travail GPU qui est en vol.

Les vignettes impliquées dans la copie ne peuvent pas inclure des vignettes qui contiennent des des mipmaps compressés ou qui ont des résultats qui ne sont pas définis. Pour transférer des données vers/à partir de des mipmaps que les packages matériels dans une vignette, vous devez utiliser les API de copie/mise à jour standard (non spécifiques à une mosaïque) ou [**ID3D11DeviceContext :: GenerateMips**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-generatemips) pour l’ensemble de la chaîne MIP.

**Remarque sur [**GenerateMips**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-generatemips):** l’utilisation de [**ID3D11DeviceContext :: GenerateMips**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-generatemips) sur une ressource avec des vignettes partiellement mappées produit des résultats qui suivent simplement les règles de lecture et d’écriture de la **valeur null** appliquée à l’algorithme que le matériel et le pilote d’affichage sont utilisés pour **GenerateMips**. Par conséquent, il n’est pas particulièrement utile pour une application de procéder à cette opération, sauf si les zones avec des mappages **null** (et leur effet sur d’autres mips pendant la phase de génération) n’ont aucune conséquence sur les parties de la surface qui intéressent l’application.

La copie de données de vignette à partir d’une surface intermédiaire ou de la mémoire de l’application est le moyen de charger des vignettes qui ont pu être diffusées en continu, par exemple. Une variation lors de la diffusion en continu sur le disque consiste à charger un certain type de données compressées dans la mémoire GPU, puis à décoder sur le GPU. La cible Decode peut être une ressource de mémoire tampon dans la mémoire du GPU, à partir de laquelle [**CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) est ensuite copiée dans la ressource en mosaïque réelle. Cette étape de copie permet au GPU de Swizzle lorsque le modèle Swizzle n’est pas connu. Swizzling n’est pas nécessaire si la ressource en mosaïque elle-même est une ressource tampon (par exemple, par opposition à une texture).

La disposition de la mémoire des vignettes dans le côté ressource de mémoire tampon non en mosaïque de la copie est simplement linéaire en mémoire dans les mosaïques de 64 Ko, que le pilote matériel et le pilote d’affichage Swizzle/deswizzle par vignette, le cas échéant, lors du transfert vers/à partir d’une ressource en mosaïque. Pour les surfaces MSAA (multiéchantillonner l’anticrénelage), chaque échantillon de pixel est parcouru dans un exemple d’ordre d’index avant de passer au pixel suivant. Pour les vignettes qui sont partiellement remplies sur le côté droit (pour une surface dont la largeur n’est pas un multiple de la largeur de la mosaïque en pixels), le tangage/Stride pour descendre dans une ligne correspond à la taille totale, en octets, du nombre de pixels qui correspondrait à la vignette si la vignette était pleine. Par conséquent, il peut y avoir un intervalle entre chaque ligne de pixels en mémoire. Pour simplifier la spécification, les des mipmaps plus petits qu’une vignette ne sont pas regroupés dans la disposition linéaire. Cela semble être un gaspillage de l’espace mémoire, mais comme indiqué lors de la copie vers des mips, les packs matériels ne sont pas autorisés via [**CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) ou [**UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles). L’application peut simplement utiliser \* des API UpdateSubresource () ou CopySubresource () génériques \* pour copier des petits mips individuellement, bien que dans le cas de CopySubresource \* (), cela signifie que la mémoire linéaire doit être la même dimension que la ressource en mosaïque-CopySubresource \* () ne peut pas copier à partir d’une ressource de mémoire tampon vers une Texture2D par exemple.

Si un Swizzle matériel standard est défini, des indicateurs peuvent être ajoutés pour indiquer que les données de la mémoire tampon doivent être interprétées dans ce format (pas d’Swizzle nécessaire lors du transfert), bien que d’autres approches de chargement des données peuvent également être utiles dans ce cas, par exemple autoriser les applications à accéder directement à la mémoire du pool de mosaïques.

Les opérations de copie peuvent être effectuées sur un contexte immédiat ou différé.

## <a name="resizing-tile-pool"></a>Redimensionnement du pool de mosaïques

Pour redimensionner un pool de mosaïques, utilisez [**ID3D11DeviceContext2 :: ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool).

## <a name="tiled-resource-barrier"></a>Barrière des ressources en mosaïque

Pour spécifier une contrainte de classement d’accès aux données entre plusieurs ressources en mosaïque, utilisez [**ID3D11DeviceContext2 :: TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ressources en mosaïque](tiled-resources.md)
</dt> </dl>

 

 





---
title: Sous-ressources (Direct3D 12 Graphics)
description: Décrit comment une ressource est divisée en sous-ressources et comment référencer une seule, plusieurs ou plusieurs sous-ressources.
ms.assetid: C4F92F8A-DBF0-412B-8707-CC4C1BF2D88F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8fa8ea0d48fea7ee8e192d9dcf1fe5e3d22423
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104548552"
---
# <a name="subresources-direct3d-12-graphics"></a>Sous-ressources (Direct3D 12 Graphics)

Décrit comment une ressource est divisée en sous-ressources et comment référencer une seule, plusieurs ou plusieurs sous-ressources.

-   [Exemples de sous-ressources](#example-subresources)
    -   [Indexation des sous-ressources](#subresource-indexing)
    -   [Tranche MIP](#mip-slice)
    -   [Tranche de tableau](#array-slice)
    -   [Tranche plan](#plane-slice)
    -   [Sous-ressources multiples](#multiple-subresources)
-   [API de sous-ressource](#subresource-apis)
-   [Rubriques connexes](#related-topics)

## <a name="example-subresources"></a>Exemples de sous-ressources

Si une ressource contient une mémoire tampon, elle contient simplement une sous-ressource avec un index de 0. Si la ressource contient une texture (ou un tableau de textures), le référencement des sous-ressources est plus complexe.

Certaines API accèdent à une ressource entière (telle que la méthode [**ID3D12GraphicsCommandList :: CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource) ), d’autres accèdent à une partie d’une ressource (par exemple, la méthode [**ID3D12Resource :: ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) ). Les méthodes qui accèdent à une partie d’une ressource utilisent généralement une description de la vue (telle que la structure [**\_ SRV du \_ tableau \_ D3D12 TEX2D**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv) ) pour spécifier les sous-ressources auxquelles accéder. Reportez-vous à la section API des sous- [ressources](#subresource-apis) pour obtenir une liste complète.

### <a name="subresource-indexing"></a>Indexation des sous-ressources

Pour indexer une sous-ressource particulière, les niveaux MIP sont indexés en premier lorsque chaque entrée de tableau est indexée.

![indexation des sous-ressources](images/subresource-index.png)

### <a name="mip-slice"></a>Tranche MIP

Une tranche MIP comprend un niveau de mipmap pour chaque texture d’un tableau, comme illustré dans l’image suivante.

![tranches MIP de sous-ressources](images/subresource-mip-slice.png)

### <a name="array-slice"></a>Tranche de tableau

À partir d’un tableau de textures, chaque texture avec des mipmaps, une tranche de tableau comprend une texture et tous ses niveaux MIP, comme illustré dans l’image suivante.

![tranches de groupe de sous-ressources](images/subresource-array-slices.png)

### <a name="plane-slice"></a>Tranche plan

En général, les formats planaires ne sont pas utilisés pour stocker les données RVBA, mais dans les cas où il s’agit (par exemple, des données RGB 24bpp), un plan peut représenter l’image rouge, l’image verte et l’image bleue. Toutefois, un plan n’est pas nécessairement une couleur, deux couleurs ou plus peuvent être combinées dans un plan. Plus généralement, les données planaires sont utilisées pour les données de Depth-Stencil et YCbCr sous-échantillonnées. Depth-Stencil est le seul format qui prend entièrement en charge les des mipmaps, les tableaux et les plans multiples (souvent le plan 0 pour la profondeur et le plan 1 du stencil).

L’indexation des sous-ressources pour un tableau de deux images Depth-Stencil, chacune avec trois niveaux MIP, est illustrée ci-dessous.

![indexation du stencil de profondeur](images/depth-stencil-indexing.png)

Le sous-échantillon YCbCr prend en charge les tableaux et contient des plans, mais ne prend pas en charge des mipmaps. Les images YCbCr ont deux plans, l’un pour la luminance (Y), dont l’oeil humain est le plus sensible, et l’autre pour la chrominance (à la fois CB et CR, entrelacé) qui est moins sensible à l’oeil humain. Ce format permet la compression des valeurs de chrominance afin de compresser une image sans affecter la luminance, et est un format de compression vidéo courant pour cette raison, bien qu’elle soit utilisée pour compresser des images fixes. L’image ci-dessous montre le format NV12, en notant que la chrominance a été compressée à un quart de la résolution de la luminance, ce qui signifie que la largeur de chaque plan est identique et que le plan de chrominance correspond à la moitié de la hauteur du plan de luminance. Les plans sont indexés en tant que sous-ressources de manière identique à l’exemple de Depth-Stencil ci-dessus.

![format nv12](images/ycbcr.png)

Les formats planaires existaient dans Direct3D 11, mais les plans individuels n’ont pas pu être traités individuellement, par exemple pour les opérations de copie ou de mappage. Cela a été modifié dans Direct3D 12 afin que chaque plan ait reçu son propre ID de sous-ressource. Comparez les deux méthodes suivantes pour calculer l’ID de sous-ressource.

Direct3D 11

``` syntax
inline UINT D3D11CalcSubresource( UINT MipSlice, UINT ArraySlice, UINT MipLevels )
{
    return MipSlice + (ArraySlice * MipLevels); 
}
```

Direct3D 12

``` syntax
inline UINT D3D12CalcSubresource( UINT MipSlice, UINT ArraySlice, UINT PlaneSlice, UINT MipLevels, UINT ArraySize )
{ 
    return MipSlice + (ArraySlice * MipLevels) + (PlaneSlice * MipLevels * ArraySize); 
}
```

La plupart du matériel suppose que la mémoire pour le plan N est toujours allouée immédiatement après le plan N-1.

Une alternative à l’utilisation de sous-ressources est qu’une application peut allouer une ressource complètement distincte par plan. Dans ce cas, l’application comprend les données planes et utilise plusieurs ressources pour les représenter.

### <a name="multiple-subresources"></a>Sous-ressources multiples

Un affichage des ressources de nuanceur peut sélectionner n’importe quelle zone rectangulaire de sous-ressources, à l’aide de l’une des tranches décrites ci-dessus et de l’utilisation judicieuse des champs dans les structures de vue (par exemple, [**D3D12 \_ TEX2D \_ array \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)), comme indiqué dans l’image.

![sélection de plusieurs sous-ressources](images/subresource-multiple.png)

Une vue de cible de rendu ne peut utiliser qu’une seule sous-ressource ou une seule tranche MIP et ne peut pas inclure de sous-ressources de plus d’une tranche MIP. Autrement dit, chaque texture dans une vue de cible de rendu doit avoir la même taille. Un affichage des ressources de nuanceur peut sélectionner n’importe quelle zone rectangulaire de sous-ressources, comme illustré dans l’image.

## <a name="subresource-apis"></a>API de sous-ressource

Les API suivantes référencent et utilisent des sous-ressources :

Énumérations :

-   [**\_Type de \_ copie de texture D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)

Les structures suivantes contiennent des index *PlaneSlice* , la plupart contiennent des index *MipSlice* .

-   [**D3D12 \_ TEX2D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_rtv)
-   [**D3D12 \_ \_ tableau TEX2D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [**D3D12 \_ TEX2D \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_srv)
-   [**\_SRV du \_ tableau D3D12 TEX2D \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [**D3D12 \_ TEX2D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_uav)
-   [**D3D12 \_ TEX2D \_ array \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

Les structures suivantes contiennent des index *ArraySlice* , la plupart contiennent des index *MipSlice* .

-   [**\_DSV D3D12 TEX1D \_ array \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv)
-   [**\_DSV D3D12 TEX2D \_ array \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv)
-   [**\_DSV D3D12 TEX2DMS \_ array \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv)
-   [**D3D12 \_ \_ tableau TEX1D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv)
-   [**D3D12 \_ \_ tableau TEX2D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [**D3D12 \_ \_ tableau TEX2DMS \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv)
-   [**\_SRV du \_ tableau D3D12 TEX1D \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv)
-   [**\_SRV du \_ tableau D3D12 TEX2D \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [**\_SRV du \_ tableau D3D12 TEX2DMS \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv)
-   [**D3D12 \_ TEX1D \_ array \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav)
-   [**D3D12 \_ TEX2D \_ array \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

Les structures suivantes contiennent des index *MipSlice* , mais ni des index *ArraySlice* , ni des index *PlaneSlice* .

-   [**D3D12 \_ TEX1D \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_dsv)
-   [**D3D12 \_ TEX2D \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_dsv)
-   [**D3D12 \_ TEX1D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_rtv)
-   [**D3D12 \_ TEX3D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_rtv)
-   [**D3D12 \_ TEX1D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_uav)
-   [**D3D12 \_ TEX3D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_uav)

Les structures suivantes référencent également des sous-ressources :

-   [**D3D12 \_ IGNORER la \_ région**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) : structure utilisée pour la préparation de l’abandon d’une ressource.
-   [**D3D12 \_ \_ \_ Encombrement**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) des sous-ressources placé : ajoute un décalage dans une ressource à l’encombrement de base.
-   [**D3D12 \_ \_ \_ Barrière de transition de ressource**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) : décrit la transition des sous-ressources entre différentes utilisations (ressource de nuanceur, cible de rendu, etc.).
-   [**D3D12 \_ \_Données**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) des sous-ressources : les données des sous-ressources incluent les données elles-mêmes, ainsi que la largeur des lignes et des secteurs.
-   [**D3D12 \_ \_Encombrement**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) des sous-ressources : un encombrement comprend le format, la largeur, la hauteur, la profondeur et l’espacement des lignes de la sous-ressource.
-   [**D3D12 \_ \_Informations sur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_info) les sous-ressources : contient le décalage, la largeur des lignes et le pas de profondeur de la sous-ressource.
-   [**D3D12 \_ \_Mosaïque**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) de sous-ressources : décrit un volume de sous-ressources en mosaïque (reportez-vous à [ressources en mosaïque de volume](volume-tiled-resources.md)).
-   [**D3D12 \_ \_ \_ Emplacement de copie de texture**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) : décrit une partie d’une texture à des fins de copie.
-   [**D3D12 \_ \_ \_ Coordonnée des ressources en mosaïque**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : décrit les coordonnées d’une ressource en mosaïque.

Méthodes :

-   [**ID3D12Device :: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints) : obtient des informations sur une ressource pour permettre l’établissement d’une copie.
-   [**ID3D12Device :: GetResourceTiling**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : obtient des informations sur la façon dont une ressource en mosaïque est divisée en mosaïques.
-   [**ID3D12GraphicsCommandList :: ResolveSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource) : copie une sous-ressource échantillonnée sur plusieurs sous-ressources échantillonnées.
-   [**ID3D12Resource :: Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) : retourne un pointeur vers les données spécifiées dans la ressource et refuse l’accès au GPU à la sous-ressource.
-   [**ID3D12Resource :: ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) : copie les données d’une sous-ressource, ou une zone rectangulaire d’une sous-ressource.
-   [**ID3D12Resource :: DEMAPPAGE**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) : annule la correspondance de la plage de mémoire spécifiée et invalide le pointeur vers la ressource. Rétablit l’accès GPU à la sous-ressource.
-   [**ID3D12Resource :: WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) : copie des données vers une sous-ressource, ou une zone rectangulaire d’une sous-ressource.

Les textures doivent être dans l’État commun de l’état de la [**\_ ressource \_ \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) pour que l’accès au processeur via [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) et [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) soit légal, mais ce n’est pas le cas des tampons. L’accès de l’UC à une ressource est généralement effectué par le biais de [**mappages de mappage**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) / [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Liaison de ressource](resource-binding.md)
</dt> </dl>

 

 





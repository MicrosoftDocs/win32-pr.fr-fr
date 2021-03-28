---
title: Sous-ressources (graphiques Direct3D 11)
description: Cette rubrique décrit les sous-ressources de texture ou des parties d’une ressource.
ms.assetid: 57444cb5-6c8b-4dac-8d6b-ca2b45eafac9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a432dbfbcbf08c4359ea436a3e8fa025c801d12
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032160"
---
# <a name="subresources-direct3d-11-graphics"></a>Sous-ressources (graphiques Direct3D 11)

Cette rubrique décrit les sous-ressources de texture ou des parties d’une ressource.

Direct3D peut faire référence à une ressource entière ou référencer des sous-ensembles d’une ressource. Le terme sous-ressource fait référence à un sous-ensemble d’une ressource.

Une mémoire tampon est définie en tant que sous-ressource unique. Les textures sont un peu plus compliquées, car il existe plusieurs types de textures (1D, 2D, etc.) qui prennent en charge des niveaux de mipmap et/ou des tableaux de texture. En commençant par le cas le plus simple, une texture 1D est définie en tant que sous-ressource unique, comme le montre l’illustration suivante.

![illustration d’une texture 1D](images/d3d10-1d-texture.png)

Cela signifie que le tableau de texels qui composent une texture 1D est contenu dans une seule sous-ressource.

Si vous développez une texture 1D avec trois niveaux de mipmap, elle peut être visualisée comme dans l’illustration suivante.

![illustration d’une texture 1D avec trois niveaux de mipmap](images/d3d10-resource-texture1d.png)

Imaginez qu’il s’agit d’une texture unique composée de trois sous-ressources. Une sous-ressource peut être indexée à l’aide du niveau de détail (LOD) pour une seule texture. Lors de l’utilisation d’un tableau de textures, l’accès à une sous-ressource particulière nécessite à la fois le LOD et la texture particulière. L’API combine ces deux informations dans un seul index de sous-ressources de base zéro, comme indiqué dans l’illustration suivante.

![illustration d’un index de sous-ressources de base zéro](images/d3d10-resource-texture1darray-sub-indexing.png)

## <a name="selecting-subresources"></a>Sélection de sous-ressources

Certaines API accèdent à une ressource entière (par exemple, la méthode [**ID3D11DeviceContext :: CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) ), d’autres accèdent à une partie d’une ressource (par exemple, la méthode [**ID3D11DeviceContext :: UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) ou la méthode [**ID3D11DeviceContext :: CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) ). Les méthodes qui accèdent à une partie d’une ressource utilisent généralement une description de la vue (telle que la structure [**\_ \_ \_ DSV d3d11 TEX2D Array**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_dsv) ) pour spécifier les sous-ressources auxquelles accéder.

Les illustrations des sections suivantes montrent les termes utilisés par une description de la vue lors de l’accès à un tableau de textures.

### <a name="array-slice"></a>Tranche de tableau

À partir d’un tableau de textures, chaque texture avec des mipmaps, une *tranche de tableau* (représentée par le rectangle blanc) comprend une texture et toutes ses sous-ressources, comme le montre l’illustration suivante.

![illustration d’une tranche de tableau](images/d3d10-resource-array-slice.png)

### <a name="mip-slice"></a>Tranche MIP

Une *tranche MIP* (représentée par le rectangle blanc) comprend un niveau de mipmap pour chaque texture d’un tableau, comme indiqué dans l’illustration suivante.

![illustration d’une tranche MIP](images/d3d10-resource-mip-slice.png)

### <a name="selecting-a-single-subresource"></a>Sélection d’une seule sous-ressource

Vous pouvez utiliser ces deux types de tranches pour choisir une seule sous-ressource, comme indiqué dans l’illustration suivante.

![illustration du choix d’une sous-ressource à l’aide d’un segment de tableau et d’une tranche MIP](images/d3d10-resource-subresources-1.png)

### <a name="selecting-multiple-subresources"></a>Sélection de plusieurs sous-ressources

Vous pouvez aussi utiliser ces deux types de tranches avec le nombre de niveaux de mipmap et/ou le nombre de textures, pour choisir plusieurs sous-ressources, comme indiqué dans l’illustration suivante.

![illustration du choix de plusieurs sous-ressources](images/d3d10-resource-subresources-2.png)

> [!Note]  
> Une [**vue de cible de rendu**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_render_target_view_desc) ne peut utiliser qu’une seule sous-ressource ou une seule tranche MIP et ne peut pas inclure de sous-ressources de plus d’une tranche MIP. Autrement dit, chaque texture dans une vue de cible de rendu doit avoir la même taille. Un [**affichage des ressources de nuanceur**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) peut sélectionner n’importe quelle région rectangulaire de sous-ressources, comme illustré dans la figure.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ressources](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





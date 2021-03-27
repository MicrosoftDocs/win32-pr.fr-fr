---
title: Structures de ressources (graphiques Direct3D 11)
description: Les structures sont utilisées pour créer et utiliser des ressources.
ms.assetid: a29e01ac-8aa1-4a40-ad4d-3b738e129436
keywords:
- structures, ressource Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5020792e1fb56a52e7a4354964c45bb5d65bbba4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103843009"
---
# <a name="resource-structures-direct3d-11-graphics"></a>Structures de ressources (graphiques Direct3D 11)

Les structures sont utilisées pour créer et utiliser des ressources.


## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                         | Description                                                                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**Description de la \_ mémoire tampon d3d11 \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc)<br/>                                   | Décrit une ressource de mémoire tampon.<br/>                                                                           |
| [**D3D11 \_ - \_ RTV de tampon**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_rtv)<br/>                                     | Spécifie les éléments d’une ressource de mémoire tampon à utiliser dans une vue de cible de rendu.<br/>                            |
| [**\_Mémoire tampon d3d11 \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_srv)<br/>                                     | Spécifie les éléments d’une ressource de mémoire tampon à utiliser dans un affichage des ressources de nuanceur.<br/>                          |
| [**\_Mémoire tampon d3d11 \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_uav)<br/>                                     | Décrit les éléments d’une mémoire tampon à utiliser dans un affichage d’accès non ordonné.<br/>                                  |
| [**D3D11 \_ BUFFEREX \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_bufferex_srv)<br/>                                 | Décrit les éléments d’une ressource de mémoire tampon brute à utiliser dans un affichage des ressources de nuanceur.<br/>                      |
| [**\_Vue du stencil de profondeur d3d11 \_ \_ \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc)<br/>         | Spécifie les sous-ressources d’une texture qui sont accessibles à partir d’une vue de stencil de profondeur.<br/>                 |
| [**Sous- \_ ressource mappée d3d11 \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource)<br/>                     | Fournit l’accès aux données de sous-ressource.<br/>                                                                   |
| [**\_Description MIP d3d11 compressée \_ \_**](/windows/desktop/api/d3d11_2/ns-d3d11_2-d3d11_packed_mip_desc)<br/>                          | Décrit la structure de vignette d’une ressource en mosaïque avec des mipmaps. <br/>                                        |
| [**Vue de la \_ cible de rendu d3d11 \_ \_ \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_render_target_view_desc)<br/>         | Spécifie les sous-ressources d’une ressource qui sont accessibles à l’aide d’une vue de cible de rendu.<br/>             |
| [**Vue de la \_ cible de rendu d3d11 \_ \_ \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_render_target_view_desc1)<br/>       | Décrit les sous-ressources d’une ressource qui sont accessibles à l’aide d’une vue de cible de rendu.<br/>             |
| [**Vue de la \_ ressource du nuanceur d3d11 \_ \_ \_ desc**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc)<br/>     | Décrit un affichage des ressources de nuanceur.<br/>                                                                      |
| [**\_Affichage des ressources du nuanceur d3d11 \_ \_ \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_shader_resource_view_desc1)<br/>   | Décrit un affichage des ressources de nuanceur.<br/>                                                                      |
| [**Données de sous- \_ ressources d3d11 \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data)<br/>                         | Spécifie des données pour l’initialisation d’une sous-ressource.<br/>                                                         |
| [**Mosaïque de sous- \_ ressources d3d11 \_**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_subresource_tiling)<br/>                     | Décrit un volume de sous-ressources en mosaïque.<br/>                                                                  |
| [**\_DSV d3d11 TEX1D \_ array \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_dsv)<br/>                          | Spécifie les sous-ressources d’un tableau de textures 1D à utiliser dans une vue de stencil de profondeur.<br/>                |
| [**D3D11 \_ \_ tableau TEX1D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_rtv)<br/>                          | Spécifie les sous-ressources d’un tableau de textures 1D à utiliser dans une vue de cible de rendu.<br/>                |
| [**\_SRV du \_ tableau d3d11 TEX1D \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_srv)<br/>                          | Spécifie les sous-ressources d’un tableau de textures 1D à utiliser dans un affichage des ressources de nuanceur.<br/>              |
| [**D3D11 \_ TEX1D \_ array \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_uav)<br/>                          | Décrit un tableau de ressources de texture 1D avec accès non ordonné.<br/>                                           |
| [**D3D11 \_ TEX1D \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_dsv)<br/>                                       | Spécifie la sous-ressource d’une texture 1D qui est accessible à une vue de stencil de profondeur.<br/>                |
| [**D3D11 \_ TEX1D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_rtv)<br/>                                       | Spécifie la sous-ressource à partir d’une texture 1D à utiliser dans une vue de cible de rendu.<br/>                            |
| [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv)<br/>                                       | Spécifie la sous-ressource d’une texture 1D à utiliser dans un affichage des ressources de nuanceur.<br/>                          |
| [**D3D11 \_ TEX1D \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_uav)<br/>                                       | Décrit une ressource de texture 1D avec accès non ordonné.<br/>                                                      |
| [**\_DSV d3d11 TEX2D \_ array \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_dsv)<br/>                          | Spécifie les sous-ressources d’une texture 2D de tableau qui sont accessibles à une vue de stencil de profondeur.<br/>      |
| [**D3D11 \_ \_ tableau TEX2D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_rtv)<br/>                          | Spécifie les sous-ressources d’un tableau de textures 2D à utiliser dans une vue de cible de rendu.<br/>                |
| [**D3D11 \_ TEX2D \_ array \_ RTV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_array_rtv1)<br/>                        | Décrit les sous-ressources d’un tableau de textures 2D à utiliser dans une vue de cible de rendu.<br/>                |
| [**\_SRV du \_ tableau d3d11 TEX2D \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_srv)<br/>                          | Spécifie les sous-ressources d’un tableau de textures 2D à utiliser dans un affichage des ressources de nuanceur.<br/>              |
| [**D3D11 \_ TEX2D \_ array \_ SRV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_array_srv1)<br/>                        | Décrit les sous-ressources d’un tableau de textures 2D à utiliser dans un affichage des ressources de nuanceur.<br/>              |
| [**D3D11 \_ TEX2D \_ array \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_uav)<br/>                          | Décrit un tableau de ressources de texture 2D avec accès non ordonné.<br/>                                           |
| [**D3D11 \_ TEX2D \_ array \_ UAV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_array_uav1)<br/>                        | Décrit un tableau de ressources de texture 2D avec accès non ordonné.<br/>                                           |
| [**D3D11 \_ TEX2D \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_dsv)<br/>                                       | Spécifie la sous-ressource d’une texture 2D qui est accessible à une vue de stencil de profondeur.<br/>                |
| [**D3D11 \_ TEX2D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_rtv)<br/>                                       | Spécifie la sous-ressource d’une texture 2D à utiliser dans une vue de cible de rendu.<br/>                            |
| [**D3D11 \_ TEX2D \_ RTV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_rtv1)<br/>                                     | Décrit la sous-ressource d’une texture 2D à utiliser dans une vue de cible de rendu.<br/>                            |
| [**D3D11 \_ TEX2D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_srv)<br/>                                       | Spécifie la sous-ressource d’une texture 2D à utiliser dans un affichage des ressources de nuanceur.<br/>                          |
| [**D3D11 \_ TEX2D \_ SRV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_srv1)<br/>                                     | Décrit la sous-ressource d’une texture 2D à utiliser dans un affichage des ressources de nuanceur.<br/>                          |
| [**D3D11 \_ TEX2D \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_uav)<br/>                                       | Décrit une ressource de texture 2D avec accès non ordonné.<br/>                                                      |
| [**D3D11 \_ TEX2D \_ UAV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_uav1)<br/>                                     | Décrit une ressource de texture 2D avec accès non ordonné.<br/>                                                      |
| [**\_DSV d3d11 TEX2DMS \_ array \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_array_dsv)<br/>                      | Spécifie les sous-ressources d’un tableau de textures 2D à échantillonnages pour une vue de stencil de profondeur.<br/>         |
| [**D3D11 \_ \_ tableau TEX2DMS \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_array_rtv)<br/>                      | Spécifie les sous-ressources d’un tableau de textures 2D multiéchantillonnées à utiliser dans une vue de cible de rendu.<br/> |
| [**\_SRV du \_ tableau d3d11 TEX2DMS \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_array_srv)<br/>                      | Spécifie les sous-ressources d’un tableau de textures 2D à échantillonnages à utiliser dans un affichage des ressources de nuanceur.<br/> |
| [**D3D11 \_ TEX2DMS \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_dsv)<br/>                                   | Spécifie la sous-ressource à partir d’une texture 2D échantillonnée qui est accessible à une vue de stencil de profondeur.<br/>   |
| [**D3D11 \_ TEX2DMS \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_rtv)<br/>                                   | Spécifie la sous-ressource d’une texture 2D à échantillonnages à utiliser dans une vue de cible de rendu.<br/>               |
| [**D3D11 \_ TEX2DMS \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_srv)<br/>                                   | Spécifie les sous-ressources d’une texture 2D à échantillonnages à utiliser dans un affichage des ressources de nuanceur.<br/>            |
| [**D3D11 \_ TEX3D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex3d_rtv)<br/>                                       | Spécifie les sous-ressources d’une texture 3D à utiliser dans une vue de cible de rendu.<br/>                           |
| [**D3D11 \_ TEX3D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex3d_srv)<br/>                                       | Spécifie les sous-ressources d’une texture 3D à utiliser dans un affichage des ressources de nuanceur.<br/>                         |
| [**D3D11 \_ TEX3D \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex3d_uav)<br/>                                       | Décrit une ressource de texture 3D avec accès non ordonné.<br/>                                                      |
| [**\_SRV du \_ tableau d3d11 TEXCUBE \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texcube_array_srv)<br/>                      | Spécifie les sous-ressources d’un tableau de textures de cube à utiliser dans un affichage des ressources de nuanceur.<br/>            |
| [**D3D11 \_ TEXCUBE \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texcube_srv)<br/>                                   | Spécifie la sous-ressource d’une texture de cube à utiliser dans un affichage des ressources de nuanceur.<br/>                        |
| [**D3D11 \_ TEXTURE1D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture1d_desc)<br/>                             | Décrit une texture 1D.<br/>                                                                                |
| [**D3D11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc)<br/>                             | Décrit une texture 2D.<br/>                                                                                |
| [**D3D11 \_ TEXTURE2D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture2d_desc1)<br/>                           | Décrit une texture 2D.<br/>                                                                                |
| [**D3D11 \_ TEXTURE3D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture3d_desc)<br/>                             | Décrit une texture 3D.<br/>                                                                                |
| [**D3D11 \_ TEXTURE3D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture3d_desc1)<br/>                           | Décrit une texture 3D.<br/>                                                                                |
| [**Taille de la \_ zone de vignette d3d11 \_ \_**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size)<br/>                        | Décrit la taille d’une région en mosaïque.<br/>                                                                  |
| [**\_Coordonnée de ressources en mosaïque d3d11 \_ \_**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate)<br/>      | Décrit les coordonnées d’une ressource en mosaïque.<br/>                                                         |
| [**\_Forme de vignette d3d11 \_**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape)<br/>                                     | Décrit la forme d’une vignette en spécifiant ses dimensions.<br/>                                            |
| [**D3D11 \_ vue d’accès non ordonné \_ \_ \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_unordered_access_view_desc)<br/>   | Spécifie les sous-ressources d’une ressource qui sont accessibles à l’aide d’un affichage d’accès non ordonné.<br/>         |
| [**D3D11 \_ vue d’accès non ordonné \_ \_ \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_unordered_access_view_desc1)<br/> | Décrit les sous-ressources d’une ressource qui sont accessibles à l’aide d’un affichage d’accès non ordonné.<br/>         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de ressource](d3d11-graphics-reference-resource.md)
</dt> </dl>

 

 






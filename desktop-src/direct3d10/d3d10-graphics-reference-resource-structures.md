---
description: Structures utilisées pour créer et utiliser des ressources.
ms.assetid: d8fe2ebe-349a-456e-9a5a-16f2d3419800
title: Structures de ressources (graphiques Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da964bf19c1ce5e1e5c4dfd0685df79b28ac5e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513928"
---
# <a name="resource-structures-direct3d-10-graphics"></a>Structures de ressources (graphiques Direct3D 10)

Structures utilisées pour créer et utiliser des [ressources](d3d10-graphics-programming-guide-resources-types.md).



| Structures                                                                 | Description                                                                                                                                                   |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Description de la \_ mémoire tampon D3D10 \_**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)                           | Description d’une ressource de [mémoire tampon](d3d10-graphics-programming-guide-resources-types.md) .                                                                     |
| [**D3D10 \_ - \_ RTV de tampon**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_buffer_rtv)                             | Décrit les éléments d’une [mémoire tampon](d3d10-graphics-programming-guide-resources-types.md) à utiliser dans une vue de cible de rendu.                                |
| [**\_Mémoire tampon D3D10 \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_buffer_srv)                             | Décrit les éléments d’une ressource de [mémoire tampon](d3d10-graphics-programming-guide-resources-types.md) à utiliser dans un affichage des ressources de nuanceur.                         |
| [**\_Vue du stencil de profondeur D3D10 \_ \_ \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_view_desc) | Décrit une vue de stencil de profondeur.                                                                                                                               |
| [**D3D10 \_ mappé \_ TEXTURE2D**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_mapped_texture2d)                 | Fournit l’accès aux données de sous-ressource dans une [texture 2D](d3d10-graphics-programming-guide-resources-types.md).                                                  |
| [**D3D10 \_ mappé \_ TEXTURE3D**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_mapped_texture3d)                 | Fournit l’accès aux données de sous-ressource dans une [texture 3D](d3d10-graphics-programming-guide-resources-types.md).                                                  |
| [**Vue de la \_ cible de rendu D3D10 \_ \_ \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_render_target_view_desc) | Décrit une vue de cible de rendu.                                                                                                                               |
| [**Données de sous- \_ ressources D3D10 \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data)                 | Spécifie des données pour l’initialisation d’une ressource.                                                                                                                   |
| [**\_DSV D3D10 TEX1D \_ array \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_dsv)                  | Spécifie le niveau de mipmap et les textures dans un [tableau de texture 1D](d3d10-graphics-programming-guide-resources-types.md) à utiliser dans une vue de stencil de profondeur.       |
| [**D3D10 \_ \_ tableau TEX1D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_rtv)                  | Spécifie la ou les sous-ressources d’un tableau de [textures 1D](d3d10-graphics-programming-guide-resources-types.md) à utiliser dans une vue de cible de rendu.             |
| [**\_SRV du \_ tableau D3D10 TEX1D \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_srv)                  | Spécifie les niveaux de mipmap et les textures dans un [tableau de texture 1D](d3d10-graphics-programming-guide-resources-types.md) à utiliser dans un affichage des ressources de nuanceur.      |
| [**D3D10 \_ TEX1D \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_dsv)                               | Spécifie la ou les sous-ressources d’une [texture 1D](d3d10-graphics-programming-guide-resources-types.md) à utiliser dans une vue de stencil de profondeur.                        |
| [**D3D10 \_ TEX1D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_rtv)                               | Spécifie la ou les sous-ressources d’une [texture 1D](d3d10-graphics-programming-guide-resources-types.md) à utiliser dans une vue de cible de rendu.                        |
| [**D3D10 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_srv)                               | Spécifie la ou les sous-ressources d’une [texture 1D](d3d10-graphics-programming-guide-resources-types.md) à utiliser dans un affichage des ressources de nuanceur.                      |
| [**\_DSV D3D10 TEX2D \_ array \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_dsv)                  | Spécifie le niveau de mipmap et les textures dans un [tableau de textures 2D](d3d10-graphics-programming-guide-resources-types.md) à utiliser dans une vue de stencil de profondeur. |
| [**D3D10 \_ \_ tableau TEX2D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_rtv)                  | Spécifie le niveau de mipmap et les textures dans un [tableau de textures 2D](d3d10-graphics-programming-guide-resources-types.md) à utiliser dans une vue de cible de rendu. |
| [**\_SRV du \_ tableau D3D10 TEX2D \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_srv)                  | Spécifie la ou les sous-ressources d’un tableau de [textures 2D](d3d10-graphics-programming-guide-resources-types.md) à utiliser dans un affichage des ressources de nuanceur.           |
| [**D3D10 \_ TEX2D \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_dsv)                               | Spécifie la ou les sous-ressources d’une [texture 2D](d3d10-graphics-programming-guide-resources-types.md) à utiliser dans une vue de stencil de profondeur.                        |
| [**D3D10 \_ TEX2D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_rtv)                               | Spécifie la ou les sous-ressources d’une [texture 2D](d3d10-graphics-programming-guide-resources-types.md) à utiliser dans une vue de cible de rendu.                        |
| [**D3D10 \_ TEX2D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_srv)                               | Spécifie la ou les sous-ressources d’une [texture 2D](d3d10-graphics-programming-guide-resources-types.md) à utiliser dans un affichage des ressources de nuanceur.                      |
| [**\_DSV D3D10 TEX2DMS \_ array \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_dsv)              | Spécifie la ou les sous-ressources d’un tableau de [textures 2D](d3d10-graphics-programming-guide-resources-types.md) à utiliser dans une vue de stencil de profondeur.             |
| [**D3D10 \_ \_ tableau TEX2DMS \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_rtv)              | Spécifie la ou les sous-ressources d’un tableau de [textures 2D](d3d10-graphics-programming-guide-resources-types.md) à utiliser dans une vue de cible de rendu.             |
| [**\_SRV du \_ tableau D3D10 TEX2DMS \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_srv)              | Spécifie la ou les sous-ressources d’un tableau de [textures 2D](d3d10-graphics-programming-guide-resources-types.md) à utiliser dans un affichage des ressources de nuanceur.           |
| [**D3D10 \_ TEX2DMS \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_dsv)                           | Spécifie la ou les sous-ressources d’une [texture 2D](d3d10-graphics-programming-guide-resources-types.md) à échantillonnages à utiliser dans une vue de stencil de profondeur.           |
| [**D3D10 \_ TEX2DMS \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_rtv)                           | Spécifie la ou les sous-ressources d’une [texture 2D](d3d10-graphics-programming-guide-resources-types.md) à échantillonnages à utiliser dans une vue de cible de rendu.           |
| [**D3D10 \_ TEX2DMS \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_srv)                           | Spécifie la ou les sous-ressources d’une [texture 2D](d3d10-graphics-programming-guide-resources-types.md) à échantillonnages à utiliser dans un affichage des ressources de nuanceur.         |
| [**D3D10 \_ TEX3D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex3d_rtv)                               | Spécifie la ou les sous-ressources d’une [texture 3D](d3d10-graphics-programming-guide-resources-types.md) à utiliser dans une vue de cible de rendu.                        |
| [**D3D10 \_ TEX3D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex3d_srv)                               | Spécifie la ou les sous-ressources d’une [texture 3D](d3d10-graphics-programming-guide-resources-types.md) à utiliser dans un affichage des ressources de nuanceur.                      |
| [**D3D10 \_ TEXCUBE \_ array \_ SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1)            | Spécifie la ou les sous-ressources d’une [texture de cube](d3d10-graphics-programming-guide-resources-types.md) à utiliser dans un affichage des ressources de nuanceur.                    |
| [**D3D10 \_ TEXCUBE \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_texcube_srv)                           | Spécifie la ou les sous-ressources d’une [texture de cube](d3d10-graphics-programming-guide-resources-types.md) à utiliser dans un affichage des ressources de nuanceur.                    |
| [**D3D10 \_ TEXTURE1D \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture1d_desc)                     | Décrit une ressource de [texture 1D](d3d10-graphics-programming-guide-resources-types.md) .                                                                      |
| [**D3D10 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture2d_desc)                     | Décrit une ressource de [texture 2D](d3d10-graphics-programming-guide-resources-types.md) .                                                                      |
| [**D3D10 \_ TEXTURE3D \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture3d_desc)                     | Décrit une ressource de [texture 3D](d3d10-graphics-programming-guide-resources-types.md) .                                                                      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de ressource](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 




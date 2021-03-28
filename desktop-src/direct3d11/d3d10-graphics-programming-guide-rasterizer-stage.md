---
title: Étape du rastériseur
description: L’étape de pixellisation convertit les informations vectorielles (composées de formes ou de Primitives) en une image raster (composée de pixels) pour l’affichage de graphiques 3D en temps réel.
ms.assetid: efd3f819-7c63-4e1a-9923-8e7198354ec6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e746c5ace3512f36f9b9ad34d34a3ea578e1de36
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103941498"
---
# <a name="rasterizer-stage"></a>Étape du rastériseur

L’étape de pixellisation convertit les informations vectorielles (composées de formes ou de Primitives) en une image raster (composée de pixels) pour l’affichage de graphiques 3D en temps réel.

Pendant la pixellisation, chaque primitive est convertie en pixels, tout en interpolant les valeurs par vertex sur chaque primitive. La pixellisation comprend des sommets de découpage pour la vue frustum, en effectuant une division par z pour fournir une perspective, en mappant les primitives à une fenêtre d’affichage 2D et en déterminant comment appeler le nuanceur de pixels. Bien que l’utilisation d’un nuanceur de pixels soit facultative, l’étape de rastérisation effectue toujours le découpage, une division de perspective pour transformer les points en un espace homogène et mappe les vertex à la fenêtre d’affichage.

Les sommets (x, y, z, w), arrivant à l’étape de rastérisation, sont supposés être dans l’espace de clip homogène. Dans cet espace de coordonnées, les points de l’axe X sont à droite, Y pointe vers le haut et Z points loin de l’appareil photo.

Vous pouvez désactiver la pixellisation en indiquant au pipeline qu’il n’existe aucun nuanceur de pixels (définissez l’étape nuanceur de pixels sur **null** avec [**ID3D11DeviceContext ::P ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader)) et désactivez les tests de profondeur et de stencil (définissez **DepthEnable** et **StencilEnable** sur **false** dans le [**stencil de profondeur d3d11 \_ \_ \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)). Quand la rastérisation est désactivée, les compteurs du pipeline relatif à la rastérisation ne sont pas mis à jour. Il existe également une description complète des [règles de pixellisation](d3d10-graphics-programming-guide-rasterizer-stage-rules.md).

Sur le matériel qui implémente des optimisations hiérarchiques de la mémoire tampon Z, vous pouvez activer le préchargement de la mémoire tampon z en affectant à l’étape nuanceur de pixels la **valeur null** tout en activant le test de profondeur et de stencil.


## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                                         | Description                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Prise en main avec l’étape de rastérisation](d3d10-graphics-programming-guide-rasterizer-stage-getting-started.md)<br/> | Cette section décrit la définition de la fenêtre d’affichage, du rectangle de ciseaux, de l’état du rastériseur et de l’échantillonnage multiple.<br/>                                                                                                                                                                                                |
| [Règles de pixellisation](d3d10-graphics-programming-guide-rasterizer-stage-rules.md)<br/>                                 | Les règles de pixellisation définissent la façon dont les données vectorielles sont mappées dans les données raster. Les données raster sont alignées sur les emplacements d’entiers qui sont ensuite éliminés et découpés (pour dessiner le nombre minimal de pixels), et les attributs par pixel sont interpolés (à partir des attributs par vertex) avant d’être passés à un nuanceur de pixels.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Pipeline graphique](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Étapes de pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 


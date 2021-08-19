---
description: Constantes de limitation de ressources.
ms.assetid: a6bfba45-7a0c-4894-a0a6-ee468002175d
title: D3D10_REQ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32e099c26706772bbb76ad6709759fa4712e22ea3bc9793b905a2050f25d0f75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118100751"
---
# <a name="d3d10_req"></a>D3D10 \_ req

Constantes de limitation de ressources.



| \#définition                                      | Valeur | Description                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ Niveaux MIP D3D10 \_ req                       | 14    | Nombre maximal de niveaux de mipmap qu’une ressource de texture peut avoir.                                                                                                                                                                                                                                                                                                                                                                    |
| \_ \_ Taille de la ressource req D3D10 \_ \_ en \_ mégaoctets     | 128   | Taille maximale possible d’une ressource en mégaoctets. Les applications peuvent créer des ressources plus volumineuses que la taille maximale des ressources sur un matériel graphique. Toutefois, nous recommandons que les applications conservent des ressources inférieures à la taille maximale des ressources pour bénéficier de la compatibilité maximale entre les fournisseurs de graphiques. Le runtime garantit que les allocations au sein de la taille maximale des ressources sont prises en charge par tout le matériel Direct3D 10. |
| DIMENSION de l' \_ axe du tableau D3D10 req \_ TEXTURE1D \_ \_ \_ | 512   | Taille maximale d’un tableau de texture 1D.                                                                                                                                                                                                                                                                                                                                                                                       |
| DIMENSION de l' \_ axe du tableau D3D10 req \_ TEXTURE2D \_ \_ \_ | 512   | Taille de tableau maximale d’un tableau de textures 2D.                                                                                                                                                                                                                                                                                                                                                                                       |
| \_Dimension D3D10 req \_ TEXTURE1D \_ U \_           | 8 192  | Largeur maximale d’une texture 1D.                                                                                                                                                                                                                                                                                                                                                                                                  |
| \_Dimension D3D10 req \_ TEXTURE2D \_ U \_ ou \_ V \_    | 8 192  | Largeur et hauteur maximales d’une texture 2D.                                                                                                                                                                                                                                                                                                                                                                                       |
| D3D10 \_ req \_ TEXTURE3D \_ U \_ V \_ ou \_ W \_ dimension | 2 048  | Largeur, hauteur et profondeur maximales d’une texture 3D.                                                                                                                                                                                                                                                                                                                                                                               |
| D3D10 \_ req \_ TEXTURECUBE \_ dimension            | 8 192  | Taille maximale d’une texture de cube.                                                                                                                                                                                                                                                                                                                                                                                                 |



 

Les constantes sont définies dans D3D10. h.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes de ressource](d3d10-graphics-reference-resource-constants.md)
</dt> <dt>

[Référence Direct3D](d3d10-graphics-reference-d3d10.md)
</dt> </dl>

 

 




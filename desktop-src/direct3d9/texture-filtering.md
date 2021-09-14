---
description: Lorsque Direct3D rend une primitive, il mappe la primitive 3D sur un écran 2D.
ms.assetid: vs|directx_sdk|~\texture_filtering.htm
title: Filtrage de texture (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faeeb83e1a3bc7fc03534771b15b6076aeb48f8c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127291735"
---
# <a name="texture-filtering-direct3d-9"></a>Filtrage de texture (Direct3D 9)

Lorsque Direct3D rend une primitive, il mappe la primitive 3D sur un écran 2D. Si la primitive a une texture, Direct3D doit utiliser cette texture pour produire une couleur pour chaque pixel dans l’image de rendu 2D de la primitive. Pour chaque pixel de l’image à l’écran de la primitive, il doit obtenir une valeur de couleur de la texture. Ce processus est appelé filtrage de texture.

Lorsqu’une opération de filtre de texture est effectuée, la texture utilisée est généralement agrandie ou minimisés. En d’autres termes, elle est mappée dans une image primitive plus grande ou plus petite que celle-ci. Le grossissement d’une texture peut entraîner le mappage de plusieurs pixels à un seul Texel. Le résultat peut être une apparence groupée. La minimisation d’une texture signifie souvent qu’un seul pixel est mappé à de nombreux texels. L’image résultante peut être floue ou avec un alias. Pour résoudre ces problèmes, une fusion des couleurs texels doit être effectuée pour atteindre une couleur pour le pixel.

Direct3D simplifie le processus complexe de filtrage de texture. Il offre trois types de filtrage de texture : le filtrage linéaire, le filtrage anisotrope et le filtrage mipmap. Si vous ne sélectionnez aucun filtrage de texture, Direct3D utilise une technique appelée échantillonnage à point le plus proche.

Chaque type de filtrage de texture présente des avantages et des inconvénients. Par exemple, le filtrage de texture linéaire peut produire des bords dentelés ou une apparence groupée dans l’image finale. Toutefois, il s’agit d’une méthode de faible surcharge de calcul de filtrage de texture. Le filtrage avec des mipmaps produit généralement les meilleurs résultats, en particulier lorsqu’il est combiné avec le filtrage anisotrope. Toutefois, il requiert la plus grande partie de la mémoire des techniques prises en charge par Direct3D.

Les applications qui utilisent des pointeurs d’interface de texture doivent définir la méthode de filtrage de texture actuelle en appelant la méthode [**IDirect3DDevice9 :: SetSamplerState**](/windows/desktop/api) . Définissez la valeur du premier paramètre sur le numéro d’index entier (0-7) de la texture pour laquelle vous sélectionnez une méthode de filtrage de texture. Transmettez D3DSAMP \_ MAGFILTER, D3DSAMP \_ MINFILTER ou D3DSAMP \_ MIPFILTER pour le deuxième paramètre afin de définir le filtre d’agrandissement, de minimisation ou de mappage MIP. Transmettez un membre du type énuméré [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) comme valeur dans le troisième paramètre.

Cette section présente les méthodes de filtrage de texture prises en charge par Direct3D. Elle est organisée dans les rubriques suivantes.

-   [Échantillonnage à point le plus proche (Direct3D 9)](nearest-point-sampling.md)
-   [Filtrage de texture linéaire (Direct3D 9)](linear-texture-filtering.md)
-   [Filtrage de texture bilinéaire (Direct3D 9)](bilinear-texture-filtering.md)
-   [Filtrage de texture anisotrope (Direct3D 9)](anisotropic-texture-filtering.md)
-   [Filtrage de texture avec des mipmaps (Direct3D 9)](texture-filtering-with-mipmaps.md)

> [!Note]  
> Bien que les États de rendu de filtrage de texture présents dans le type énuméré [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) soient remplacés par les États d’étape de texture, [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate), par opposition à la version IDirect3DDevice2, n’échoue pas si vous tentez de les utiliser. Au lieu de cela, le système mappe les effets de ces États de rendu à la première étape de la cascade de multitextures, étape 0. Les applications ne doivent pas mélanger les États de rendu hérités à leurs États d’étape de texture correspondants, car des résultats imprévisibles peuvent se produire.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Textures Direct3D](direct3d-textures.md)
</dt> </dl>

 

 

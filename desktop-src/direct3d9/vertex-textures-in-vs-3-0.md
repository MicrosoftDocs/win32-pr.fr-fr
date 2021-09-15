---
description: Le modèle Vertex Shader 3,0 prend en charge la recherche de texture dans le nuanceur de sommets à l’aide de l’instruction texldl-vs texture Load.
ms.assetid: 595cb5c0-da12-4fe9-944c-a61d8ed990b4
title: Textures de vertex dans vs_3_0 (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a4e8e7bbf7e1ae9764fe5b30647f318dfaeb3ba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530949"
---
# <a name="vertex-textures-in-vs_3_0-directx-hlsl"></a>Textures de vertex dans vs \_ 3 \_ 0 (DirectX HLSL)

Le modèle Vertex Shader 3,0 prend en charge la recherche de texture dans le nuanceur de sommets à l’aide de l’instruction [texldl-vs](../direct3dhlsl/texldl---vs.md) texture Load. Le moteur vertex contient quatre étapes d’échantillonnage de texture, nommées [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md), D3DVERTEXTEXTURESAMPLER1, D3DVERTEXTEXTURESAMPLER2 et D3DVERTEXTEXTURESAMPLER3. Celles-ci sont distinctes de l’échantillonneur de mappage et des échantillonneurs de texture dans le moteur de pixels.

Pour échantillonner les textures à ces quatre étapes, vous pouvez utiliser le moteur de vertex et programmer les étapes avec la méthode [**CheckDeviceFormat**](/windows/desktop/api) . Définissez les textures à ces étapes à l’aide de [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture), avec l’index intermédiaire [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md) jusqu’à D3DVERTEXTEXTURESAMPLER3. Un nouveau registre a été introduit dans le nuanceur de sommets, le registre de l’échantillonneur (comme dans PS \_ 2 \_ 0), qui représente l’échantillonneur de texture de vertex. Ce registre doit être défini dans le nuanceur avant de l’utiliser.

Une application peut demander si un format est pris en charge en tant que texture de vertex en appelant [**CheckDeviceFormat**](/windows/desktop/api) avec [D3DUSAGE \_ query \_ VERTEXTEXTURE](d3dusage-query.md).

> [!Note]  
> Il s’agit d’un indicateur de requête qui n’est pas accepté dans une fonction CreateXXX. Une texture de vertex créée dans le pool par défaut peut être définie comme une texture de pixels et vice versa. Toutefois, pour utiliser le traitement du vertex logiciel, la texture de vertex doit être créée dans le pool de Scratch (peu importe s’il s’agit d’un appareil en mode mixte ou d’un périphérique de traitement de vertex logiciel).

 

Les fonctionnalités sont identiques aux textures de pixels, à l’exception des éléments suivants :

-   Le filtrage de texture anisotrope n’est pas pris en charge, c’est pourquoi D3DSAMP \_ MAXANISOTROPY est ignoré et D3DTEXF \_ anisotrope ne peut pas être défini pour la loupe, ou réduire pour ces étapes.
-   Le taux d’informations sur les modifications n’est pas disponible. par conséquent, l’application doit calculer le niveau de détail et fournir ces informations en tant que paramètre à [texldl-vs](../direct3dhlsl/texldl---vs.md).

Les restrictions sont les suivantes :

-   Comme dans les nuanceurs de pixels, si les textures multiéléments sont prises en charge, D3DSAMP \_ ELEMENTINDEX est utilisé pour déterminer l’élément à partir duquel échantillonner.
-   L’État D3DSAMP \_ DMAPOFFSET est ignoré pour ces étapes.
-   Utilisez [**CheckDeviceFormat**](/windows/desktop/api) avec [D3DUSAGE \_ query \_ VERTEXTEXTURE»](d3dusage-query.md) pour interroger une texture afin de déterminer si elle peut être utilisée comme texture de vertex.
-   VertexTextureFilterCaps indique le type de filtres qui sont autorisés au niveau des échantillonneurs de texture de vertex. [D3DPTFILTERCAPS \_ MINFANISOTROPIC](d3dptfiltercaps.md) et D3DPTFILTERCAPS \_ MAGFANISOTROPIC ne sont pas autorisés.

## <a name="sampling-stage-registers"></a>Registres des étapes d’échantillonnage

Un registre des étapes d’échantillonnage identifie une unité d’échantillonnage qui peut être utilisée dans les instructions de chargement de texture. Une unité d’échantillonnage correspond à la phase d’échantillonnage de texture, en encapsulant l’état spécifique à l’échantillonnage fourni dans [**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate).

Chaque échantillonneur identifie de façon unique une surface de texture unique qui est définie sur l’échantillonneur correspondant à l’aide de [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture). Toutefois, la même surface de texture peut être définie sur plusieurs échantillonneurs.

Au moment du tracé, une texture ne peut pas être définie simultanément comme une cible de rendu et une texture à une étape.

Étant donné que vs \_ 3 \_ 0 prend en charge quatre échantillonneurs, jusqu’à quatre surfaces de texture peuvent être lues à partir d’une seule passe de nuanceur. Un registre d’échantillonnage peut apparaître uniquement comme argument dans l’instruction de chargement de texture : [texldl-vs](../direct3dhlsl/texldl---vs.md).

Dans vs \_ 3 \_ 0, si vous utilisez un échantillonneur, il doit être déclaré au début du programme Shader, à l’aide de la [DCL \_ samplerType (SM3-vs ASM)](../direct3dhlsl/dcl-samplertype---vs.md) (comme dans PS \_ 2 \_ 0).

## <a name="software-processing"></a>Traitement logiciel

Ce composant sera pris en charge dans le traitement des vertex logiciels. Les types de filtres spécifiques pris en charge peuvent être vérifiés en appelant [**GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) et en vérifiant VertexTextureFilterCaps. Tous les formats de texture publiés seront pris en charge en tant que textures vertex dans le traitement des vertex logiciels.

Les applications peuvent vérifier si un format de texture particulier est pris en charge dans le mode de traitement du vertex logiciel en appelant [**CheckDeviceFormat**](/windows/desktop/api) et en fournissant (D3DVERTEXTEXTURESAMPLER \| [**D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md)) comme utilisation. Tous les formats sont pris en charge pour le traitement des vertex logiciels. Le pool de travail est requis pour le traitement des vertex logiciels.

## <a name="api-changes"></a>Modifications de l’API


```
   
// New define
#define D3DVERTEXTEXTURESAMPLER0 (D3DDMAPSAMPLER+1)
#define D3DVERTEXTEXTURESAMPLER1 (D3DDMAPSAMPLER+2)
#define D3DVERTEXTEXTURESAMPLER2 (D3DDMAPSAMPLER+3)
#define D3DVERTEXTEXTURESAMPLER3 (D3DDMAPSAMPLER+4)
    

#define D3DVERTEXTEXTURESAMPLER  (0x00100000L)

// New caps field in D3DCAPS9
DWORD VertexTextureFilterCaps;
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Pipeline de vertex](vertex-pipeline.md)
</dt> </dl>

 

 

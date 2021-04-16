---
description: Un bloc d’État peut être utilisé pour capturer uniquement l’état des pixels (consultez États d’enregistrement et de restauration des blocs d’État (Direct3D 9)).
ms.assetid: 30624c0a-e30f-4383-bc0c-b43f42403e72
title: Enregistrement de l’état de Pixel avec un StateBlock (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80741d9f17939d5795163a3e84c58bcdb9003c70
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522388"
---
# <a name="saving-pixel-state-with-a-stateblock-direct3d-9"></a>Enregistrement de l’état de Pixel avec un StateBlock (Direct3D 9)

Un bloc d’État peut être utilisé pour capturer uniquement l’état des pixels (consultez États d' [enregistrement et de restauration des blocs d’État (Direct3D 9)](state-blocks-save-and-restore-state.md)). L’état de pixel est le suivant :

-   État du rendu de pixel (voir [pipeline de pixels : état de rendu](#pixel-pipeline-render-state)).
-   État de la texture pixel (voir [pipeline de pixels : état](#pixel-pipeline-texture-state)de la texture).
-   État de l’échantillonneur de pixels (voir [pipeline de pixels : état de l’échantillonneur](#pixel-pipeline-sampler-state)).
-   Le nuanceur de pixels actuel et chacune des constantes de nuanceur de pixels.

Pour capturer l’état de Pixel avec un bloc d’État, spécifiez D3DSBT \_ PIXELSTATE lors de l’appel de [**IDirect3DDevice9 :: CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).

## <a name="pixel-pipeline-render-state"></a>Pipeline de pixels : état de rendu

Les États de rendu des appareils affectent le comportement de presque toutes les parties du pipeline. Les États de rendu sont définis en appelant [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).

Le tableau suivant répertorie tous les États de rendu qui configurent l’état des pixels :



| États de rendu                              | Valeur par défaut      |
|--------------------------------------------|--------------------|
| D3DRS \_ ZENABLE                             | D3DZB \_ false       |
| D3DRS \_ SpecularEnable                      | **FALSE**          |
| [**D3DFILLMODE**](./d3dfillmode.md)   | D3DFILL \_ Solid     |
| [**D3DSHADEMODE**](./d3dshademode.md) | D3DSHADE \_ Gouraud  |
| D3DRS \_ ZWRITEENABLE                        | **TRUE**           |
| D3DRS \_ ALPHATESTENABLE                     | **FALSE**          |
| D3DRS \_ LASTPIXEL                           | **TRUE**           |
| D3DRS \_ SRCBLEND                            | D3DBLEND \_ un      |
| D3DRS \_ DESTBLEND                           | D3DBLEND \_ zéro     |
| D3DRS \_ ZFUNC                               | D3DCMP \_ LESSEQUAL  |
| D3DRS \_ ALPHAREF                            | 0                  |
| D3DRS \_ ALPHAFUNC                           | D3DCMP \_ toujours     |
| D3DRS \_ DITHERENABLE                        | **FALSE**          |
| D3DRS \_ FOGSTART                            | 0                  |
| D3DRS \_ FOGEND                              | 1                  |
| D3DRS \_ FOGDENSITY                          | 1                  |
| D3DRS \_ ALPHABLENDENABLE                    | **FALSE**          |
| D3DRS \_ DEPTHBIAS                           | 0                  |
| D3DRS \_ STENCILENABLE                       | **FALSE**          |
| D3DRS \_ STENCILFAIL                         | D3DSTENCILOP \_ conserver |
| D3DRS \_ STENCILZFAIL                        | D3DSTENCILOP \_ conserver |
| D3DRS \_ STENCILPASS                         | D3DSTENCILOP \_ conserver |
| D3DRS \_ STENCILFUNC                         | D3DCMP \_ toujours     |
| D3DRS \_ STENCILREF                          | 0                  |
| D3DRS \_ STENCILMASK                         | égale         |
| D3DRS \_ STENCILWRITEMASK                    | égale         |
| D3DRS \_ TEXTUREFACTOR                       | égale         |
| D3DRS \_ WRAP0                               | 0                  |
| D3DRS \_ WRAP1                               | 0                  |
| D3DRS \_ WRAP2                               | 0                  |
| D3DRS \_ WRAP3                               | 0                  |
| D3DRS \_ WRAP4                               | 0                  |
| D3DRS \_ WRAP5                               | 0                  |
| D3DRS \_ WRAP6                               | 0                  |
| D3DRS \_ WRAP7                               | 0                  |
| D3DRS \_ WRAP8                               | 0                  |
| D3DRS \_ WRAP9                               | 0                  |
| D3DRS \_ WRAP10                              | 0                  |
| D3DRS \_ WRAP11                              | 0                  |
| D3DRS \_ WRAP12                              | 0                  |
| D3DRS \_ WRAP13                              | 0                  |
| D3DRS \_ WRAP14                              | 0                  |
| D3DRS \_ WRAP15                              | 0                  |
| D3DRS \_ LOCALVIEWER                         | **TRUE**           |
| D3DRS \_ EMISSIVEMATERIALSOURCE              | \_Matériau D3DMCS   |
| D3DRS \_ AMBIENTMATERIALSOURCE               | \_Matériau D3DMCS   |
| D3DRS \_ DIFFUSEMATERIALSOURCE               | D3DMCS \_ COLOR1     |
| D3DRS \_ SPECULARMATERIALSOURCE              | D3DMCS \_ COLOR2     |
| D3DRS \_ COLORWRITEENABLE                    | 0x0000000f         |
| [**D3DBLENDOP**](./d3dblendop.md)     | D3DBLENDOP \_ Ajouter    |
| D3DRS \_ SCISSORTESTENABLE                   | **FALSE**          |
| D3DRS \_ SLOPESCALEDEPTHBIAS                 | 0                  |
| D3DRS \_ ANTIALIASEDLINEENABLE               | **FALSE**          |
| D3DRS \_ TWOSIDEDSTENCILMODE                 | **FALSE**          |
| D3DRS \_ CCW \_ STENCILFAIL                    | D3DSTENCILOP \_ conserver |
| D3DRS \_ CCW \_ STENCILZFAIL                   | D3DSTENCILOP \_ conserver |
| D3DRS \_ CCW \_ STENCILPASS                    | D3DSTENCILOP \_ conserver |
| D3DRS \_ CCW \_ STENCILFUNC                    | D3DCMP \_ toujours     |
| D3DRS \_ COLORWRITEENABLE1                   | 0x0000000f         |
| D3DRS \_ COLORWRITEENABLE2                   | 0x0000000f         |
| D3DRS \_ COLORWRITEENABLE3                   | 0x0000000f         |
| D3DRS \_ BLENDFACTOR                         | égale         |
| D3DRS \_ SRGBWRITEENABLE                     | 0                  |
| D3DRS \_ SEPARATEALPHABLENDENABLE            | **FALSE**          |
| D3DRS \_ SRCBLENDALPHA                       | D3DBLEND \_ un      |
| D3DRS \_ DESTBLENDALPHA                      | D3DBLEND \_ zéro     |
| D3DRS \_ BLENDOPALPHA                        | D3DBLENDOP \_ Ajouter    |



 

## <a name="pixel-pipeline-sampler-state"></a>Pipeline de pixels : état de l’échantillonneur

Les États de l’échantillonneur contrôlent les rubriques connexes relatives à l’échantillonnage, telles que le filtrage, la mosaïque et les modes d’adresse des coordonnées de texture. Utilisez [**IDirect3DDevice9 :: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) pour configurer l’état de l’échantillonneur (y compris celui utilisé dans l’unité du paveur pour échantillonner les mappages de déplacement). Les États de l’échantillonneur ont été renommés avec un \_ préfixe « D3DSAMP » pour permettre la détection des erreurs au moment de la compilation lors du Portage à partir de DirectX 8.

Le tableau suivant répertorie tous les États de l’échantillonneur qui configurent l’état des pixels :



| États de l’échantillonneur         | Valeur par défaut     |
|------------------------|-------------------|
| \_Adresse D3DSAMP      | \_Retour à la ligne D3DTADDRESS |
| D3DSAMP \_ ADDRESSV      | \_Retour à la ligne D3DTADDRESS |
| D3DSAMP \_ ADDRESSW      | \_Retour à la ligne D3DTADDRESS |
| D3DSAMP \_ BORDERCOLOR   | 0x00000000        |
| D3DSAMP \_ MAGFILTER     | \_Point D3DTEXF    |
| D3DSAMP \_ MINFILTER     | \_Point D3DTEXF    |
| D3DSAMP \_ MIPFILTER     | D3DTEXF \_ aucun     |
| D3DSAMP \_ MIPMAPLODBIAS | 0                 |
| D3DSAMP \_ MAXMIPLEVEL   | 0                 |
| D3DSAMP \_ MAXANISOTROPY | 1                 |
| D3DSAMP \_ SRGBTEXTURE   | 0                 |
| D3DSAMP \_ ELEMENTINDEX  | 0                 |



 

## <a name="pixel-pipeline-texture-state"></a>Pipeline de pixels : état de la texture

Les États de texture contrôlent les opérations de fusion de texture du mélangeur à textures multiples. Utilisez [**IDirect3DDevice9 :: SetTextureStageState**](/windows/desktop/api) pour configurer les États des étapes de texture. Utilisez [**IDirect3DDevice9 :: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) pour associer une texture à une étape d’échantillonnage.

Le tableau suivant répertorie tous les États de texture qui configurent l’état des pixels :



| États de la texture                | Valeur par défaut    |
|-------------------------------|------------------|
| D3DTSS \_ COLOROP               | Désactivation de D3DTOP \_  |
| D3DTSS \_ COLORARG1             | \_Texture D3DTA   |
| D3DTSS \_ COLORARG2             | D3DTA \_ actuel   |
| D3DTSS \_ ALPHAOP               | Désactivation de D3DTOP \_  |
| D3DTSS \_ ALPHAARG1             | \_Texture D3DTA   |
| D3DTSS \_ ALPHAARG2             | D3DTA \_ actuel   |
| D3DTSS \_ BUMPENVMAT00          | 0                |
| D3DTSS \_ BUMPENVMAT01          | 0                |
| D3DTSS \_ BUMPENVMAT10          | 0                |
| D3DTSS \_ BUMPENVMAT11          | 0                |
| D3DTSS \_ TEXCOORDINDEX         | 0                |
| D3DTSS \_ BUMPENVLSCALE         | 0                |
| D3DTSS \_ BUMPENVLOFFSET        | 0                |
| D3DTSS \_ TEXTURETRANSFORMFLAGS | Désactivation de D3DTTFF \_ |
| D3DTSS \_ COLORARG0             | D3DTA \_ actuel   |
| D3DTSS \_ ALPHAARG0             | D3DTA \_ actuel   |
| D3DTSS \_ RESULTARG             | D3DTA \_ actuel   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[État de l’enregistrement et de la restauration des blocs d’État](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 

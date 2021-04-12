---
title: Définir l’état de l’appareil sur la fonction fixe, pipelines de nuanceur
description: Cette section présente les principales différences entre la définition de l’état de l’appareil avec le pipeline de nuanceur programmable et de fonction fixe.
ms.assetid: FF0F2A97-F75A-4AF0-8F5A-EA687523E753
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2d5c0e0ba9e1ac890468654d348b0f8b316f64
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200847"
---
# <a name="set-device-state-on-fixed-function-shader-pipelines"></a>Définir l’état de l’appareil sur la fonction fixe, pipelines de nuanceur

Cette section présente les principales différences entre la définition de l’état de l’appareil avec le pipeline de nuanceur programmable et de fonction fixe.

Voici les États des appareils que vous pouvez définir pour un pipeline à fonction fixe :

-   Transformation et éclairage de fonction fixe : [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) avec D3DRS \_ SHADEMODE, D3DRS \_ SpecularEnable, D3DRS \_ Lighting, D3DRS ambiant, D3DRS \_ \_ COLORVERTEX, D3DRS \_ LOCALVIEWER, D3DRS \_ NORMALIZENORMALS, D3DRS \_ DIFFUSEMATERIALSOURCE, D3DRS \_ SPECULARMATERIALSOURCE, D3DRS \_ AMBIENTMATERIALSOURCE, D3DRS \_ EMISSIVEMATERIALSOURCE, D3DRS \_ VERTEXBLEND, D3DRS \_ INDEXEDVERTEXBLENDENABLE, D3DRS \_ TWEENFACTOR, [**IDirect3DDevice9 :: Eclaircir**](/windows/desktop/api), [**IDirect3DDevice9 :**](/windows/desktop/api) [](/windows/desktop/api) [](/windows/desktop/api) [](/windows/desktop/api) [](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) : MultiplyTransform, IDirect3DDevice9 :: SetFVF, IDirect3DDevice9 :: SetLight, IDirect3DDevice9 :: SetMaterial, IDirect3DDevice9 :: setTransform
-   Pixel-nuanceur de pixels de fonction fixe : [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) avec D3DRS \_ TEXTUREFACTOR, [**IDirect3DDevice9 :: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)
-   Brouillard : [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) avec D3DRS \_ FOGENABLE, D3DRS \_ FOGCOLOR, D3DRS \_ FOGTABLEMODE, D3DRS \_ FOGSTART, D3DRS \_ FOGEND, D3DRS \_ FOGDENSITY, D3DRS \_ RANGEFOGENABLE, D3DRS \_ FOGVERTEXMODE

Voici les États du rendu de l’appareil que vous pouvez définir avec [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) pour les pipelines de nuanceur programmable et de fonction fixe :

-   État de la cible de rendu : D3DRS \_ COLORWRITEENABLE, D3DRS \_ COLORWRITEENABLE1, D3DRS \_ COLORWRITEENABLE2, D3DRS \_ COLORWRITEENABLE3, D3DRS \_ SRGBWRITEENABLE
-   État de profondeur : D3DRS \_ ZENABLE, D3DRS \_ ZWRITEENABLE, D3DRS \_ ZFUNC, D3DRS \_ SLOPESCALEDEPTHBIAS, D3DRS \_ DEPTHBIAS
-   État du stencil : D3DRS \_ STENCILENABLE, D3DRS \_ STENCILFAIL, D3DRS \_ STENCILZFAIL, D3DRS \_ STENCILPASS, D3DRS \_ STENCILFUNC, D3DRS \_ STENCILREF, D3DRS \_ STENCILMASK, D3DRS \_ STENCILWRITEMASK, D3DRS \_ TWOSIDEDSTENCILMODE, D3DRS \_ CCW STENCILFAIL, D3DRS \_ \_ \_ \_ \_ \_ \_ CCW STENCILZFAIL, D3DRS CCW STENCILPASS, D3DRS CCW STENCILFUNC
-   Fusion alpha : D3DRS \_ SRCBLEND, D3DRS \_ DESTBLEND, D3DRS \_ BLENDOP, D3DRS \_ BLENDFACTOR, D3DRS \_ SEPARATEALPHABLENDENABLE, D3DRS \_ SRCBLENDALPHA, D3DRS \_ DESTBLENDALPHA, D3DRS \_ BLENDOPALPHA
-   Test alpha : D3DRS \_ ALPHATESTENABLE, D3DRS \_ ALPHAREF, D3DRS \_ ALPHAFUNC
-   État du rastériseur : D3DRS \_ FillMode, D3DRS \_ LASTPIXEL, D3DRS \_ DITHERENABLE (surfaces 16 bits)
-   Élimination : D3DRS \_ CULLMODE
-   Découpage : \_ découpage D3DRS, D3DRS \_ CLIPPLANEENABLE
-   Ciseaux : D3DRS \_ SCISSORTESTENABLE
-   Échantillonneurs de texture : D3DRS \_ WRAP0, D3DRS \_ WRAP1, D3DRS \_ WRAP2, D3DRS \_ WRAP3, D3DRS \_ WRAP4, D3DRS \_ WRAP5, D3DRS \_ WRAP6, D3DRS \_ WRAP7, D3DRS \_ WRAP8, D3DRS \_ WRAP9, D3DRS \_ WRAP10, D3DRS \_ WRAP11, D3DRS \_ WRAP12, D3DRS \_ WRAP13, D3DRS \_ WRAP14, D3DRS \_ WRAP15
-   Anticrénelage : D3DRS \_ MULTISAMPLEANTIALIAS, D3DRS \_ MULTISAMPLEMASK, D3DRS \_ ANTIALIASEDLINEENABLE
-   Point sprites : D3DRS \_ , D3DRS, D3DRS, \_ POINTSPRITEENABLE, D3DRS, MAXD3DRS, POINTSCALEENABLE D3DRS, POINTSCALE D3DRS \_ \_ A, POINTSCALE D3DRS \_ \_ \_ \_ \_ \_ \_ B, POINTSCALE \_ \_ C
-   N-patches : D3DRS \_ PATCHEDGESTYLE, D3DRS \_ POSITIONDEGREE, D3DRS \_ NORMALDEGREE, D3DRS \_ MINTESSELLATIONLEVEL, D3DRS \_ MAXTESSELLATIONLEVEL, D3DRS \_ ADAPTIVETESS \_ X, D3DRS \_ ADAPTIVETESS \_ Y, D3DRS \_ ADAPTIVETESS \_ Z, D3DRS \_ ADAPTIVETESS \_ W, D3DRS \_ ENABLEADAPTIVETESSELLATION

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rubriques avancées](advanced-topics.md)
</dt> </dl>

 

 

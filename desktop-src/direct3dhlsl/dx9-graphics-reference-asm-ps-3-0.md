---
title: ps_3_0
description: En savoir plus sur ps_3_0, un nuanceur de pixels programmable, qui est constitué d’un ensemble d’instructions qui s’appliquent aux données de pixels.
ms.assetid: 3eabf173-9d9d-45b2-bc30-de857428f3ee
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 19587cbaa79e2b89633560a7b7889219172d0c25
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010862"
---
# <a name="ps_3_0"></a>PS \_ 3 \_ 0

Un nuanceur de pixels programmable est constitué d’un ensemble d’instructions qui fonctionnent sur des données de pixels. Enregistre les données de transfert dans et en dehors de l’ALU. Un contrôle supplémentaire peut être appliqué pour modifier l’instruction, les résultats ou les données qui sont écrites.

-   [les \_ instructions PS 3 \_ 0](dx9-graphics-reference-asm-ps-instructions-ps-3-0.md) contiennent une liste des instructions disponibles.
-   [ \_ registres PS 3 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) répertorie les différents types de registres utilisés par le nuanceur de pixels alu.
-   [Modificateurs](dx9-graphics-reference-asm-ps-registers-modifiers.md) Sont utilisées pour modifier le mode de fonctionnement d’une instruction.
-   Le [masque d’écriture de registre de destination](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) détermine les composants du registre de destination qui sont écrits.
-   Les [modificateurs de Registre source du nuanceur de pixels](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) modifient les données du Registre source avant l’exécution de l’instruction.
-   Le [Registre source Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) offre un contrôle supplémentaire sur les composants Register qui sont lus, copiés ou écrits.

## <a name="new-features"></a>Nouvelles fonctionnalités

Ajoutez un registre facial. Ajoutez un registre de position. Les registres de couleurs (v \# ) sont désormais à virgule flottante intégrale et les registres de coordonnées de texture (t \# ) ont été consolidés. Les déclarations d’entrée prennent les noms d’utilisation, et plusieurs utilisations sont autorisées pour les composants d’un registre donné.

## <a name="dynamic-flow-control"></a>Contrôle de Flow dynamique

L’appareil prend en charge le contrôle de Flow dynamique ([si bool-PS](if-bool---ps.md), [break-PS](break---ps.md)et [break \_ COMP-PS](break-comp---ps.md)). Profondeur d’imbrication de plages comprise entre 0 et 24.

## <a name="number-of-temporary-registers"></a>Nombre de registres temporaires

Le nombre de registres temporaires pris en charge est de 32.

## <a name="static-flow-control-nesting-depth"></a>Profondeur d’imbrication du contrôle de Flow statique

L’appel de [PS](call---ps.md) / [callnz](callnz-bool---ps.md)prévu  / peut être imbriqué sur une profondeur maximale de 4.[ \_ ](callnz-pred---ps.md) Indépendamment, [les instructions Loop-](loop---ps.md)PS / [REP-PS](rep---ps.md) peuvent être imbriquées à une profondeur maximale de 4.

## <a name="arbitrary-swizzle"></a>Swizzle arbitraire

Swizzle arbitraire est pris en charge. Consultez [Registre source Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).

## <a name="gradient-instructions"></a>Instructions de dégradé

Les instructions de dégradé sont prises en charge. Consultez [DSX-PS](dsx---ps.md), [DSY-PS](dsy---ps.md)et [texldd-PS](texldd---ps.md).

## <a name="predication"></a>Prédicat

Le prédicat d’instruction est pris en charge. Consultez [Registre de prédicat](dx9-graphics-reference-asm-ps-registers-predicate.md).

## <a name="dependent-read-limit"></a>Limite de lecture dépendante

Il n’existe aucune limite de lecture dépendante.

## <a name="texture-instruction-limit"></a>Limite de l’instruction de texture

Il n’existe aucune limite sur les instructions de texture.

## <a name="instruction-count"></a>Nombre d’instructions

Chaque nuanceur de pixels est autorisé à partir de 512 jusqu’au nombre d’emplacements dans MaxPixelShader30InstructionSlots (pas plus de 32768). Le nombre d’instructions exécutées peut être bien plus élevé en raison de la prise en charge des boucles. MaxPShaderInstructionsExecuted doit être au moins égale à 2 ^ 16.

## <a name="sampler-count"></a>Nombre d’échantillonneurs

Le nombre d’échantillonneurs de texture disponibles est 16.

## <a name="device-caps"></a>Cap de l’appareil

Si PS \_ 3 \_ 0 est pris en charge, les limites suivantes sont prises en charge dans le matériel (au minimum) :



| Encapsul                                                                                                          | Value                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MaxTextureWidth, MaxTextureHeight                                                                            | 4 Ko chacun                                                                                                                                                                                                                                                                                               |
| MaxTextureRepeat                                                                                             | 8 Ko                                                                                                                                                                                                                                                                                                    |
| MaxAnisotropy                                                                                                | 16                                                                                                                                                                                                                                                                                                    |
| PixelShaderVersion                                                                                           | 3 \_ 0                                                                                                                                                                                                                                                                                                  |
| MaxPixelShader30InstructionSlots                                                                             | 512                                                                                                                                                                                                                                                                                                   |
| Les limites primitives suivantes sont définies :                                                                        | D3DPMISCCAPS \_ BLENDOP, D3DPMISCCAPS \_ CLIPPLANESCALEDPOINTS, D3DPMISCCAPS \_ CLIPTLVERTS, D3DPMISCCAPS \_ CULLCCW, D3DPMISCCAPS \_ CULLCW, D3DPMISCCAPS \_ CULLNONE, D3DPMISCCAPS \_ FOGINFVF, D3DPMISCCAPS \_ MASKZ                                                                                               |
| Les extrémités raster suivantes sont définies :                                                                           | D3DPRASTERCAPS \_ MIPMAPLODBIAS, D3DPRASTERCAPS \_ anisotrope, D3DPRASTERCAPS \_ COLORPERSPECTIVE, D3DPRASTERCAPS \_ SCISSORTEST dans D3DCAPS9                                                                                                                                                                  |
| Prise en charge complète de l’écart de profondeur, notamment :                                                                       | D3DPRASTERCAPS \_ SLOPESCALEDEPTHBIAS, D3DPRASTERCAPS \_ DEPTHBIAS                                                                                                                                                                                                                                        |
| Ensemble complet de comparaisons pour le test de profondeur et alpha, y compris :                                                  | Toutes les D3DPCMPCAPS dans D3DCAPS9.                                                                                                                                                                                                                                                                      |
| Modes de fusion source                                                                                        | Tous les modes de fusion sont pris en charge en tant que source (à l’exception de D3DPBLENDCAPS \_ SRCALPHASAT, D3DPBLENDCAPS \_ BOTHSRCALPHA et D3DPBLENDCAPS \_ BOTHINVSRCALPHA).                                                                                                                                                    |
| Les limites de texture suivantes sont prises en charge :                                                                    | D3DPTEXTURECAPS \_ carte cubique, D3DPTEXTURECAPS \_ MIPCUBEMAP, D3DPTEXTURECAPS \_ MIPMAP, D3DPTEXTURECAPS \_ MIPVOLUMEMAP, D3DPTEXTURECAPS \_ perspective, D3DPTEXTURECAPS \_ projeté, D3DPTEXTURECAPS \_ TEXREPEATNOTSCALEDBYSIZE, D3DPTEXTURECAPS \_ VOLUMEMAP                                                        |
| Les éléments suivants sont pris en charge sur les limites de filtre de texture, les seuils de filtre de texture de volume et les filtres de texture de cube : | D3DPTFILTERCAPS \_ MINFPOINT, D3DPTFILTERCAPS \_ MINFLINEAR, D3DPTFILTERCAPS \_ MINFANISOTROPIC (cela n’est pas obligatoire pour VolumeTextureFilterCaps et CUBETEXTUREFILTERCAPS), D3DPTFILTERCAPS \_ MIPFPOINT, D3DPTFILTERCAPS \_ MIPFLINEAR, D3DPTFILTERCAPS \_ MAGFPOINT, D3DPTFILTERCAPS \_ MAGFLINEAR             |
| Les modes d’adresse de texture suivants sont pris en charge au niveau des niveaux vertex et pixel :                                | D3DPTADDRESSCAPS \_ Wrap, D3DPTADDRESSCAPS \_ Mirror, D3DPTADDRESSCAPS \_ collier, D3DPTADDRESSCAPS \_ Border, D3DPTADDRESSCAPS \_ INDEPENDENTUV, D3DPTADDRESSCAPS \_ MIRRORONCE                                                                                                                                    |
| Toutes les limites de nuanceur de pixels sont prises en charge.                                                                     | DynamicFlowControlDepth = 24, NumTemps = 32, StaticFlowControlDepth = 4, NumInstructionSlots = 512. Les fonctionnalités suivantes sont prises en charge : prédicat, Swizzles arbitraire et instructions de dégradé. Il n’existe aucune limite de lecture dépendante et aucune limite sur le mélange des instructions de texture et mathématiques. |
| Toutes les opérations de stencil sont prises en charge. Cela comprend deux stencils côte à côte.                                   | Voir [ **D3DSTENCILOP**](/windows/desktop/direct3d9/d3dstencilop)                                                                                                                                                                                                                                                        |
| Taille du point de prise en charge de périphérique par vertex                                                                         | D3DFVFCAPS \_ psize dans D3DCAPS9                                                                                                                                                                                                                                                                         |
| Prise en charge de la texture non-puissance de 2.                                                                              | Prise en charge complète ou prise en charge conditionnelle non-Pow-2 ; l’appareil ne doit pas avoir la seule limite de texture carrée que dans D3DPTEXTURECAPS \_ SQUAREONLY.                                                                                                                                                    |
| Si l’appareil prend en charge plusieurs rendertargets, les limitations suivantes sont prises en charge :                             | D3DPMISCCAPS \_ INDEPENDENTWRITEMASKS, D3DPMISCCAPS \_ MRTPOSTPIXELSHADERBLENDING                                                                                                                                                                                                                         |
| Si vs \_ 3 \_ 0 est pris en charge                                                                                     | MaxUserClipPlanes dans D3DCAPS9 est 6                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Nuanceurs de pixels](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 
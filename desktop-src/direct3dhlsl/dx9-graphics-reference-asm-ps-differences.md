---
title: Différences de nuanceur de pixels
description: Différences de nuanceur de pixels
ms.assetid: 11aefb26-eb82-486c-81ff-7c0cfbab1b7a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9a74b5cc7588220fdc5173c470f7852ee9ef763d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382143"
---
# <a name="pixel-shader-differences"></a>Différences de nuanceur de pixels

## <a name="instruction-slots"></a>Emplacements des instructions

Chaque version prend en charge un nombre différent d’emplacements d’instruction maximum.



| Version  | Nombre maximal d’emplacements d’instructions                                                                                   |
|----------|-----------------------------------------------------------------------------------------------------------------------|
| PS \_ 1 \_ 1 | 4 texture + 8 arithmétiques                                                                                              |
| PS \_ 1 \_ 2 | 4 texture + 8 arithmétiques                                                                                              |
| PS \_ 1 \_ 3 | 4 texture + 8 arithmétiques                                                                                              |
| PS \_ 1 \_ 4 | 6 texture + 8 arithmétiques par phase                                                                                    |
| PS \_ 2 \_ 0 | 32 texture + 64 arithmétique                                                                                            |
| PS \_ 2 \_ x | 96 minimum et jusqu’au nombre d’emplacements dans D3DCAPS9. D3DPSHADERCAPS2 \_ 0. NumInstructionSlots. Consultez D3DPSHADERCAPS2 \_ 0. |
| PS \_ 3 \_ 0 | 512 minimum et jusqu’au nombre d’emplacements dans D3DCAPS9. MaxPixelShader30InstructionSlots. Consultez D3DPSHADERCAPS2 \_ 0.      |



 

Pour plus d’informations sur les limitations des nuanceurs de logiciels, consultez [nuanceurs de logiciels](dx9-graphics-reference-asm-software-shaders.md).

## <a name="flow-control-nesting-limits"></a>Limites d’imbrication du contrôle de Flow

-   Consultez [limitations du contrôle de workflow](dx9-graphics-reference-asm-ps-instructions-flow-control.md).

## <a name="ps_1_x-features"></a>Fonctionnalités de PS \_ 1 \_ x

Nouvelles instructions :

Consultez les instructions PS 1 [ \_ \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md).

Nouveaux registres :

Consultez [les \_ registres PS 1 \_ 1 PS 1 \_ \_ \_ \_ 2 \_ \_ \_ \_ \_ \_ \_ \_ ](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)PS 1 3 PS 1 4.

## <a name="ps_2_0-features"></a>Fonctionnalités de PS \_ 2 \_ 0

Nouvelles fonctionnalités :

-   Trois nouveaux Swizzles-. yzxw,. zxyw,. wzyx
-   Nombre de [registres temporaires](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) passé à 12
-   Nombre de registres de [registres à virgule flottante constants](dx9-graphics-reference-asm-ps-registers-constant-float.md) (c \# ) passés à 32
-   Nombre de [registres de coordonnées de texture](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)(t \# ) augmentés à 8

Nouvelles instructions :

-   Instructions d’installation- [DCL-(SM2, SM3-PS ASM)](dcl---ps.md), [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md)
-   Instructions arithmétiques [-ABS-PS](abs---ps.md), [CRS-PS](crs---ps.md), [dp2add-PS](dp2add---ps.md), [exp-PS](exp---ps.md), [FRC-](frc---ps.md)PS [, log-PS](log---ps.md), [M3X2-PS](m3x2---ps.md), [M3x3-](m3x3---ps.md)PS [, M3x4-](m3x4---ps.md)PS, [m4x3-PS](m4x3---ps.md), [M4X4-](m4x4---ps.md)PS, [Max-](max---ps.md)PS, [min-PS](min---ps.md), [NRM](nrm---ps.md)-PS [, Pow-PS](pow---ps.md), [RCP-PS](rcp---ps.md), [rsq-](rsq---ps.md)PS, [SinCos,-PS](sincos---ps.md)
-   Instructions de texture- [texld-PS \_ 2 \_ 0 et up](texld---ps-2-0.md) (syntaxe différente), [texldb-PS](texldb---ps.md), [texldp-PS](texldp---ps.md)

Nouveaux registres :

-   [Échantillonneur (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \# )

## <a name="ps_2_x-features"></a>Fonctionnalités de PS \_ 2 \_ x

Nouvelles fonctionnalités (voir [**D3DPSHADERCAPS2 \_ 0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0).) :

-   Contrôle de Flow dynamique
-   Contrôle de Flow statique
-   Imbrication des instructions de contrôle de workflow dynamique et statique
-   Nombre d' [enregistreurs temporaires](dx9-graphics-reference-asm-ps-registers-temporary.md)(r \# ) augmentés
-   Swizzle source arbitraire
-   Instructions de dégradé
-   Prédicat
-   Aucune limite de lecture de texture dépendante
-   Aucune limite d’instruction de texture

Nouvelles instructions :

-   Instructions de contrôle de Flow statique- [si bool-PS](if-bool---ps.md), [Call-PS](call---ps.md), [callnz bool-PS](callnz-bool---ps.md), [else-PS](else---ps.md), [endif-PS](endif---ps.md), [REP-PS](rep---ps.md), [endrep-PS](endrep---ps.md), [label-PS](label---ps.md), [RET-PS](ret---ps.md)
-   Instructions de contrôle de workflow dynamique- [break-PS](break---ps.md), [break \_ COMP-PS](break-comp---ps.md), [breakp-PS](break-p---ps.md), [callnz prédit-PS](callnz-pred---ps.md), [si \_ COMP-PS](if-comp---ps.md), [si prédit-PS](if-pred---ps.md), [setp \_ COMP-PS](setp-comp---ps.md)
-   Instructions arithmétiques- [DSX-PS](dsx---ps.md), [DSY-PS](dsy---ps.md)
-   Instruction de texture- [texldd-PS](texldd---ps.md)

Nouveaux registres :

-   [Registre de prédicats](dx9-graphics-reference-asm-ps-registers-predicate.md) (P0)

## <a name="ps_3_0-features"></a>Fonctionnalités de PS \_ 3 \_ 0

Nouvelles fonctionnalités :

-   10 [registres d’entrée](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)consolidés s (v \# )
-   Registre de [couleur d’entrée](dx9-graphics-reference-asm-ps-registers-input-color.md) indexable (v \# ) avec le [Registre de compteur de boucle](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (Al)
-   Nombre de [registres temporaires](dx9-graphics-reference-asm-ps-registers-temporary.md)s (r \# ) augmentés à 32
-   Nombre de [registres de type flottant](dx9-graphics-reference-asm-ps-registers-constant-float.md)s (c \# ) augmentés à 224

Nouvelles instructions :

-   Instruction de configuration [- \_ sémantique DCL (SM3-PS ASM)](dcl-usage---ps.md)
-   Instructions de Flow statique- [Loop-PS](loop---ps.md), [ENDLOOP-PS](endloop---ps.md)
-   Instruction arithmétique- [SinCos,-PS](sincos---ps.md) (nouvelle syntaxe)
-   Instruction de texture- [texldl-PS](texldl---ps.md)

Nouveaux registres :

-   [Registre d’entrée](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v \# )
-   [Registre de position](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vPOS)
-   [Inscription faciale](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vFace)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Nuanceurs de pixels](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 
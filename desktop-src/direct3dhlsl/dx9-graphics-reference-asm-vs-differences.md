---
title: Différences entre vertex shader
description: Différences entre vertex shader
ms.assetid: 94fe4033-94c0-4561-b0fd-1fb85d8f796b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1c74603f9eab4ea91e9220bbaa172c0262aeda99
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031371"
---
# <a name="vertex-shader-differences"></a>Différences entre vertex shader

## <a name="instruction-slots"></a>Emplacements des instructions

Chaque version prend en charge un nombre différent d’emplacements d’instruction maximum.



| Version  | Nombre maximal d’emplacements d’instructions                                                                                               |
|----------|-----------------------------------------------------------------------------------------------------------------------------------|
| vs \_ 1 \_ 1 | 128                                                                                                                               |
| vs \_ 2 \_ 0 | 256                                                                                                                               |
| vs \_ 2 \_ x | 256                                                                                                                               |
| vs \_ 3 \_ 0 | 512 minimum et jusqu’au nombre d’emplacements dans D3DCAPS9. MaxVertexShader30InstructionSlots. Consultez [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9). |



 

Pour plus d’informations sur les limitations des nuanceurs de logiciels, consultez [nuanceurs de logiciels](dx9-graphics-reference-asm-software-shaders.md).

## <a name="flow-control-nesting-limits"></a>Limites d’imbrication du contrôle de Flow

-   Consultez [limites d’imbrication des contrôles de Flow](dx9-graphics-reference-asm-vs-instructions-flow-control.md).

## <a name="vs_1_1-features"></a>\_fonctionnalités vs 1 \_ 1

Nouvelles instructions :

Voir [instructions-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-instructions-vs-1-1.md).

Nouveaux registres :

Consultez [registres-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md).

## <a name="vs_2_0-features"></a>\_fonctionnalités vs 2 \_ 0

Nouvelles fonctionnalités :

-   Contrôle de Flow statique
-   Les quatre composants du [Registre d’adresses](dx9-graphics-reference-asm-vs-registers-address.md) (a0) sont disponibles.

Nouvelles instructions :

-   Instructions d’installation- [defb-vs](defb---vs.md), [assignatures-vs](defi---vs.md)
-   Instructions arithmétiques- [ABS-vs](abs---vs.md), [CRS-vs](crs---vs.md), [LRP-vs](lrp---vs.md), [Mova-](mova---vs.md)vs, [NRM-vs](nrm---vs.md), [Pow-](pow---vs.md)vs, [SGN-vs](sgn---vs.md), [SinCos,-vs](sincos---vs.md)
-   Instructions de contrôle de workflow statiques- [appel-vs](call---vs.md), [callnz bool-vs](callnz-bool---vs.md), [else-vs](else---vs.md), [endif-vs](endif---vs.md), [ENDLOOP-vs](endloop---vs.md), [endrep-vs](endrep---vs.md), [si bool-vs](if-bool---vs.md), [label-vs](label---vs.md), [Loop](loop---vs.md)-vs, [REP](rep---vs.md)-vs, [RET-vs](ret---vs.md)

Nouveaux registres :

-   [Registre booléen constant](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) (b \# )
-   [Registre d’entiers constant](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (i \# )
-   [Registre de compteur de boucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al)

## <a name="vs_2_x-features"></a>Fonctionnalités de vs \_ 2 \_ x

Nouvelles fonctionnalités (D3DCAPS9. VS20Caps):

-   Contrôle de Flow dynamique
-   Imbrication des instructions de contrôle de workflow dynamique et statique
-   Nombre d' [enregistreurs temporaires](dx9-graphics-reference-asm-vs-registers-temporary.md)(r \# ) augmentés
-   Prédicat

Nouvelles instructions :

-   Instructions de contrôle de workflow dynamique- [break-vs](break---vs.md), [pause \_ COMP-vs](break-comp---vs.md), [breakp-vs](breakp---vs.md), [callnz prédit-vs](callnz-pred---vs.md), [si \_ COMP-vs](if-comp---vs.md), [si prédit-vs](if-pred---vs.md), [setp \_ COMP-vs](setp-comp---vs.md)

Nouveaux registres :

-   [Registre de prédicats](dx9-graphics-reference-asm-vs-registers-predicate.md) (P0)

## <a name="vs_3_0-features"></a>Fonctionnalités de vs \_ 3 \_ 0

Nouvelles fonctionnalités :

-   Recherche de texture
-   Registres de [sortie](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) indexables (o \# )
-   Nombre de [registres temporaires](dx9-graphics-reference-asm-vs-registers-temporary.md)s (r \# ) augmentés à 32

Nouvelles instructions :

-   Instruction de configuration- [DCL \_ samplerType (SM3-vs ASM)](dcl-samplertype---vs.md)
-   Instruction de texture- [texldl-vs](texldl---vs.md)

Nouveaux registres :

-   [Échantillonneur (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) (s \# )

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Nuanceurs vertex](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 
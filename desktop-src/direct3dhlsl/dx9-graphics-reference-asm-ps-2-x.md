---
title: ps_2_x
description: En savoir plus sur ps_2_x, un nuanceur de pixels programmable, qui est constitué d’un ensemble d’instructions qui s’appliquent aux données de pixels.
ms.assetid: 06f657a9-6521-404e-b012-7c8e972e9d5c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9efedc6011cb63b6465fd2d3ced4a7807c09f4da
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524589"
---
# <a name="ps_2_x"></a>PS \_ 2 \_ x

Un nuanceur de pixels programmable est constitué d’un ensemble d’instructions qui fonctionnent sur des données de pixels. Enregistre les données de transfert dans et en dehors de l’ALU. Un contrôle supplémentaire peut être appliqué pour modifier l’instruction, les résultats ou les données qui sont écrites.

-   [les \_ instructions PS 2 \_ x](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) contiennent une liste des instructions disponibles.
-   [ \_ registres PS 2 \_ x](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) répertorie les différents types de registres utilisés par le nuanceur de sommets alu.
-   [Modificateurs](dx9-graphics-reference-asm-ps-registers-modifiers.md) Sont utilisées pour modifier le mode de fonctionnement d’une instruction.
-   Le [masque d’écriture de registre de destination](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) détermine les composants du registre de destination qui sont écrits.
-   Les [modificateurs de Registre source du nuanceur de pixels](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) modifient les données du Registre source avant l’exécution de l’instruction.
-   Le [Registre source Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) offre un contrôle supplémentaire sur les composants Register qui sont lus, copiés ou écrits.

## <a name="dynamic-flow-control"></a>contrôle de Flow dynamique

[**DynamicFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) représente la profondeur d’imbrication des instructions de contrôle de Flow [](if-bool---ps.md)dynamique : [si \_ COMP](if-comp---ps.md), [si \_ prédit](if-pred---ps.md), [break-PS](break---ps.md)et [break \_ COMP-PS](break-comp---ps.md). La valeur est égale à la profondeur d’imbrication du bloc if \_ COMP. Si cette limite est égale à zéro, l’appareil ne prend pas en charge les instructions de contrôle de Flow dynamique.

## <a name="number-of-temporary-registers"></a>Nombre de registres temporaires

Nombre de registres temporaires pris en charge par l’appareil. La plage est comprise entre 12 et 32.

## <a name="static-flow-control-nesting-depth"></a>profondeur d’imbrication des contrôles de Flow statique

[**StaticFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) représente la profondeur d’imbrication de deux types d’instructions de contrôle de Flow statique : le REP de [boucle](loop---ps.md)  / [](rep---ps.md) et l' [appel](call---ps.md)de  / [callnz](callnz-bool---ps.md). les instructions Loop/REP peuvent être imbriquées jusqu’à **StaticFlowControlDepth** Deep. De manière indépendante, les instructions/callnz peuvent être imbriquées jusqu’à **StaticFlowControlDepth** Deep.

## <a name="number-of-instruction-slots"></a>Nombre d’emplacements d’instructions

Le nombre d’emplacements d’instruction peut être compris entre 96 et 512, et est spécifié par [**MaxPixelShaderInstructionSlots**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0). Le nombre total d’instructions pouvant être exécutées est défini par **MaxPixelShaderInstructionsExecuted**. Cette valeur peut être supérieure au nombre d’emplacements d’instruction en raison des appels de boucle et de sous-routine.

## <a name="arbitrary-swizzle"></a>Swizzle arbitraire

Si [**D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWIZZLE**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) est défini, le Swizzle arbitraire est pris en charge. Consultez [Registre source Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).

## <a name="gradient-instructions"></a>Instructions de dégradé

Si [**D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) est défini, les instructions de dégradé sont prises en charge. Consultez [DSX-PS](dsx---ps.md), [DSY-PS](dsy---ps.md)et [texldd-PS](texldd---ps.md).

## <a name="predication"></a>Prédicat

Si [**le \_ \_ prédicat D3DD3DPSHADERCAPS2 0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) est défini, la prédicat d’instruction est pris en charge. Consultez [Registre de prédicat](dx9-graphics-reference-asm-ps-registers-predicate.md).

## <a name="dependent-read-limit"></a>Limite de lecture dépendante

Si [**D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) est défini, aucune limite de lecture n’est dépendante.

## <a name="texture-instruction-limit"></a>Limite de l’instruction de texture

Si [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) est défini, aucune limite n’est imposée sur les instructions de texture.

## <a name="sampler-count"></a>Nombre d’échantillonneurs

Le nombre d’échantillonneurs de texture disponibles est 16.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Nuanceurs de pixels](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 
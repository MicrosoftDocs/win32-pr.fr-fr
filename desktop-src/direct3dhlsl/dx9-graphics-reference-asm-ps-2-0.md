---
title: ps_2_0
description: Un nuanceur de pixels programmable est constitué d’un ensemble d’instructions qui fonctionnent sur des données de pixels. Enregistre les données de transfert dans et en dehors de l’ALU. Un contrôle supplémentaire peut être appliqué pour modifier l’instruction, les résultats ou les données qui sont écrites.
ms.assetid: 15f2e4a4-9c39-434b-bea7-5d2d31cae1d9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 98b0f252d87a1f7e08c3531415d7ebcb93d4f6f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104971326"
---
# <a name="ps_2_0"></a>PS \_ 2 \_ 0

Un nuanceur de pixels programmable est constitué d’un ensemble d’instructions qui fonctionnent sur des données de pixels. Enregistre les données de transfert dans et en dehors de l’ALU. Un contrôle supplémentaire peut être appliqué pour modifier l’instruction, les résultats ou les données qui sont écrites.

-   [les \_ instructions PS 2 \_ 0](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) contiennent une liste des instructions disponibles.
-   [ \_ registres PS 2 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) répertorie les différents types de registres utilisés par le nuanceur de sommets alu.
-   [Modificateurs](dx9-graphics-reference-asm-ps-registers-modifiers.md) Sont utilisées pour modifier le mode de fonctionnement d’une instruction.
-   Le [masque d’écriture de registre de destination](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) détermine les composants du registre de destination qui sont écrits.
-   Les [modificateurs de Registre source du nuanceur de pixels](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) modifient les données du Registre source avant l’exécution de l’instruction.
-   Le [Registre source Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) offre un contrôle supplémentaire sur les composants Register qui sont lus, copiés ou écrits.

## <a name="instruction-count"></a>Nombre d’instructions

Les nuanceurs présentent des restrictions pour le nombre maximal d’instructions. Nombre total d’emplacements d’instructions : 96 (64 arithmétique et 32 texture).

## <a name="sampler-count"></a>Nombre d’échantillonneurs

Le nombre d’échantillonneurs de texture disponibles est 16.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Nuanceurs de pixels](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 





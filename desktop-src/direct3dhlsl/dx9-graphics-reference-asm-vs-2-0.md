---
title: vs_2_0
description: Un nuanceur de sommet programmable est constitué d’un ensemble d’instructions qui fonctionnent sur des données de vertex. Enregistre les données de transfert dans et en dehors de l’ALU. Un contrôle supplémentaire peut être appliqué pour modifier l’instruction, les résultats ou les données qui sont écrites.
ms.assetid: 6e38c138-5f9c-40a6-9fe2-a93471c3c573
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce4e986e610ff95716cd6899d6167e4f69efe042
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104971446"
---
# <a name="vs_2_0"></a>vs \_ 2 \_ 0

Un nuanceur de sommet programmable est constitué d’un ensemble d’instructions qui fonctionnent sur des données de vertex. Enregistre les données de transfert dans et en dehors de l’ALU. Un contrôle supplémentaire peut être appliqué pour modifier l’instruction, les résultats ou les données qui sont écrites.

-   [Instructions-vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) contient une liste des instructions disponibles.
-   [Registres-vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) répertorie les différents types de registres utilisés par le nuanceur de sommets alu.
-   Les [modificateurs de Registre du nuanceur de sommets](dx9-graphics-reference-asm-vs-registers-modifiers.md) permettent de modifier la façon dont une instruction fonctionne.
-   Les [modificateurs de Registre source du nuanceur de sommets](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) modifient les données du Registre source avant l’exécution de l’instruction.
-   Le [Registre source Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) offre un contrôle supplémentaire sur les composants Register qui sont lus, copiés ou écrits.
-   Le [masquage du registre de destination](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) détermine les composants du registre de destination qui sont écrits.

## <a name="instruction-count"></a>Nombre d’instructions

Chaque nuanceur de sommets peut avoir jusqu’à 256 instructions stockées. Le nombre d’instructions exécutées peut être bien plus élevé (en raison de la prise en charge de la boucle/REP) et est limité par D3DCAPS9. MaxVShaderInstructionsExecuted, qui doit être au moins 0xFFFF.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Nuanceurs vertex](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 





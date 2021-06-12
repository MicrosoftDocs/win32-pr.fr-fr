---
title: ps_2_0
description: En savoir plus sur ps_2_0, un nuanceur de pixels programmable, qui est constitué d’un ensemble d’instructions qui s’appliquent aux données de pixels.
ms.assetid: 15f2e4a4-9c39-434b-bea7-5d2d31cae1d9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a2433c8490af06d23d8dccef676ec206fdbb88c0
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010982"
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

 

 





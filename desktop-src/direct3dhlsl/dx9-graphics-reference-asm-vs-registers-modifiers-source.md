---
title: Modificateurs de Registre source du nuanceur de sommets
description: Les modificateurs sources peuvent être appliqués pour modifier les données lues à partir d’un registre source avant que les données ne soient utilisées par l’instruction.
ms.assetid: 516ff7ca-0071-44ac-a246-612a9faa7e7b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49c663741da50620e03cfde9f13d67a0c0063453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380152"
---
# <a name="vertex-shader-source-register-modifiers"></a>Modificateurs de Registre source du nuanceur de sommets

Les modificateurs sources peuvent être appliqués pour modifier les données lues à partir d’un registre source avant que les données ne soient utilisées par l’instruction.

## <a name="negate"></a>Negate

Nie le contenu du Registre source.



| Modificateur de composant | Description     |
|--------------------|-----------------|
| \- r               | Négation source |



 

Le modificateur de négation ne peut pas être utilisé dans le deuxième Registre source de ces instructions : [M3X2-vs](m3x2---vs.md), [M3x3-vs](m3x3---vs.md), [M3x4-vs](m3x4---vs.md), [m4x3-vs](m4x3---vs.md), [M4X4-vs](m4x4---vs.md).



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| \-                     | x    | x    | x    | x     | x    | x     |



 

## <a name="absolute-value"></a>Valeur absolue

Prenez la valeur absolue du Registre.



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| abs                    |      |      |      |       | x    | x     |



 

Si un nuanceur de version 3 lit à partir d’un ou de plusieurs registres à virgule flottante constants (c \# ), l’une des conditions suivantes doit être vraie.

-   Tous les registres à virgule flottante constantes doivent utiliser le modificateur ABS.
-   Aucun des registres à virgule flottante constantes ne peut utiliser le modificateur ABS.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modificateurs de registre de nuanceur vertex](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 





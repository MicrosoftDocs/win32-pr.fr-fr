---
title: boucle-vs
description: Démarrer une boucle... bloc ENDLOOP.
ms.assetid: vs|directx_sdk|~\loop___vs.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6a96a1ce53b850ec8feeba282055e8111b275bfd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990777"
---
# <a name="loop---vs"></a>boucle-vs

Démarrer une boucle... bloc [ENDLOOP](endloop---vs.md) .

## <a name="syntax"></a>Syntaxe



| boucle aL, i\# |
|--------------|



 

Où :

-   aL est le [Registre de compteur de boucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md) contenant le nombre de boucles actuel.
-   Je suis \# un [Registre d’entiers constant](dx9-graphics-reference-asm-vs-registers-constant-integer.md). Consultez la section Remarques.

## <a name="remarks"></a>Notes



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| loop                   |      | x    | x    | x     | x    | x     |



 

-   Le [Registre de compteur de boucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al) contient le nombre de boucles actuel et peut être utilisé pour l’adressage relatif dans un [Registre d’entiers constant](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (c \# ) ou des registres de [sortie](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o \# ) à l’intérieur du bloc de boucle.
-   i \# . x spécifie le nombre d’itérations. La plage autorisée est \[ 0, 255 \] . Notez que cette instruction n’incrémente pas ou ne décrémente pas la valeur de i \# . x.
-   i \# . y spécifie la valeur initiale du Registre du compteur de la [boucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al). La plage autorisée est \[ 0, 255 \] . Notez que cette instruction n’incrémente pas ou ne décrémente pas la valeur de i \# . y.
-   i \# . z spécifie la taille de l’étape/du Stride. La plage autorisée est \[ -128, 127 \] .
-   i \# . w n’est pas utilisé et doit être défini sur 0.
-   Les blocs de boucle peuvent être imbriqués. Consultez [limites d’imbrication des contrôles de Flow](dx9-graphics-reference-asm-vs-instructions-flow-control.md).
-   Lorsqu’elle est imbriquée, la valeur du [Registre de compteur de boucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al) fait référence au bloc de boucle englobant immédiatement.
-   Les blocs de boucle sont autorisés à se trouver complètement à l’intérieur d’un bloc if ou à l' \* entourer complètement. Aucun chevauchement n’est autorisé.

## <a name="example"></a>Exemple


```
loop aL, i3
    add r1, r0, c2[aL]
endloop
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





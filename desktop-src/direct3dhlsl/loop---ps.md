---
title: boucle-PS
description: Démarre une boucle... bloc ENDLOOP-PS.
ms.assetid: vs|directx_sdk|~\loop___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a08d2954b478bd6afd0c52d517e07a82ba3ee148dd07f839ec7d8787d93c2134
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510982"
---
# <a name="loop---ps"></a>boucle-PS

Démarre une boucle... bloc [ENDLOOP-PS](endloop---ps.md) .

## <a name="syntax"></a>Syntaxe



| boucle aL, i\# |
|--------------|



 

Où :

-   aL est le [Registre de compteur de boucle](dx9-graphics-reference-asm-ps-registers-loop-counter.md) contenant le nombre de boucles actuel.
-   Je suis \# un [Registre d’entiers constant](dx9-graphics-reference-asm-ps-registers-constant-integer.md). Consultez la section Remarques.

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| loop                  |      |      |      |      |      |      |       | x    | x     |



 

-   Le [Registre de compteurs de boucles](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (Al) contient le nombre de boucles actuel et peut être utilisé pour l’adressage relatif dans le [Registre de couleur d’entrée](dx9-graphics-reference-asm-ps-registers-input-color.md) (v \# ) à l’intérieur du bloc de boucle.
-   i \# . x spécifie le nombre d’itérations. La plage autorisée est \[ 0, 255 \] . Notez que cette instruction n’incrémente pas ou ne décrémente pas la valeur de i \# . x.
-   i \# . y spécifie la valeur initiale du Registre du compteur de la [boucle](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (Al). La plage autorisée est \[ 0, 255 \] . Notez que cette instruction n’incrémente pas ou ne décrémente pas la valeur de i \# . y.
-   i \# . z spécifie la taille de l’étape/du Stride. La plage autorisée est \[ -128, 127 \] .
-   i \# . w n’est pas utilisé par le bloc de boucle et doit être égal à 0.
-   Les blocs de boucle peuvent être imbriqués. consultez [Limitations du contrôle de Flow](dx9-graphics-reference-asm-ps-instructions-flow-control.md).
-   Lorsqu’elle est imbriquée, la valeur du [Registre de compteur de boucle](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (Al) fait référence au bloc de boucle englobant immédiatement.
-   Les blocs de boucle sont autorisés à se trouver complètement à l’intérieur d’un bloc if ou à l' \* entourer complètement. Aucun chevauchement n’est autorisé.

## <a name="example"></a> Exemple


```
loop aL, i3
    add r1, r0, v2[ aL ]
endloop
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





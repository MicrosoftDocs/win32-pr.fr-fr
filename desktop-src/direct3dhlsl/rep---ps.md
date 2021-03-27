---
title: REP-PS
description: Démarrer un REP... bloc endrep-PS.
ms.assetid: vs|directx_sdk|~\rep___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a6873a6aee9e31b1f28ba2755b1869cddb177306
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679125"
---
# <a name="rep---ps"></a>REP-PS

Démarrer un REP... bloc [endrep-PS](endrep---ps.md) .

## <a name="syntax"></a>Syntaxe



| REP i\# |
|---------|



 

où i \# est un registre d’entiers qui spécifie le nombre de répétitions dans le composant. x. Consultez [Registre d’entiers constant](dx9-graphics-reference-asm-ps-registers-constant-integer.md).

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| attaché                   |      |      |      |      |      | x    | x     | x    | x     |



 

-   i \# . x spécifie le nombre d’itérations. La plage autorisée est \[ 0, 255 \] . Notez que cette instruction n’incrémente pas ou ne décrémente pas la valeur de i \# . x.
-   i \# . YZW ne sont pas utilisés par le bloc REPEAT.
-   Les blocs REPEAT peuvent être imbriqués. Consultez [limitations du contrôle de workflow](dx9-graphics-reference-asm-ps-instructions-flow-control.md).
-   Les blocs de répétition sont autorisés à se trouver complètement à l’intérieur d’un bloc if ou à l' \* entourer complètement. Aucun chevauchement n’est autorisé.
-   L’utilisation du même i \# pour des instructions de représentation différentes ou imbriquées est correcte. chaque boucle effectue une itération en fonction du nombre spécifié.

## <a name="example"></a>Exemple


```
rep i2
    add r0, r0, c0
endrep  
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





---
title: REP-vs
description: Démarrer un REP... bloc endrep.
ms.assetid: vs|directx_sdk|~\rep___vs.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6e800f2ef313cd5c9a4fc90d7205502db5532ae24f51ec0f1255d05cc9a589bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853789"
---
# <a name="rep---vs"></a>REP-vs

Démarrer un REP... bloc [endrep](endrep---vs.md) .

## <a name="syntax"></a>Syntaxe



| REP i\# |
|---------|



 

où i \# est un registre d’entiers qui spécifie le nombre de répétitions dans le composant. x. Consultez [Registre d’entiers constant](dx9-graphics-reference-asm-vs-registers-constant-integer.md).

## <a name="remarks"></a>Remarques



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| attaché                    |      | x    | x    | x     | x    | x     |



 

-   i \# . x spécifie le nombre d’itérations. La plage autorisée est \[ 0, 255 \] . Notez que cette instruction n’incrémente pas ou ne décrémente pas la valeur de i \# . x.
-   i \# . YZW ne sont pas utilisés par le bloc REPEAT.
-   Les blocs REPEAT peuvent être imbriqués. consultez [Flow limites d’imbrication des contrôles](dx9-graphics-reference-asm-vs-instructions-flow-control.md).
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

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





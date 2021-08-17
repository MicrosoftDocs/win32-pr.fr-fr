---
title: FRC-vs
description: Retourne la partie fractionnaire de chaque composant d’entrée. | FRC-vs
ms.assetid: 6b6a4475-b665-4de0-9423-88ea8103e606
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2ecc6a1c903f78fb7c03442809f792e3ddb984d04975d3f5ecb0b5c918f7ab4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117907642"
---
# <a name="frc---vs"></a>FRC-vs

Retourne la partie fractionnaire de chaque composant d’entrée.

## <a name="syntax"></a>Syntaxe



| FRC DST, SRC |
|--------------|



 

where

-   l’heure d’été est le registre de destination.
-   SRC est un registre source.

## <a name="remarks"></a>Remarques



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| frc                    | x    | x    | x    | x     | x    | x     |



 

Le fragment de code suivant illustre le fonctionnement conceptuel de l’instruction.


```
dest.x = src.x - (float)floor(src.x);
dest.y = src.y - (float)floor(src.y);
dest.z = src.z - (float)floor(src.z);
dest.w = src.w - (float)floor(src.w);
```



La fonction Floor convertit l’argument passé dans le plus grand entier qui est inférieur ou égal à l’argument. Elle est convertie en valeur float, puis soustraite de la valeur d’origine. La valeur fractionnaire qui en résulte est comprise entre 0,0 et 1,0.

Pour la version 1 \_ 1, les masques d’écriture autorisés sont. y et. XY (. x n’est pas autorisé).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





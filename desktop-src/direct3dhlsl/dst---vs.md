---
title: DST-vs
description: Calcule un vecteur de distance. | DST-vs
ms.assetid: 4315a29f-58e7-427f-aaa0-1fe1a81eb392
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d75eb61dd498d7a2f1d6bd9c5bd0dd9c52f3fd56625cb41b0026e9acce431ec6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068349"
---
# <a name="dst---vs"></a>DST-vs

Calcule un vecteur de distance.

## <a name="syntax"></a>Syntaxe



| DST dest, src0, src1 |
|----------------------|



 

where

-   dest est le registre de destination.
-   src0 est un registre source.
-   src1 est un registre source.

## <a name="remarks"></a>Remarques



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| dst                    | x    | x    | x    | x     | x    | x     |



 

Le fragment de code suivant montre les opérations effectuées :


```
dest.x = 1;
dest.y = src0.y * src1.y;
dest.z = src0.z;
dest.w = src1.w;
```



Le premier opérande source (src0) est supposé être le vecteur (ignoré, d d, \* d \* , ignoré) et le deuxième opérande source (src1) est supposé être le vecteur (ignoré, 1/d, ignoré, 1/d). La destination (dest) est le vecteur de résultat (1, d, d \* d, 1/d).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





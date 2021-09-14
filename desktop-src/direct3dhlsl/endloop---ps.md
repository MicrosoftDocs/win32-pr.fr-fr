---
title: ENDLOOP-PS
description: Fin d’une boucle-PS... bloc ENDLOOP.
ms.assetid: 8d05d0b3-88d2-44e3-a22d-54d8a8ceb5f4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee1a7eb10146e40a39c05bcecb99d3a7667dee2c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922411"
---
# <a name="endloop---ps"></a>ENDLOOP-PS

Fin d’une [boucle-PS](loop---ps.md)... bloc ENDLOOP.

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| ENDLOOP               |      |      |      |      |      |      |       | x    | x     |



 

ENDLOOP doit suivre la dernière instruction d’un bloc [Loop-PS](loop---ps.md) .

## <a name="example"></a>Exemple


```
loop aL, i3
    add r1, r0, c2[ aL ]
endloop
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





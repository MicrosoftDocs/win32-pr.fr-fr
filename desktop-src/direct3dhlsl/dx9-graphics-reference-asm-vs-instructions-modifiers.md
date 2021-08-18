---
title: Modificateurs d’instruction (référence HLSL VS)
description: Modificateurs d’instruction
ms.assetid: b713d847-c858-4492-918c-7a105f751624
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2bdad90d13fe960c0d7a5cabfbb508d8abba890e8114c6d4ae1e47d1977e7d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119693"
---
# <a name="instruction-modifiers-hlsl-vs-reference"></a>Modificateurs d’instruction (référence HLSL VS)

Les modificateurs d’instruction affectent le résultat de l’instruction avant qu’elle ne soit écrite dans le registre de destination.

## <a name="_sat"></a>\_sot

Sature (ou bride) le résultat de l’instruction à \[ 0,1 \] intervalle avant d’écrire dans le registre de destination.

Par exemple :


```
add_sat dst, src0, src1
```



Où :

DST = clamp \_ entre \_ 0 \_ et \_ 1 (src0 + src1)

Le \_ modificateur d’instruction SAT ne coûte aucun emplacement d’instruction supplémentaire.

En cas de prise en charge, le \_ modificateur d’instruction SAT peut être utilisé avec n’importe quelle instruction, à l’exception de : [FRC-vs](frc---vs.md), [SinCos,-vs](sincos---vs.md)et [texldl-vs](texldl---vs.md).



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| \_sot                  |      |      |      |       | x    | x     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





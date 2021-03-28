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
ms.openlocfilehash: 573f2ef618c4cd29092fb38fb4c805bdeeecc219
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104462623"
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

 

 





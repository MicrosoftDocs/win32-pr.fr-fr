---
title: étiquette-vs
description: Marquer l’instruction suivante comme ayant un index d’étiquette. | étiquette-vs
ms.assetid: e1aee8bc-4655-4bd5-8012-bd7a2d46e712
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6e2b72fe21301aa66d8428dc3696ceb3f12e6214
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992088"
---
# <a name="label---vs"></a>étiquette-vs

Marquer l’instruction suivante comme ayant un index d’étiquette.

## <a name="syntax"></a>Syntaxe



| étiquette l\# |
|-----------|



 

où \# identifie le numéro de l’étiquette.

Pour vs \_ 2 \_ 0 et vs \_ 2 \_ x, le numéro d’étiquette doit être compris entre 0 et 15.

Pour vs \_ 2 \_ SW, vs \_ 3 \_ 0 et vs \_ 3 \_ SW, le numéro d’étiquette doit être compris entre 0 et 2047.

## <a name="remarks"></a>Notes



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| label                  |      | x    | x    | x     | x    | x     |



 

Cette instruction définit une étiquette située à l’instruction de nuanceur suivante. L’instruction label ne peut être présente directement qu’après une instruction [RET](ret---vs.md) (qui définit la fin de la sous-routine ou du programme principal précédent).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





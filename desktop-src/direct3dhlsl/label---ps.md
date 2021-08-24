---
title: étiquette-PS
description: Marquer l’instruction suivante comme ayant un index d’étiquette. | étiquette-PS
ms.assetid: 21afa062-c536-4891-ba69-ca5284b0539c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 921abbc0518182eaef17326082a395e5c5729d8ab550610fe71c8dfabe46dd4e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854199"
---
# <a name="label---ps"></a>étiquette-PS

Marquer l’instruction suivante comme ayant un index d’étiquette.

## <a name="syntax"></a>Syntaxe



| étiquette l\# |
|-----------|



 

où \# identifie le numéro de l’étiquette.

Pour PS \_ 2 \_ x, le numéro d’étiquette doit être compris entre 0 et 15.

Pour les logiciels PS \_ 2 \_ , PS \_ 3 \_ 0 et PS \_ 3 \_ , le numéro d’étiquette doit être compris entre 0 et 2047.

## <a name="remarks"></a>Remarques



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| label                 |      |      |      |      |      | x    | x     | x    | x     |



 

Cette instruction définit une étiquette située à l’instruction de nuanceur suivante. L’instruction label ne peut être présente directement qu’après une instruction [RET](ret---ps.md) (qui définit la fin de la sous-routine ou du programme principal précédent).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





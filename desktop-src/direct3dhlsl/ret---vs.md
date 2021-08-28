---
title: RET-vs
description: Retour à partir d’une sous-routine ou d’une fonction main.
ms.assetid: ee3a6a7a-c068-442f-9f86-c637b5707224
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bec0356f2f1542da421a807598707e4857033c13cda2077d9281ac24e4fc3e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853769"
---
# <a name="ret---vs"></a>RET-vs

Retour à partir d’une sous-routine ou d’une fonction main.

## <a name="syntax"></a>Syntaxe



| Av |
|-----|



 

## <a name="remarks"></a>Remarques



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| Av                    |      | x    | x    | x     | x    | x     |



 

Cette instruction prend l’adresse d’une instruction de la pile d’adresses de retour et poursuit son exécution. Dans le cas de la fonction main, cette instruction arrête l’exécution du nuanceur.

L’instruction RET consomme un emplacement d’instruction de nuanceur de sommets.

Si un nuanceur ne contient pas de sous-routines, l’utilisation de RET à la fin du programme principal est facultative.

Plusieurs instructions return ne sont pas autorisées dans le programme principal ou dans une sous-routine, la première instruction return est traitée comme la fin du programme ou de la sous-routine principale.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





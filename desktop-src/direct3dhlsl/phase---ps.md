---
title: phase-PS
description: L’instruction de phase marque la transition entre la phase 1 et la phase 2. Si aucune instruction de phase n’est présente, le nuanceur entier s’exécute comme s’il s’agissait d’un nuanceur de phase 2.
ms.assetid: e0e89425-dc8e-489f-a0d1-3eefbfd09178
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aac29792274a36ad4bb7266ffa02d0ea5d2bb1b6cec8efe2db213e9b0dd4890b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118088692"
---
# <a name="phase---ps"></a>phase-PS

L’instruction de phase marque la transition entre la phase 1 et la phase 2. Si aucune instruction de phase n’est présente, le nuanceur entier s’exécute comme s’il s’agissait d’un nuanceur de phase 2.

Cette instruction s’applique uniquement à la version 1 \_ 4.

## <a name="syntax"></a>Syntaxe


```
phase
```



## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| phase                 |      |      |      | x    |      |      |       |      |       |



 

Les instructions de nuanceur qui se produisent avant l’instruction de phase sont des instructions de la phase 1. Toutes les autres instructions sont des instructions de la phase 2. En ayant deux phases pour les instructions, le nombre maximal d’instructions par nuanceur est augmenté.

L’effet secondaire de la transition de phase est que le composant alpha des [registres temporaires](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) n’est pas persistant dans la transition. En d’autres termes, le composant alpha doit être réinitialisé après l’instruction de phase.

## <a name="example"></a>Exemple

Cet exemple montre comment regrouper des instructions en tant qu’instructions de phase 1 ou de phase 2 au sein d’un nuanceur.

L’instruction de phase est également communément appelée marqueur de phase, car elle marque la transition entre les instructions de phase 1 et 2. Dans un \_ nuanceur de 4 pixels version 1, si le marqueur de phase n’est pas présent, le nuanceur est exécuté comme s’il s’exécutait à la phase 2. C’est important, car il existe des différences entre les instructions de phase 1 et 2 et l’inscription de la disponibilité. Les différences sont indiquées dans la section de référence.


```
ps_1_4
  // Add phase 1 instructions here

phase
  // Add phase 2 instructions here
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





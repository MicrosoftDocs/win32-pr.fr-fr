---
title: MOV-vs
description: Déplacer des données à virgule flottante entre registres.
ms.assetid: bf013ab2-593e-4201-ba75-faebd0c9f97a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 00f207261ad8ba6ac83360c40bc6008530292816
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679169"
---
# <a name="mov---vs"></a>MOV-vs

Déplacer des données à virgule flottante entre registres.

## <a name="syntax"></a>Syntaxe



| MOV DST, SRC |
|--------------|



 

where

-   l’heure d’été est le registre de destination.
-   SRC est un registre source.

## <a name="remarks"></a>Notes



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| Moy                    | x    | x    | x    | x     | x    | x     |



 

Peut être utilisé pour les données à virgule flottante. Pour la version vs \_ 1 \_ 1, il peut également être utilisé pour écrire le registre d’adresses. Lorsqu’elles sont utilisées pour mettre à jour des registres d’adresses, les valeurs sont converties de la virgule flottante à l’aide de l’arrondi au plus proche.

Le fragment de code suivant montre les opérations effectuées.


```
if(dest is an integer register)
{
    int intSrc = RoundToNearest(src.w);
    dest = intSrc;
}
else
{
    dest = src;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





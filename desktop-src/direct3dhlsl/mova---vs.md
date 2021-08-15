---
title: Mova-vs
description: Déplacez des données à partir d’un registre à virgule flottante vers le registre d’adresses, a0.
ms.assetid: 929a0670-f337-4d6d-a7e7-d285e7dc8ae1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dec849009ee47b4aaef1bc3766e2b141a8a6ccf5e17b16a370c6ea8284eaf957
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986329"
---
# <a name="mova---vs"></a>Mova-vs

Déplacez des données à partir d’un registre à virgule flottante vers le [Registre d’adresses](dx9-graphics-reference-asm-vs-registers-address.md), a0.

## <a name="syntax"></a>Syntaxe



| Mova DST, SRC |
|---------------|



 

where

-   l’heure d’été doit être le [Registre d’adresses](dx9-graphics-reference-asm-vs-registers-address.md), a0.
-   SRC est un registre source.

## <a name="remarks"></a>Remarques



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| mova                   |      | x    | x    | x     | x    | x     |



 

Déplace les données à virgule flottante vers un registre d’entiers. Les valeurs sont converties de la virgule flottante à l’aide de l’arrondi au plus proche.

Le registre d’adresses est le seul registre de destination autorisé.

Le fragment de code suivant montre les opérations effectuées.


```
if(dest is an integer register)
{
    int intSrc = RoundToNearest(src);
    dest = intSrc;
}
else
{
    dest = src;
}
```



Pour les versions 2 \_ x et ultérieures, le registre d’adresses est un vecteur de composant. Par conséquent, n’importe quel masque d’écriture est autorisé.


```
mova a0.xz, r0
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





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
ms.openlocfilehash: 9ac29bf0d74b4eb2cb6cb86bdf6b070cf56823eb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971610"
---
# <a name="mova---vs"></a>Mova-vs

Déplacez des données à partir d’un registre à virgule flottante vers le [Registre d’adresses](dx9-graphics-reference-asm-vs-registers-address.md), a0.

## <a name="syntax"></a>Syntaxe



| Mova DST, SRC |
|---------------|



 

where

-   l’heure d’été doit être le [Registre d’adresses](dx9-graphics-reference-asm-vs-registers-address.md), a0.
-   SRC est un registre source.

## <a name="remarks"></a>Notes



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

 

 





---
title: Si bool-vs
description: Démarre une si... sinon... endif-bloc vs.
ms.assetid: d77e2f81-400c-4997-9c34-426b6e6f47be
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b113c806342d786d258713128bc2cadcbb000235c2639f49e5b57ce3fa3bd2e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986529"
---
# <a name="if-bool---vs"></a>Si bool-vs

Démarre une si... [sinon](else---vs.md)... [endif-bloc vs](endif---vs.md) .

## <a name="syntax"></a>Syntaxe



| Si bool |
|---------|



 

où bool est un numéro de Registre bool. Consultez [Registre booléen constant](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).

## <a name="remarks"></a>Remarques



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| Si bool                |      | x    | x    | x     | x    | x     |



 

Si le registre booléen source dans l’instruction if a la valeur true, le code inclus dans l’instruction if et le signe else correspondant est exécuté. Sinon, le code délimité par [else](else---vs.md)... [endif-les instructions vs](endif---vs.md) sont exécutées. Cette instruction consomme un emplacement d’instruction.

Si les blocs peuvent être imbriqués.

Un bloc If ne peut pas chevaucher un bloc de boucle.

## <a name="example"></a>Exemple

Cette instruction fournit un contrôle de workflow statique conditionnel.


```
defb b2, TRUE

...

if b2
// Instructions to run if b2 is nonzero

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[else-vs](else---vs.md)
</dt> <dt>

[endif-vs](endif---vs.md)
</dt> </dl>

 

 





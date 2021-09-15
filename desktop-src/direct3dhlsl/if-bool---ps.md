---
title: Si bool-PS
description: Début d’un bloc If.
ms.assetid: cff53072-1c73-4cf8-9ecd-11032a9c4bbb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 92c3158a09aeb871ef367133c07278b0f3b87390
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519777"
---
# <a name="if-bool---ps"></a>Si bool-PS

Début d’un bloc If.

## <a name="syntax"></a>Syntaxe



| Si bool |
|---------|



 

Où :

-   bool est un numéro de Registre bool (booléen). Consultez [Registre booléen constant](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Si bool               |      |      |      |      |      | x    | x     | x    | x     |



 

Si le registre booléen source dans l’instruction if a la valeur true, le code inclus dans l’instruction if et la correspondance [endif-PS](endif---ps.md) ou [else-PS](else---ps.md) est exécuté. Sinon, le code délimité par else-PS... les instructions endif-PS sont exécutées. Cette instruction consomme un emplacement d’instruction.

Un bloc If peut être imbriqué.

Un bloc If ne peut pas chevaucher un bloc de boucle.

Un bloc If peut être suivi d’un bloc d’instructions et/ou d’une instruction [else-PS](else---ps.md) , et/ou d’une instruction [endif-PS](endif---ps.md) .

## <a name="example"></a>Exemple

Cette instruction fournit un contrôle de workflow statique conditionnel.


```
defb b3, true

if b3
// Instructions to run if b3 is nonzero
else
// Instructions to run otherwise
endif
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[else-PS](else---ps.md)
</dt> <dt>

[endif-PS](endif---ps.md)
</dt> </dl>

 

 





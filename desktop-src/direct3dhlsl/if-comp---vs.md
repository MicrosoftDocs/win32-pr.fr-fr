---
title: if_comp-vs
description: Démarrer une si bool-vs... else-vs... endif-bloc vs, avec une condition basée sur les valeurs qui peuvent être calculées dans un nuanceur. Cette instruction est utilisée pour ignorer un bloc de code, en fonction d’une condition.
ms.assetid: a3fe93c6-be26-4216-a601-3be52a74be06
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 11c7abceb9b484c4cd104e136c47edeb55b93b5273f953cb6d98052e247513d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743579"
---
# <a name="if_comp---vs"></a>Si \_ COMP-vs

Démarrer une [si bool-vs](if-bool---vs.md)... [else-vs](else---vs.md)... [endif-bloc vs](endif---vs.md) , avec une condition basée sur les valeurs qui peuvent être calculées dans un nuanceur. Cette instruction est utilisée pour ignorer un bloc de code, en fonction d’une condition.

## <a name="syntax"></a>Syntaxe



| Si \_ COMP src0, src1 |
|---------------------|



 

Où :

-   \_COMP est une comparaison entre les deux registres sources. Les valeurs possibles sont les suivantes : 

    | Syntaxe | Comparaison            |
    |--------|-----------------------|
    | \_TB   | Supérieur à          |
    | \_terme   | Inférieur à             |
    | \_&   | Supérieur ou égal à |
    | \_WinINSTALL   | Inférieur ou égal à    |
    | \_EQ   | Égal à              |
    | \_ne   | Différent de          |

    

     

-   src0 est un registre source. La réplication de Swizzle est requise pour sélectionner un composant.
-   src1 est un registre source. La réplication de Swizzle est requise pour sélectionner un composant.

## <a name="remarks"></a>Remarques



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| Si \_ COMP               |      |      | x    | x     | x    | x     |



 

Cette instruction est utilisée pour ignorer un bloc de code, en fonction d’une condition.


```
if_lt src0, src1
   jump to the corresponding else or endif instruction;
```



Veillez à utiliser les modes de comparaison égal à et différent de sur les nombres à virgule flottante. Étant donné que l’arrondi se produit pendant les calculs à virgule flottante, la comparaison peut être effectuée par rapport à une valeur Epsilon (petit nombre différent de zéro) pour éviter les erreurs.

Les restrictions sont les suivantes :

-   Si \_ COMP... [else-vs](else---vs.md)... [endif-](endif---vs.md) les blocs vs (avec les blocs if prédicats) peuvent être imbriqués jusqu’à 24 couches.
-   les registres src0 et src1 requièrent un Swizzle de réplication.
-   Si \_ les blocs COMP doivent se terminer par une instruction [else-vs](else---vs.md) ou [endif-vs](endif---vs.md) .
-   Si \_ COMP... [else-vs](else---vs.md)... [endif-les blocs vs](endif---vs.md) ne peuvent pas chevaucher un bloc de boucle. Le \_ bloc If COMP doit être complètement à l’intérieur ou à l’extérieur du bloc [Loop-vs](loop---vs.md) .

## <a name="example"></a>Exemples

Cette instruction fournit un contrôle de workflow dynamique conditionnel.


```
if_lt r3.x, r4.y
// Instructions to run if r3.x < r4.y

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





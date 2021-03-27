---
title: if_comp-PS
description: Démarrer une si bool-PS... else-PS... endif-bloc PS, avec une condition basée sur les valeurs qui peuvent être calculées dans un nuanceur. Cette instruction est utilisée pour ignorer un bloc de code, en fonction d’une condition.
ms.assetid: a641e347-df28-4a3f-a461-0b6aee758e59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: db30983c83bc7d66e06befd07f4eb1dcdc9b21ea
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679101"
---
# <a name="if_comp---ps"></a>Si \_ COMP-PS

Démarrer une [si bool-PS](if-bool---ps.md)... [else-PS](else---ps.md)... [endif-bloc PS](endif---ps.md) , avec une condition basée sur les valeurs qui peuvent être calculées dans un nuanceur. Cette instruction est utilisée pour ignorer un bloc de code, en fonction d’une condition.

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

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Si \_ COMP              |      |      |      |      |      | x    | x     | x    | x     |



 

Cette instruction est utilisée pour ignorer un bloc de code, en fonction d’une condition.


```
if (src0 comparison src1)
   jump to the corresponding else or endif instruction;
```



Veillez à utiliser les modes de comparaison égal à et différent de sur les nombres à virgule flottante. Étant donné que l’arrondi se produit pendant les calculs à virgule flottante, la comparaison peut être effectuée par rapport à une valeur Epsilon (petit nombre différent de zéro) pour éviter les erreurs.

Les restrictions sont les suivantes :

-   Si \_ COMP... [else-PS](else---ps.md)... [endif](endif---ps.md) les blocs PS (ainsi que les blocs [If](if-bool---ps.md) prédicats) peuvent être imbriqués jusqu’à 24 niveaux de profondeur.
-   les registres src0 et src1 requièrent un Swizzle de réplication.
-   Si \_ les blocs COMP doivent se terminer par une instruction [else-vs](else---vs.md) ou [endif-vs](endif---vs.md) .
-   Si \_ COMP... [else-PS](else---ps.md)... [endif : les blocs PS](endif---ps.md) ne peuvent pas chevaucher un bloc de boucle. Le \_ bloc If COMP doit être complètement à l’intérieur ou à l’extérieur du bloc de boucle.

## <a name="example"></a>Exemple

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

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





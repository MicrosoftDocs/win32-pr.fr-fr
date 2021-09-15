---
title: setp_comp-vs
description: Définissez le registre de prédicat. | setp_comp-vs
ms.assetid: bfead3f8-f7fe-4fc1-939f-8e5fbc3e0adf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77d9e5f46e9fb8bbcfb96e56d13cd6f7cebfecc2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524529"
---
# <a name="setp_comp---vs"></a>\_COMP setp-vs

Définissez le registre de prédicat.

## <a name="syntax"></a>Syntaxe



| SETP \_ COMP DST, src0, src1 |
|----------------------------|



 

Où :

-   \_COMP est une comparaison par canal entre les deux registres sources. Les valeurs possibles sont les suivantes : 

    | Syntaxe | Comparaison            |
    |--------|-----------------------|
    | \_TB   | Supérieur à          |
    | \_terme   | Inférieur à             |
    | \_&   | Supérieur ou égal à |
    | \_WinINSTALL   | Inférieur ou égal à    |
    | \_EQ   | Égal à              |
    | \_ne   | Différent de          |

    

     

-   DST est le registre de [Registre des prédicats](dx9-graphics-reference-asm-vs-registers-predicate.md) , P0.
-   src0 est un registre source.
-   src1 est un registre source.

## <a name="remarks"></a>Notes



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| \_COMP setp             |      |      | x    | x     | x    | x     |



 

Cette instruction fonctionne comme suit :


```
per channel in destination write mask
{
  dst.channel = src0.channel cmp src1.channel
}
```



Pour chaque canal qui peut être écrit selon le masque d’écriture de destination, enregistrez le résultat booléen de l’opération de comparaison entre les canaux correspondants de src0 et src1 (une fois que le modificateur de source Swizzles a été résolu).

Les registres sources permettent de spécifier des Swizzles de composant arbitraires.

Le registre de destination autorise des masques d’écriture arbitraires.

Le registre de dest doit être le registre de prédicat.

## <a name="applying-the-predicate-register"></a>Application du registre de prédicat

Une fois que le registre de prédicat a été initialisé avec setp, il peut être utilisé pour contrôler une instruction par composant. Voici la syntaxe :


```
([!]p0[.swizzle]) instruction dest, srcReg, ...
```



Où :

-   \[!\] est un booléen facultatif NOT
-   P0 correspond au registre de prédicat
-   \[. Swizzle \] est un Swizzle facultatif à appliquer au contenu du registre de prédicat avant de l’utiliser pour masquer l’instruction. Les Swizzles disponibles sont :. XYZW (valeur par défaut si aucune valeur n’est spécifiée) ou n’importe quel Swizzle de réplication :. x/. r,. y/. g,. z/. b ou. a/. w.
-   instruction est une aritmetic ou une instruction de texture. Il ne peut pas s’agir d’une instruction de contrôle de workflow statique ou dynamique.
-   dest, srcReg,... registres requis par l’instruction

En supposant que le registre de prédicat a été configuré avec des valeurs de composant (true, true, false, false), il peut être appliqué à cette instruction :


```
// given r0 = 0,0,1,1
// given r1 = 1,1,0,0
setp_le p0, r0, r1
(p0) add r2, r3, r4
```



pour effectuer un ajout de 2 composants.


```
r2.x = r3.x + r4.x
r2.y = r3.y + r4.y
```



Les composants x et y de R2 ne seront pas écrits puisque le registre de prédicat contenait la valeur false dans les composants z et w.

L’application du registre de prédicat à une instruction arithmétique ou de texture augmente son nombre d’emplacements d’instructions de 1.

Le registre de prédicat peut également être appliqué à [If prédit-vs](if-pred---vs.md), [callnz prédit-vs](callnz-pred---vs.md) et [breakp-vs](breakp---vs.md) . Ces instructions de contrôle de Flow n’ont pas d’augmentation du nombre d’emplacements d’instruction lors de l’utilisation du registre de prédicat.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





---
title: setp_comp-PS
description: Définissez le registre de prédicat. | setp_comp-PS
ms.assetid: a9acb685-f9aa-41f1-8ef1-6d104cb76a09
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d278a6104a6c47d84623b185f78b921d61899f296eeaa557a6c6c6d5344097b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119487079"
---
# <a name="setp_comp---ps"></a>SETP \_ COMP-PS

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

    

     

-   DST est le registre de [Registre des prédicats](dx9-graphics-reference-asm-ps-registers-predicate.md) , P0.
-   src0 est un registre source.
-   src1 est un registre source.

## <a name="remarks"></a>Remarques



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| \_COMP setp            |      |      |      |      |      | x    | x     | x    | x     |



 

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

Le registre de l’heure d’été doit être un registre de prédicat.

## <a name="applying-the-predicate-register"></a>Application du registre de prédicat

Une fois que le registre de prédicat a été initialisé avec setp \_ COMP, il peut être utilisé pour contrôler une instruction par composant. Voici la syntaxe :


```
([!]p0[.swizzle]) instruction dest, src0, ...
```



Où :

-   \[!\] est un booléen facultatif NOT
-   P0 correspond au registre de prédicat
-   \[. Swizzle \] est un Swizzle facultatif à appliquer au contenu du registre de prédicat avant de l’utiliser pour masquer l’instruction. Les Swizzles disponibles sont :. XYZW (valeur par défaut si aucune valeur n’est spécifiée) ou n’importe quel Swizzle de réplication :. x/. r,. y/. g,. z/. b ou. a/. w.
-   instruction est une aritmetic ou une instruction de texture. Il ne peut pas s’agir d’une instruction de contrôle de workflow statique ou dynamique.
-   dest, src0,... registres requis par l’instruction

En supposant que le registre de prédicat a été configuré avec des valeurs de composant (true, true, false, false), il peut être appliqué à cette instruction :


```
(p0) add r1, r2, r3
```



pour effectuer un ajout de 2 composants.


```
r1.x = r2.x + r3.x
r1.y = r2.y + r3.y
```



Les composants z et w de R1 ne seront pas écrits puisque le registre de prédicat contenait la valeur false dans les composants z et w.

L’application du registre de prédicat à une instruction arithmétique ou de texture augmente son nombre d’emplacements d’instructions de 1.

Le registre de prédicat peut également être appliqué aux instructions [If prédit-PS](if-pred---ps.md), [callnz prédit-PS](callnz-pred---ps.md) et [breakp-PS](break-p---ps.md) . Ces instructions de contrôle de Flow n’ont pas d’augmentation du nombre d’emplacements d’instruction lors de l’utilisation du registre de prédicat.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





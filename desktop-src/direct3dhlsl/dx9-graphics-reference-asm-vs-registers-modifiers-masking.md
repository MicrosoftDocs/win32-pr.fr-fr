---
title: Masquage du registre de destination
description: Le masquage spécifie les composants du registre de destination qui seront mis à jour avec le résultat d’une instruction. Les registres de texture ont un ensemble de règles et les registres de la même façon ont un autre ensemble de règles.
ms.assetid: 989ebe55-1f80-4063-b116-4284520f52cc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7ce15f75f424cb7796ef7db7a8b89bd5bcbfa9cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380153"
---
# <a name="destination-register-masking"></a>Masquage du registre de destination

Le masquage spécifie les composants du registre de destination qui seront mis à jour avec le résultat d’une instruction. Les registres de texture ont un ensemble de règles et les registres de la même façon ont un autre ensemble de règles.

-   virtuel DX9 \_ Graphics \_ Reference \_ ASM \_ vs \_ enregistreurs \_ modificateurs \_ Masking-cette section contient des règles pour l’application de masques aux registres de destination.
-   \_ \_ Masques de registre de texture-les registres de texture présentent des règles uniques.

## <a name="destination-register-masking"></a>Masquage du registre de destination

Comme indiqué dans le tableau suivant, le masquage (où est l’un des [registres de nuanceur](dx9-graphics-reference-asm-vs-registers.md)vertex nuanceur de sommets valides) peut être appliqué aux composants individuels des données vectorielles.



| Modificateur de composant | Description      |
|--------------------|------------------|
| r. {x} {y} {z} {w}     | Masque de destination |



 

-   En général, la spécification de masques d’écriture de registre de destination est un bon style de codage. Cela rend le code plus facile à lire et à gérer.
-   Vous pouvez spécifier n’importe quelle combinaison de composants (y compris aucun) tant que x précède y, y précède z et z précède w.
-   Les registres de sortie oPts et oFog doivent utiliser un seul masque.
-   Certaines instructions requièrent que le registre de destination utilise un masque d’écriture unique : exp, expp, log, logP, Pow, RCP et rsq.
-   Dans la version 1,0, l’instruction FRC nécessitait l’une des combinaisons de masques suivantes :. x ou. y ou. XY. La version 2,0 n’a aucune restriction de masque.
-   SinCos, requiert l’une des combinaisons de masques suivantes :. x ou. y ou. xyz.
-   M3X2 requiert le masque d’écriture. XY.
-   M3x3 et m4x3 requièrent le masque d’écriture. xyz.
-   M3x4 et M4X4 requièrent le masque d’écriture. xyz ou le masque d’écriture par défaut (XYZW).

## <a name="texture-register-masks"></a>Masques de registre de texture

Les règles de validation pour l’utilisation de modificateurs sur les registres de coordonnées de texture sont plus strictes que les règles de validation pour les autres registres.

-   Si oTn est écrit, tous les registres précédents (oTn-1 ~ oT0) doivent également être écrits.
-   Le masque d’écriture « combiné » pour tout \# Registre OT doit être exactement l’un des éléments suivants :
    -   .x
    -   . XY
    -   . xyz
    -   . XYZW (ce qui équivaut à ne pas utiliser de modificateurs de composant)

Par exemple, un nuanceur de sommets peut sortir des registres de texture dans des instructions distinctes.


```
    oT1.y  
    oT0.y  
    oT2  
    oT0.xz  
    oT1.x
```



Ou, les instructions peuvent être combinées.


```
    oT0.xyz  
    oT1.xy  
    oT2.xyzw    
```



Ces restrictions s’appliquent uniquement aux registres de coordonnées de texture.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modificateurs de registre de nuanceur vertex](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 





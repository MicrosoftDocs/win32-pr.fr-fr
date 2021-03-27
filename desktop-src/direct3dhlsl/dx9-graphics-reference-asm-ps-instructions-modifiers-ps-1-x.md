---
title: Modificateurs pour ps_1_X
description: Les modificateurs d’instruction affectent le résultat de l’instruction avant qu’elle ne soit écrite dans le registre de destination.
ms.assetid: 15b892da-b6fd-4bd5-8889-bc48035e7819
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bbc8a9b13f7ffc29cf84bc839409f29bea6c8c8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840842"
---
# <a name="modifiers-for-ps_1_x"></a>Modificateurs pour PS \_ 1 \_ X

Les modificateurs d’instruction affectent le résultat de l’instruction avant qu’elle ne soit écrite dans le registre de destination. Par exemple, utilisez-les pour multiplier ou diviser le résultat par un facteur de deux, ou pour fixer le résultat entre zéro et un. Les modificateurs d’instruction sont appliqués après l’exécution de l’instruction mais avant l’écriture du résultat dans le registre de destination.

La liste des modificateurs est indiquée ci-dessous.



| Modificateur | Description                   | Syntaxe           | Version |      |      |      |
|----------|-------------------------------|------------------|---------|------|------|------|
|          |                               |                  | 1\_1    | 1\_2 | 1 \_ 3 | 1\_4 |
| \_x2     | Multiplier par 2                 | instruction \_ x2  | X       | X    | X    | X    |
| \_x4     | Multiplier par 4                 | instruction \_ X4  | X       | X    | X    | X    |
| \_8     | Multiplier par 8                 | instruction \_ x8  |         |      |      | X    |
| \_D2     | Division par 2                   | instruction \_ D2  | X       | X    | X    | X    |
| \_D4     | Division par 4                   | instruction \_ D4  |         |      |      | X    |
| \_D8     | Division par 8                   | instruction \_ D8  |         |      |      | X    |
| \_sot    | Saturation (Clamp de 0 et 1) | instruction \_ SAT | X       | X    | X    | X    |



 

-   Le modificateur Multiply multiplie les données de Registre par une puissance de deux après leur lecture. C’est le même qu’un décalage vers la gauche.
-   Le modificateur de division divise les données de Registre par une puissance de deux après leur lecture. C’est le même qu’un décalage vers la droite.
-   Le modificateur de saturation fixe la plage des valeurs de registre de zéro à un.

Les modificateurs d’instruction peuvent être utilisés sur des instructions arithmétiques. Elles ne peuvent pas être utilisées dans les instructions d’adresse de texture.

Multiplier (modificateur)

Cet exemple charge le registre de destination (dest) avec la somme des deux couleurs dans les opérandes sources (src0 et src1) et multiplie le résultat par deux.


```
add_x2 dest, src0, src1
```



Cet exemple combine deux modificateurs d’instruction. En premier lieu, deux couleurs dans les opérandes sources (src0 et src1) sont ajoutées. Le résultat est ensuite multiplié par deux et placé entre 0,0 et 1,0 pour chaque composant. Le résultat est enregistré dans le registre de destination.


```
add_x2_sat dest, src0, src1
```



Diviser (modificateur)

Cet exemple charge le registre de destination (dest) avec la somme des deux couleurs dans les opérandes sources (src0 et src1) et divise le résultat par deux.


```
add_d2 dest, src0, src1
```



Saturation (modificateur)

Pour les instructions arithmétiques, le modificateur de saturation fixe le résultat de cette instruction dans la plage 0,0 à 1,0 pour chaque composant. L’exemple suivant montre comment utiliser ce modificateur d’instruction.


```
dp3_sat r0, t0_bx2, v0_bx2    ; t0 is bump, v0 is light direction
```



Cette opération se produit après n’importe quel modificateur d’instruction Multiply ou de division. \_la SAT est le plus souvent utilisé pour brider les résultats du produit scalaire. Toutefois, elle permet également une émulation cohérente des méthodes multipasses dans lesquelles la mémoire tampon de trame est toujours comprise entre 0 et 1, et de la syntaxe de multitexture DirectX 6 et 7,0, dans laquelle la saturation est définie pour se produire à chaque étape.

Cet exemple charge le registre de destination (dest) avec la somme des deux couleurs dans les opérandes sources (src0 et src1) et fixe le résultat dans la plage 0,0 à 1,0 pour chaque composant.


```
add_sat dest, src0, src1
```



Cet exemple combine deux modificateurs d’instruction. En premier lieu, deux couleurs dans les opérandes sources (src0 et src1) sont ajoutées. Le résultat est multiplié par deux et est ancré entre 0,0 et 1,0 pour chaque composant. Le résultat est enregistré dans le registre de destination.


```
add_x2_sat dest, src0, src1
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





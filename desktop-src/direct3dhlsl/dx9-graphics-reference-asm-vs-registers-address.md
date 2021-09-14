---
title: Registre d’adresses
description: Le Registre a0 est un registre d’adresses.
ms.assetid: ad86013c-3358-4770-a01c-544c868691f4
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e58f42848034d12063611e14b82cb2f2d132cb43
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292675"
---
# <a name="address-register"></a>Registre d’adresses

Le Registre a0 est un registre d’adresses. Un registre unique est disponible dans la version vs \_ 1 \_ 1. Le registre d’adresses, désigné par a0. x dans vs \_ 1 \_ 1, peut être utilisé comme décalage d’entier signé pour l’adressage relatif dans le fichier de registre de constante. Pour les versions vs \_ 2 \_ et supérieures, les quatre composants (. x,. y,. z,. w) sont disponibles pour l’adressage relatif.


```
c[a0.x + n]
```



Le registre d’adresses ne peut pas être lu par un nuanceur de sommets, il ne peut être utilisé que pour l’adressage relatif d’un registre de constante. La lecture des valeurs en dehors de la plage légale retourne (0,0, 0,0, 0,0, 0,0). Le registre d’adresses ne peut être qu’une destination pour l’instruction [MOV-vs](mov---vs.md) . Si un nombre à virgule flottante est déplacé dans un registre d’entiers, une conversion d’arrondi à la valeur la plus proche se produit.

Tous les nuanceurs doivent initialiser le registre d’adresses avant de l’utiliser. Pour la version de vs \_ 2 \_ 0 et les versions ultérieures, l’instruction [Mova-vs](mova---vs.md) peut déplacer une valeur à virgule flottante vers un registre d’adresses.



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ logiciels | 2 \_ x | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|-------|------|------|-------|
| Registre d’adresses       | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Registres de nuanceur vertex](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 





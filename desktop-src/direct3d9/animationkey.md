---
description: Définit un ensemble de clés d’animation. Une clé de matrice est utile pour les jeux de données d’animation qui doivent être représentés en tant que matrices de transformation.
ms.assetid: bf007541-7fea-423e-910b-fa5f45271608
title: AnimationKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05728f124ae01962a1291547f8fe8b7fcebd175a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513945"
---
# <a name="animationkey"></a>AnimationKey

Définit un ensemble de clés d’animation. Une clé de matrice est utile pour les jeux de données d’animation qui doivent être représentés en tant que matrices de transformation.

``` syntax
template AnimationKey
{
    < 10DD46A8-775B-11CF-8F52-0040333594A3 >
    DWORD keyType;
    DWORD nKeys;
    array TimedFloatKeys keys[nKeys];
} 
```

Où :

-   KeyType : spécifie si les clés sont des clés de rotation, de mise à l’échelle, de position ou de matrice (à l’aide des entiers 0, 1, 2 ou 3, respectivement).
-   nKeys : nombre de clés.
-   Keys : un tableau de clés. Consultez [**TimedFloatKeys**](timedfloatkeys.md).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Modèles](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 




---
description: Définit un ensemble de clés d’animation. Une clé de matrice est utile pour les jeux de données d’animation qui doivent être représentés en tant que matrices de transformation.
ms.assetid: bf007541-7fea-423e-910b-fa5f45271608
title: AnimationKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bad23a6cc519b0b0525cd0dac1b488184b3bf91e99359e252f44dca435ace529
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118806404"
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

 

 




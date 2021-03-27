---
title: Registre temporaire (référence du PS HLSL)
description: Les registres temporaires d’entrée de nuanceur de pixels sont utilisés pour conserver les résultats intermédiaires.
ms.assetid: e61daaa1-0a9b-4b1c-b91c-56573be59ed9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7aebee99a693ac629d9cc8a372fba7589a9e29ef
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "103841717"
---
# <a name="temporary-register-hlsl-ps-reference"></a>Registre temporaire (référence du PS HLSL)

Les registres temporaires d’entrée de nuanceur de pixels sont utilisés pour conserver les résultats intermédiaires.

Syntaxe


```
no declaration is required
```





| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ logiciels | 2 \_ x | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| Registre temporaire    |      |      |      |      | x    | x     | x    | x    | x     |



 

-   Il y a 12 registres temporaires de nuanceur de pixels : R0 à R11.
-   Ces registres sont utilisés pour stocker les résultats intermédiaires lors des calculs.
-   Si un registre temporaire utilise des composants qui ne sont pas définis dans le code précédent, la validation du nuanceur échoue.
-   Il s’agit au moins d’une précision à virgule flottante.
-   Un maximum de trois peut être utilisé dans une instruction unique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscrit](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 





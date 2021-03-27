---
title: Registre de compteur de boucles (référence du PS HLSL)
description: Le seul registre de cette banque est le Registre du compteur de boucles actuel (aL).
ms.assetid: 36999873-a251-4939-aac0-faa7f910bc33
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 47582552b7e32ede7cd83637cbc3900494dfd611
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "103679226"
---
# <a name="loop-counter-register-hlsl-ps-reference"></a>Registre de compteur de boucles (référence du PS HLSL)

Le seul registre de cette banque est le Registre du compteur de boucles actuel (aL). Elle est incrémentée automatiquement à chaque exécution du bloc [Loop-PS](loop---ps.md) / [ENDLOOP-PS](endloop---ps.md) . Il peut donc être utilisé dans le bloc pour l’adressage relatif si nécessaire et n’est pas valide pour l’utiliser en dehors de la boucle.



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ logiciels | 2 \_ x | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| Registre de compteur de boucle |      |      |      |      |      |       |      | x    | x     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscrit](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 





---
title: Registre source Swizzling (référence HLSL VS)
description: Avant l’exécution d’une instruction, les données d’un registre source sont copiées dans un registre temporaire. Swizzling fait référence à la capacité de copier n’importe quel composant Registre source vers un composant de registre temporaire. Swizzling n’affecte pas les données du Registre source.
ms.assetid: 6271d846-c68d-467c-a110-be3279e0c11a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03dd2d9051c185d1be1ccb6fce18549bf5aa3414975c9a600bb8f8c47f78d4c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854549"
---
# <a name="source-register-swizzling-hlsl-vs-reference"></a>Registre source Swizzling (référence HLSL VS)

Avant l’exécution d’une instruction, les données d’un registre source sont copiées dans un registre temporaire. Swizzling fait référence à la capacité de copier n’importe quel composant Registre source vers un composant de registre temporaire. Swizzling n’affecte pas les données du Registre source.

## <a name="component-swizzling"></a>Swizzling composant

Comme indiqué dans le tableau suivant, swizzling peut être appliqué aux composants individuels des données du Registre source (où sont l’un des registres d’entrée de nuanceur de sommets valides [-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)).



| Modificateur de composant                 | Description    |
|------------------------------------|----------------|
| r. \[ XYZW \] \[ XYZW \] \[ XYZW \] \[ XYZW\] | Swizzle source |



 

-   Les quatre composants sont toujours copiés. Si moins de quatre composants sont spécifiés, le dernier composant est répété (XY signifie. xyyy). Si aucun composant n’est spécifié, x est répété (. xxxx).
-   Les composants peuvent apparaître dans n’importe quel ordre. v0. ywx résultats dans v0. ywxx.
-   Les composants RVBA peuvent être utilisés respectivement pour XYZW (r pour x, g pour b, etc.).
-   Ces instructions implémentent la source-inscrire un composant unique Swizzles : exp, expp, log, logP, Pow, RCP, rsq. Le résultat de ces instructions est copié dans les quatre composants du registre de destination.

Swizzling ne peut pas être utilisé sur les instructions [M3X2-vs](m3x2---vs.md), [M3x3-vs](m3x3---vs.md), [m4x3-vs](m4x3---vs.md)et [M4X4-vs](m4x4---vs.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modificateurs de registre de nuanceur vertex](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 





---
title: Registre d’entiers constant (référence PS HLSL)
description: Les registres d’entiers constants sont utilisés uniquement par Loop-PS et REP-PS.
ms.assetid: 85720ec0-b6aa-4a24-910c-3ad0468300dc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9b03a27a95f84ae30a70147caaf5662e1949cf18
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971750"
---
# <a name="constant-integer-register-hlsl-ps-reference"></a>Registre d’entiers constant (référence PS HLSL)

Les registres d’entiers constants sont utilisés uniquement par [Loop-PS](loop---ps.md) et [REP-PS](rep---ps.md).

Ils peuvent être définis à l’aide de la définition [-PS](defi---ps.md) ou [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti).

En cas d’utilisation comme argument de l’instruction [Loop-PS](loop---ps.md) :

-   . x est le nombre d’itérations. ([REP-PS](rep---ps.md) utilise uniquement ce composant).
-   . y est la valeur initiale du compteur de boucle.
-   . z est l’étape d’incrément du compteur de boucles.



| Versions de nuanceur de pixels     | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ logiciels | 2 \_ x | 3 \_ 0 | 3 \_ logiciels |
|---------------------------|------|------|------|------|------|-------|------|------|-------|
| Registre d’entiers constant |      |      |      |      |      |       | x    | x    | x     |



 

Le comportement des constantes de nuanceur a changé entre Direct3D 8 et Direct3D 9.

-   Pour Direct3D 9, les constantes définies avec defx affectent des valeurs à l’espace constant du nuanceur. La durée de vie d’une constante déclarée avec defx est limitée à l’exécution de ce nuanceur uniquement. À l’inverse, les constantes définies à l’aide des API SetXXXShaderConstantX initialisent des constantes dans l’espace global. Les constantes dans l’espace global ne sont pas copiées dans l’espace local (visible par le nuanceur) tant que SetxxxShaderConstants n’est pas appelé.
-   Pour Direct3D 8, les constantes définies avec defx ou les API attribuent des valeurs à l’espace de constante de nuanceur. Chaque fois que le nuanceur est exécuté, les constantes sont utilisées par le nuanceur actuel, quelle que soit la technique utilisée pour les définir.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscrit](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 
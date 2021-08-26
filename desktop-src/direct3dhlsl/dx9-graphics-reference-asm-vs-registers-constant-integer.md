---
title: Registre d’entiers constants (référence HLSL VS)
description: Les registres d’entiers constants sont utilisés uniquement par Loop-vs et REP-vs.
ms.assetid: da9916d4-655b-4c98-99a4-1abfa66459b5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b46390303b2ee3aae2243f25d2a5a76385b9e9dd275c2952e8aa93e18f999e9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949899"
---
# <a name="constant-integer-register-hlsl-vs-reference"></a>Registre d’entiers constants (référence HLSL VS)

Les registres d’entiers constants sont utilisés uniquement par [Loop-vs](loop---vs.md) et [REP-vs](rep---vs.md).

Ils peuvent être définis à l’aide de la définition [-vs](defi---vs.md) ou [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti).

En cas d’utilisation comme argument de l’instruction [Loop-vs](loop---vs.md) :

-   . x est le nombre d’itérations. ([REP-vs](rep---vs.md) utilise uniquement ce composant).
-   . y est la valeur initiale du compteur de boucle.
-   . z est l’étape d’incrément du compteur de boucles.

Le comportement des constantes de nuanceur a changé entre Direct3D 8 et Direct3D 9.

-   Pour Direct3D 9, les constantes définies avec defx affectent des valeurs à l’espace constant du nuanceur. La durée de vie d’une constante déclarée avec defx est limitée à l’exécution de ce nuanceur uniquement. À l’inverse, les constantes définies à l’aide des API SetXXXShaderConstantX initialisent des constantes dans l’espace global. Les constantes dans l’espace global ne sont pas copiées dans l’espace local (visible par le nuanceur) tant que SetxxxShaderConstants n’est pas appelé.
-   Pour Direct3D 8, les constantes définies avec defx ou les API attribuent des valeurs à l’espace de constante de nuanceur. Chaque fois que le nuanceur est exécuté, les constantes sont utilisées par le nuanceur actuel, quelle que soit la technique utilisée pour les définir.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Registres de nuanceur vertex](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 
---
title: Registre booléen constant (référence HLSL VS)
description: Ce registre est une collection de bits utilisés dans les instructions de contrôle de Flow statique (par exemple, si bool-vs-else-vs-endif-vs).
ms.assetid: bd02d03b-c228-481a-9c98-7442be4cdd07
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9b32841f060a29fce2918daca8f8fd008529bef1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971747"
---
# <a name="constant-boolean-register-hlsl-vs-reference"></a>Registre booléen constant (référence HLSL VS)

Ce registre est une collection de bits utilisés dans les instructions de contrôle de Flow statique (par exemple, [si bool-vs](if-bool---vs.md)  -  [else-vs](else---vs.md)  -  [endif-vs](endif---vs.md)). Il y en a 16, donc un nuanceur peut avoir 16 conditions de branche indépendantes. Ils peuvent être définis à l’aide [de defb-vs](defb---vs.md) ou [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb).

Le comportement des constantes de nuanceur a changé entre Direct3D 8 et Direct3D 9.

-   Pour Direct3D 9, les constantes définies avec defx affectent des valeurs à l’espace constant du nuanceur. La durée de vie d’une constante déclarée avec defx est limitée à l’exécution de ce nuanceur uniquement. À l’inverse, les constantes définies à l’aide des API SetXXXShaderConstantX initialisent des constantes dans l’espace global. Les constantes dans l’espace global ne sont pas copiées dans l’espace local (visible par le nuanceur) tant que SetxxxShaderConstants n’est pas appelé.
-   Pour Direct3D 8, les constantes définies avec defx ou les API attribuent des valeurs à l’espace de constante de nuanceur. Chaque fois que le nuanceur est exécuté, les constantes sont utilisées par le nuanceur actuel, quelle que soit la technique utilisée pour les définir.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Registres de nuanceur vertex](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 
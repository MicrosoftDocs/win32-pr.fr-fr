---
title: Registre à virgule flottante constante (référence PS HLSL)
description: Registre d’entrée de nuanceur de pixels pour une constante à virgule flottante 4D.
ms.assetid: e4f46a48-c81e-4105-901b-332b92fa6195
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 05bb382b745d172ea4b81f9920154e7c79a58c2d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382392"
---
# <a name="constant-float-register-hlsl-ps-reference"></a>Registre à virgule flottante constante (référence PS HLSL)

Registre d’entrée de nuanceur de pixels pour une constante à virgule flottante 4D.

Ils peuvent être définis à l’aide [de def-PS](def---ps.md) ou [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).

Le comportement des constantes de nuanceur a changé entre Direct3D 8 et Direct3D 9.

-   Pour Direct3D 9, les constantes définies avec defx affectent des valeurs à l’espace constant du nuanceur. La durée de vie d’une constante déclarée avec defx est limitée à l’exécution de ce nuanceur uniquement. À l’inverse, les constantes définies à l’aide des API SetXXXShaderConstantX initialisent des constantes dans l’espace global. Les constantes dans l’espace global ne sont pas copiées dans l’espace local (visible par le nuanceur) tant que SetxxxShaderConstants n’est pas appelé.
-   Pour Direct3D 8, les constantes définies avec defx ou les API attribuent des valeurs à l’espace de constante de nuanceur. Chaque fois que le nuanceur est exécuté, les constantes sont utilisées par le nuanceur actuel, quelle que soit la technique utilisée pour les définir.

## <a name="examples"></a>Exemples

Voici un exemple de déclaration de deux constantes à virgule flottante dans un nuanceur.


```
def c40, 0.0f,0.0f,0.0f,0.0f;
```



Ces constantes sont chargées chaque fois que [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader) est appelé.

Si vous définissez des valeurs constantes avec l’API, aucune déclaration de nuanceur n’est requise.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscrit](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 
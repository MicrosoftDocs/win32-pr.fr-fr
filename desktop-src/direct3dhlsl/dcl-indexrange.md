---
title: dcl_indexRange (SM4-ASM)
description: DCL \_ indexRange (SM4-ASM)
ms.assetid: 88af30f3-dbf9-4556-b170-a7371680f9b9
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6fe587c3a5cfeae21b5da09a2dd79b67b82bc0c2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472065"
---
# <a name="dcl_indexrange-sm4---asm"></a>DCL \_ indexRange (SM4-ASM)

Déclare une plage de registres accessibles par index (un entier calculé dans le nuanceur).



| DCL \_ IndexRange *minRegisterM*, *maxRegisterN* |
|------------------------------------------------|



 




| Élément | Description | 
|------|-------------|
| <span id="minRegisterM"></span><span id="minregisterm"></span><span id="MINREGISTERM"></span><em>minRegisterM</em><br /> | dans Premier registre auquel accéder par index. <br /><ul><li><em>minRegister</em> est soit <strong>v</strong> pour un registre d’entrée de nuanceur de vertex ou de pixels, soit <strong>o</strong> pour un registre de sortie de nuanceur de sommets.</li><li><em>M</em> est un entier qui indique le numéro du Registre.</li></ul> | 
| <span id="maxRegisterN"></span><span id="maxregistern"></span><span id="MAXREGISTERN"></span><em>maxRegisterN</em><br /> | dans Dernier registre auquel accéder par index. Même forme que <em>minRegister</em> , sauf que <em>N</em> est le numéro du Registre.<br /> | 




 

Les restrictions suivantes s’appliquent à tous les registres :

-   Les registres min et Max doivent être du même type et avoir les mêmes masques de composant (si les masques sont déclarés).
-   Un registre peut avoir plusieurs plages d’index, à condition qu’elles ne se chevauchent pas.
-   Le numéro de Registre minimal doit être inférieur au nombre maximal de registres.
-   Un registre d’index ne peut pas contenir une [valeur système](dx-graphics-hlsl-semantics.md).
-   L’indexation d’un registre en dehors de la déclaration d’index max génère des résultats indéfinis.

Les registres d’entrée de nuanceur de pixels doivent utiliser le même mode d’interpolation ; les registres de sortie du nuanceur de pixels ne sont pas indexables.

Un registre d’entrée de nuanceur Geometry a deux dimensions (axe de vertex, axe d’attribut); la plage d’index s’applique uniquement à l’axe des attributs, car l’axe des vertex est toujours entièrement indexé.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Cette instruction est incluse pour faciliter le débogage d’un nuanceur dans l’assembly. vous ne pouvez pas créer de nuanceur dans un langage assembleur à l’aide du nuanceur modèle 4.

## <a name="example"></a>Exemple

Voici un exemple.


```
dcl_indexRange v1, v3
dcl_indexRange v4, v9
```



## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                              | Prise en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | Oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | Oui       |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | Oui       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 4 du nuanceur (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 






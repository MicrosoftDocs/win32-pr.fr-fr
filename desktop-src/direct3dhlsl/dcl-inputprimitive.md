---
title: dcl_inputPrimitive (SM4-ASM)
description: DCL \_ inputPrimitive (SM4-ASM)
ms.assetid: 86672fd3-7955-45ac-a8b2-a9cc8d1e8805
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0660fe4da14a20f074e4f04de8891fc0848f2597
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479895"
---
# <a name="dcl_inputprimitive-sm4---asm"></a>DCL \_ inputPrimitive (SM4-ASM)

Déclare le type primitif pour les entrées Geometry-Shader.



| \_ *type* de inputPrimitive DCL |
|----------------------------|



 




| Élément | Description | 
|------|-------------|
| <span id="type"></span><span id="TYPE"></span><em>entrer</em><br /> | dans Type primitif de données d’entrée, qui est l’un des éléments suivants : <br /><ul><li>liste <em>de points</em></li><li>liste <em>des lignes</em></li><li><em>triangle</em> -liste de triangles</li><li>Liste des lignes <em>line_adj</em> avec les données d’contiguïté</li><li><em>triangle_adj</em> liste de triangles avec données d’contiguïté</li></ul> | 




 

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
|               | x               |              |



 

Cette instruction est incluse pour faciliter le débogage d’un nuanceur dans l’assembly. vous ne pouvez pas créer de nuanceur dans un langage assembleur à l’aide du nuanceur modèle 4.

## <a name="example"></a>Exemple

Voici un exemple.


```
dcl_inputPrimitive triangle
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

 

 






---
title: dcl_maxOutputVertexCount (SM4-ASM)
description: DCL \_ maxOutputVertexCount (SM4-ASM)
ms.assetid: 91eb2dfc-f4ff-4f23-9cb4-ec5fdb676157
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ba7783575ac5782c63bc1ec3ca5f56f6ffe9a1bc7483f3f01ccbcf8adac5e23f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068519"
---
# <a name="dcl_maxoutputvertexcount-sm4---asm"></a>DCL \_ maxOutputVertexCount (SM4-ASM)

Déclare le nombre maximal de vertex qui peuvent être générés par un nuanceur Geometry.



| \_ *nombre* de maxOutputVertexCount DCL |
|-----------------------------------|



 



| Élément                                                               | Description                                                             |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="count"></span><span id="COUNT"></span>*saut*<br/> | \[dans \] un entier non signé 32 bits compris entre 1 et n, inclus.<br/> |



 

Un nuanceur Geometry peut générer un nombre maximal de valeurs de 1024 32 bits. Cette valeur maximale comprend la taille des données d’entrée et la taille des données créées par le nuanceur.

Voici quelques limitations :

-   Si le nombre de vertex est atteint avant la fin de l’exécution du nuanceur Geometry, le nuanceur se termine.
-   Un nuanceur Geometry peut atteindre la fin de son programme avant de sortir des vertex. Cela est parfaitement légal.
-   Si vous déboguez un nuanceur Geometry, vous pouvez indiquer le nombre de vertex générés en comptant le nombre d’instructions d’émission générées.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
|               | x               |              |



 

Cette instruction est incluse pour faciliter le débogage d’un nuanceur dans l’assembly. vous ne pouvez pas créer de nuanceur dans un langage assembleur à l’aide du nuanceur modèle 4.

## <a name="example"></a>Exemple

Voici quelques exemples.

Supposons que les données d’entrée se composent de positions (. XYZW) et de couleur (. RGB). Chaque composant consomme un octet ; à partir de 7 octets, le nombre maximal de vertex pouvant être générés par le nuanceur est de 1024/(4 + 3) = 146.


```
dcl_maxOutputVertexCount 146
```



Supposons que votre nuanceur Geometry crée des vecteurs de composant 32 4. Le nombre maximal de vertex que le nuanceur peut générer est 1024/(32 \* 4) = 8.


```
dcl_maxOutputVertexCount 8
```



## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                              | Pris en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | oui       |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | oui       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 4 du nuanceur (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 






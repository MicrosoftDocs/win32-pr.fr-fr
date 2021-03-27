---
title: dcl_outputTopology (SM4-ASM)
description: DCL \_ outputTopology (SM4-ASM)
ms.assetid: a03a6feb-ec34-4655-a68c-a91e31e7140b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e3b305d195ca09a1ef95c99624b47a50058021ca
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679182"
---
# <a name="dcl_outputtopology-sm4---asm"></a>DCL \_ outputTopology (SM4-ASM)

Déclare la géométrie du type primitif-données de sortie du nuanceur.



| \_ *type* de outputTopology DCL |
|----------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Élément</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Entrer</em><br/></td>
<td>dans Une topologie de primitive de sortie, qui est l’une des valeurs suivantes : <br/>
<ul>
<li><em>pointlist</em></li>
<li><em>linestrip</em></li>
<li><em>trianglestrip</em></li>
</ul></td>
</tr>
</tbody>
</table>



 

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
|               | x               |              |



 

Cette instruction est incluse pour faciliter le débogage d’un nuanceur dans l’assembly. vous ne pouvez pas créer de nuanceur dans un langage assembleur à l’aide du nuanceur modèle 4.

## <a name="example"></a>Exemple

Voici un exemple.


```
dcl_outputTopology trianglestrip
```



## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                              | Prise en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | Oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | Oui       |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | Oui       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 4 du nuanceur (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 






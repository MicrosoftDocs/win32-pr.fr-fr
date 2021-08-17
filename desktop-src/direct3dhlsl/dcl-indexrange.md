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
ms.openlocfilehash: a652d200a211eb5528f6e7ecdedf2cc20579817d1f0148d59855d1e864de55de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117727189"
---
# <a name="dcl_indexrange-sm4---asm"></a>DCL \_ indexRange (SM4-ASM)

Déclare une plage de registres accessibles par index (un entier calculé dans le nuanceur).



| DCL \_ IndexRange *minRegisterM*, *maxRegisterN* |
|------------------------------------------------|



 



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
<td><span id="minRegisterM"></span><span id="minregisterm"></span><span id="MINREGISTERM"></span><em>minRegisterM</em><br/></td>
<td>dans Premier registre auquel accéder par index. <br/>
<ul>
<li><em>minRegister</em> est soit <strong>v</strong> pour un registre d’entrée de nuanceur de vertex ou de pixels, soit <strong>o</strong> pour un registre de sortie de nuanceur de sommets.</li>
<li><em>M</em> est un entier qui indique le numéro du Registre.</li>
</ul></td>
</tr>
<tr class="even">
<td><span id="maxRegisterN"></span><span id="maxregistern"></span><span id="MAXREGISTERN"></span><em>maxRegisterN</em><br/></td>
<td>dans Dernier registre auquel accéder par index. Même forme que <em>minRegister</em> , sauf que <em>N</em> est le numéro du Registre.<br/></td>
</tr>
</tbody>
</table>



 

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

 

 






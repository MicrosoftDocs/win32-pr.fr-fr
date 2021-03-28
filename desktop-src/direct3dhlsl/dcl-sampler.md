---
title: dcl_sampler (SM4-ASM)
description: '\_exemple de DCL (SM4-ASM)'
ms.assetid: 285a47fa-2d47-4ba9-90b9-3f4c61d5dce1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 45b6da3bcdb027a00edeb4f009773533424efeb8
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104383060"
---
# <a name="dcl_sampler-sm4---asm"></a>\_exemple de DCL (SM4-ASM)

Déclare un registre d’échantillonneur.



| DCL \_ sampler SN, mode |
|-----------------------|



 



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
<td><span id="sN"></span><span id="sn"></span><span id="SN"></span>s<em>N</em><br/></td>
<td>dans Un registre d’échantillonnage, où <em>N</em> est un entier qui désigne le numéro du Registre.<br/></td>
</tr>
<tr class="even">
<td><span id="mode"></span><span id="MODE"></span><em>mode</em><br/></td>
<td>dans Mode échantillonneur qui limite les États de l’échantillonneur (répertoriés dans les membres de <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_sampler_desc"><strong>D3D10_SAMPLER_DESC</strong></a>) qui sont honorés. Les modes et les États sont répertoriés dans le tableau suivant.<br/> 
<table>
<thead>
<tr class="header">
<th>Mode</th>
<th>États de l’échantillonneur honorés</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>default</td>
<td><em>Filtre</em> (peut ne pas utiliser les valeurs _COMPARISON ou _TEXT), adsent <em>/V/W</em>, <em>MinLOD/MaxLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em>, <em>BorderColor [4]</em></td>
</tr>
<tr class="even">
<td>comparaison</td>
<td><em>Filter</em>, <em>ComparisonFunction</em>, adverse <em>/V/W</em>, <em>MinLOD, MaxLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em>, <em>BorderColor [4]</em></td>
</tr>
<tr class="odd">
<td>carbur</td>
<td><em>Filter</em> (doit être l’une des valeurs _TEXT), <em>MonoFilterWidth</em>, <em>MonoFilterHeight</em> (ces deux États sont l’état global du périphérique), <em>MinLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

Le mode limite les exemples d’instructions qui peuvent être utilisés. ce tableau répertorie les méthodes d’objet de texture prises en charge pour chaque mode.



| Un échantillonneur fonctionnant dans ce mode | Peut utiliser ces méthodes Texture-Object                                                                                                           |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| default                          | [Exemple](dx-graphics-hlsl-to-sample.md), [SampleLevel](dx-graphics-hlsl-to-samplelevel.md), [SampleGrad](dx-graphics-hlsl-to-samplegrad.md) |
| comparaison                       | [SampleCmp](dx-graphics-hlsl-to-samplecmp.md), [SampleCmpLevelZero](dx-graphics-hlsl-to-samplecmplevelzero.md)                               |
| carbur                             | [SampleLevel](dx-graphics-hlsl-to-samplelevel.md)                                                                                             |



 

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
| x             | x               | x\*          |



 

\* -L’utilisation d’un échantillonneur en mode mono est prise en charge uniquement dans un nuanceur de pixels.

Cette instruction est incluse pour faciliter le débogage d’un nuanceur dans l’assembly. vous ne pouvez pas créer de nuanceur dans un langage assembleur à l’aide du nuanceur modèle 4.

## <a name="example"></a>Exemple

Voici un exemple.


```
dcl_sampler s3, default
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

 


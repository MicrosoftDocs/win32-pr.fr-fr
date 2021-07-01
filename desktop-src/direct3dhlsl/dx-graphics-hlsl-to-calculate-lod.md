---
title: CalculateLevelOfDetail (objet texture HLSL DirectX)
description: Calcule le niveau de détail.
ms.assetid: 7c7c3754-45a9-49c6-8420-aac22f776b15
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9e307527f93c153f0f78ce58b4d70ead4f7c1bc4
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120554"
---
# <a name="calculatelevelofdetail-directx-hlsl-texture-object"></a>CalculateLevelOfDetail (objet texture HLSL DirectX)

Calcule le niveau de détail.

RET Object. CalculateLevelOfDetail (état de l’échantillonneur \_ S, float x);



 

## <a name="parameters"></a>Paramètres



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
<td><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Dessin</em><br/></td>
<td>Tout type d' <a href="dx-graphics-hlsl-to-type.md">objet texture</a> (sauf Texture2DMS et Texture2DMSArray).<br/></td>
</tr>
<tr class="even">
<td><span id="S"></span><span id="s"></span><em>X</em><br/></td>
<td>dans État de l' <a href="/windows/desktop/direct3d10/d3d10-effect-sampler-syntax">échantillonneur</a>. Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.<br/></td>
</tr>
<tr class="odd">
<td><span id="x"></span><span id="X"></span><em>x</em><br/></td>
<td>dans Valeur ou valeurs d’interpolation linéaire, qui est un nombre à virgule flottante compris entre 0,0 et 1,0 inclus. Le nombre de composants dépend du type d’objet texture. <br/> 
<table>
<thead>
<tr class="header">
<th>Type de Texture-Object</th>
<th>Type de paramètre</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture1D, Texture1DArray</td>
<td>float1</td>
</tr>
<tr class="even">
<td>Texture2D, Texture2DArray</td>
<td>float2</td>
</tr>
<tr class="odd">
<td>Texture3D, TextureCube, TextureCubeArray </td>
<td>float3</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a>Valeur renvoyée

Retourne le LOD calculé, une valeur à virgule flottante unique.

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | PS \_ 4 \_ 0 | PS \_ 4 \_ 1  | GS \_ 4 \_ 0 | GS \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           |          | x         |          |           |



 

1.  TextureCubeArray est disponible dans le nuancier modèle 4,1 ou version ultérieure.
2.  Le modèle de nuanceur 4,1 est disponible dans Direct3D 10,1 ou version ultérieure.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Texture-objet](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 


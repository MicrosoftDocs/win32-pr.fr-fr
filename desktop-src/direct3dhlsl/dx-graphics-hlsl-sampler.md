---
title: Type d’échantillonneur
description: Utilisez la syntaxe suivante pour déclarer l’état de l’échantillonneur ainsi que l’état de comparaison de l’échantillonneur.
ms.assetid: 6534d343-d724-46e5-b300-2a29124a1a28
keywords:
- Type d’échantillonneur HLSL
topic_type:
- apiref
api_name:
- Sampler Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ccdc81b21ba18fe3983a44655d23c9d463045b18
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624995"
---
# <a name="sampler-type"></a>Type d’échantillonneur

Utilisez la syntaxe suivante pour déclarer l’état de l’échantillonneur ainsi que l’état de comparaison de l’échantillonneur.



<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Différences entre Direct3D 9 et Direct3D 10 et versions ultérieures :<br/> Voici la syntaxe d’un échantillonneur dans Direct3D 9.<br/> 
<table>
<tbody>
<tr class="odd">
<td><em>nom</em>de l’échantillonneur  =  <em>SamplerType</em>{texture = <<em>texture_variable</em> > ;   [<em>state_name = state_value ;</em>]   ... };</td>
</tr>
</tbody>
</table>

<p> </p>
<p>La syntaxe d’un échantillonneur dans Direct3D 10 et les versions ultérieures est légèrement modifiée pour prendre en charge les objets texture et les tableaux d’échantillonneurs.</p>

<table>
<tbody>
<tr class="odd">
<td><em>SamplerType nom [index]</em>{[<em>state_name = state_value ;</em>]   ... };</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="sampler"></span><span id="SAMPLER"></span>échantillonneur
</dt> <dd>

Direct3D 9 uniquement. Mot clé requis.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nomme*
</dt> <dd>

Chaîne ASCII qui identifie de façon unique le nom de la variable d’échantillonneur.

</dd> <dt>

<span id="_Index_"></span><span id="_index_"></span><span id="_INDEX_"></span>*\[Évaluer\]*
</dt> <dd>

Direct3D 10 et versions ultérieures uniquement. Taille de tableau facultative ; entier positif supérieur ou égal à 1.

</dd> <dt>

<span id="SamplerType"></span><span id="samplertype"></span><span id="SAMPLERTYPE"></span>*SamplerType*
</dt> <dd>

\[dans \] le type d’échantillonneur, qui est l’un des suivants : *échantillonner*, *sampler1D*, *sampler2D*, *sampler3D*, *samplerCUBE*, état de l' *échantillonneur \_*, *SamplerState*.

Différences entre Direct3D 9 et Direct3D 10 et versions ultérieures :

- Direct3D 10 et versions ultérieures prennent en charge un type d’échantillonneur supplémentaire : *SamplerComparisonState*.



 

</dd> <dt>

<span id="Texture____texture_variable__"></span><span id="texture____texture_variable__"></span><span id="TEXTURE____TEXTURE_VARIABLE__"></span>*Texture* = <*> \_ variable de texture* ;
</dt> <dd>

Direct3D 9 uniquement. Variable de texture. Le mot clé de *texture* est obligatoire sur le côté gauche ; le nom de la variable appartient sur le côté droit de l’expression entre crochets pointus.

</dd> <dt>

<span id="state_name___state_value"></span><span id="STATE_NAME___STATE_VALUE"></span>*State \_ name = valeur d’état \_*
</dt> <dd>

\[dans le \] ou les affectations d’État facultatives. La partie gauche d’une assignation est un nom d’État, la partie droite est la valeur d’État. Toutes les attributions d’État doivent apparaître dans un bloc d’instructions (entre accolades). Chaque instruction est séparée par un point-virgule. Le tableau suivant répertorie les noms d’État possibles.


```
// sampler state
AddressU
AddressV
AddressW
BorderColor
Filter
MaxAnisotropy
MaxLOD
MinLOD
MipLODBias

// sampler-comparison state
ComparisonFunc
```



La partie droite de chaque expression correspond à la valeur affectée à chaque État. Consultez la structure DESC de l' [**\_ \_ échantillonneur d3d11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_sampler_desc) pour connaître les valeurs d’État possibles pour Direct3D 11. Il y a une relation 1 à 1 entre les noms d’État et les membres de la structure. Consultez l’exemple qui suit.

</dd> </dl>

## <a name="remarks"></a>Remarques

Lorsque vous implémentez un effet, l’état de l’échantillonneur est l’un des différents types d’État que vous devrez peut-être configurer dans le pipeline pour le rendu. Pour obtenir la liste de tous les États possibles que vous pouvez définir dans un effet, consultez :

-   Direct3D 10 utilise des [groupes d’États](/windows/desktop/direct3d10/d3d10-effect-states).
-   Direct3D 9 utilise des [États](/windows/desktop/direct3d9/effect-states)individuels.

## <a name="example"></a>Exemple



<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Différences entre Direct3D 9 et Direct3D 10 :<br/> Voici un exemple partiel d’un échantillonneur Direct3D 9 issu de l’exemple <a href="https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx">BasicHLSL</a>.<br/> <span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>sampler MeshTextureSampler = 
sampler_state
{
    Texture = <g_MeshTexture>;
    MipFilter = LINEAR;
    MinFilter = LINEAR;
    MagFilter = LINEAR;
};</code></pre></td>
</tr>
</tbody>
</table>

<p>Voici un exemple partiel d’un échantillonneur Direct3D 10 à partir de l' <a href="https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx">exemple BasicHLSL10</a>.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

Voici un exemple partiel de la déclaration de l’état de comparaison de l’échantillonneur et de l’appel d’un échantillonneur de comparaison dans Direct3D 10.


```
SamplerComparisonState ShadowSampler
{
   // sampler state
   Filter = COMPARISON_MIN_MAG_LINEAR_MIP_POINT;
   AddressU = MIRROR;
   AddressV = MIRROR;

   // sampler comparison state
   ComparisonFunc = LESS;
};
        
float3 vModProjUV;
  ...
float fShadow = g_ShadowMap.SampleCmpLevelZero( ShadowSampler, vModProjUV.xy, vModProjUV.z);
```



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types de données (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 


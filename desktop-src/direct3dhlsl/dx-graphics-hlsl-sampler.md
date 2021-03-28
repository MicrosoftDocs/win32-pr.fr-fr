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
ms.openlocfilehash: fe3cd51c81617632d240dd06df5c8f61b103bf91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031266"
---
# <a name="sampler-type"></a><span data-ttu-id="89b78-104">Type d’échantillonneur</span><span class="sxs-lookup"><span data-stu-id="89b78-104">Sampler Type</span></span>

<span data-ttu-id="89b78-105">Utilisez la syntaxe suivante pour déclarer l’état de l’échantillonneur ainsi que l’état de comparaison de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="89b78-105">Use the following syntax to declare sampler state as well as sampler-comparison state.</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="89b78-106">Différences entre Direct3D 9 et Direct3D 10 et versions ultérieures :</span><span class="sxs-lookup"><span data-stu-id="89b78-106">Differences between Direct3D 9 and Direct3D 10 and later:</span></span><br/> <span data-ttu-id="89b78-107">Voici la syntaxe d’un échantillonneur dans Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="89b78-107">Here is the syntax for a sampler in Direct3D 9.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="89b78-108"><em>nom</em>de l’échantillonneur  =  <em>SamplerType</em>{texture = <<em>texture_variable</em> > ;   [<em>state_name = state_value ;</em>]   ... };</span><span class="sxs-lookup"><span data-stu-id="89b78-108">sampler <em>Name</em> = <em>SamplerType</em>{   Texture = <<em>texture_variable</em>>;   [<em>state_name = state_value;</em>]   ... };</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="89b78-109">La syntaxe d’un échantillonneur dans Direct3D 10 et les versions ultérieures est légèrement modifiée pour prendre en charge les objets texture et les tableaux d’échantillonneurs.</span><span class="sxs-lookup"><span data-stu-id="89b78-109">The syntax for a sampler in Direct3D 10 and later is changed slightly to support texture objects and sampler arrays.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="89b78-110"><em>SamplerType nom [index]</em>{[<em>state_name = state_value ;</em>]   ... };</span><span class="sxs-lookup"><span data-stu-id="89b78-110"><em>SamplerType Name[Index]</em>{   [<em>state_name = state_value;</em>]   ... };</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="parameters"></a><span data-ttu-id="89b78-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89b78-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89b78-112"><span id="sampler"></span><span id="SAMPLER"></span>échantillonneur</span><span class="sxs-lookup"><span data-stu-id="89b78-112"><span id="sampler"></span><span id="SAMPLER"></span>sampler</span></span>
</dt> <dd>

<span data-ttu-id="89b78-113">Direct3D 9 uniquement.</span><span class="sxs-lookup"><span data-stu-id="89b78-113">Direct3D 9 only.</span></span> <span data-ttu-id="89b78-114">Mot clé requis.</span><span class="sxs-lookup"><span data-stu-id="89b78-114">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="89b78-115"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nomme*</span><span class="sxs-lookup"><span data-stu-id="89b78-115"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="89b78-116">Chaîne ASCII qui identifie de façon unique le nom de la variable d’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="89b78-116">ASCII string that uniquely identifies the sampler variable name.</span></span>

</dd> <dt>

<span data-ttu-id="89b78-117"><span id="_Index_"></span><span id="_index_"></span><span id="_INDEX_"></span>*\[Évaluer\]*</span><span class="sxs-lookup"><span data-stu-id="89b78-117"><span id="_Index_"></span><span id="_index_"></span><span id="_INDEX_"></span>*\[Index\]*</span></span>
</dt> <dd>

<span data-ttu-id="89b78-118">Direct3D 10 et versions ultérieures uniquement.</span><span class="sxs-lookup"><span data-stu-id="89b78-118">Direct3D 10 and later only.</span></span> <span data-ttu-id="89b78-119">Taille de tableau facultative ; entier positif supérieur ou égal à 1.</span><span class="sxs-lookup"><span data-stu-id="89b78-119">Optional array size; a positive integer greater than or equal to 1.</span></span>

</dd> <dt>

<span data-ttu-id="89b78-120"><span id="SamplerType"></span><span id="samplertype"></span><span id="SAMPLERTYPE"></span>*SamplerType*</span><span class="sxs-lookup"><span data-stu-id="89b78-120"><span id="SamplerType"></span><span id="samplertype"></span><span id="SAMPLERTYPE"></span>*SamplerType*</span></span>
</dt> <dd>

<span data-ttu-id="89b78-121">\[dans \] le type d’échantillonneur, qui est l’un des suivants : *échantillonner*, *sampler1D*, *sampler2D*, *sampler3D*, *samplerCUBE*, état de l' *échantillonneur \_*, *SamplerState*.</span><span class="sxs-lookup"><span data-stu-id="89b78-121">\[in\] The sampler type, which is one of the following: *sampler*, *sampler1D*, *sampler2D*, *sampler3D*, *samplerCUBE*, *sampler\_state*, *SamplerState*.</span></span>



|                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89b78-122">Différences entre Direct3D 9 et Direct3D 10 et versions ultérieures :</span><span class="sxs-lookup"><span data-stu-id="89b78-122">Differences between Direct3D 9 and Direct3D 10 and later:</span></span><br/> <span data-ttu-id="89b78-123">Direct3D 10 et versions ultérieures prennent en charge un type d’échantillonneur supplémentaire : *SamplerComparisonState*.</span><span class="sxs-lookup"><span data-stu-id="89b78-123">Direct3D 10 and later supports one additional sampler type: *SamplerComparisonState*.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="89b78-124"><span id="Texture____texture_variable__"></span><span id="texture____texture_variable__"></span><span id="TEXTURE____TEXTURE_VARIABLE__"></span>*Texture* = <*> \_ variable de texture* ;</span><span class="sxs-lookup"><span data-stu-id="89b78-124"><span id="Texture____texture_variable__"></span><span id="texture____texture_variable__"></span><span id="TEXTURE____TEXTURE_VARIABLE__"></span>*Texture* = <*texture\_variable*>;</span></span>
</dt> <dd>

<span data-ttu-id="89b78-125">Direct3D 9 uniquement.</span><span class="sxs-lookup"><span data-stu-id="89b78-125">Direct3D 9 only.</span></span> <span data-ttu-id="89b78-126">Variable de texture.</span><span class="sxs-lookup"><span data-stu-id="89b78-126">A texture variable.</span></span> <span data-ttu-id="89b78-127">Le mot clé de *texture* est obligatoire sur le côté gauche ; le nom de la variable appartient sur le côté droit de l’expression entre crochets pointus.</span><span class="sxs-lookup"><span data-stu-id="89b78-127">The *Texture* keyword is required on the left-hand side; the variable name belongs on the right-hand side of the expression within the angle brackets.</span></span>

</dd> <dt>

<span data-ttu-id="89b78-128"><span id="state_name___state_value"></span><span id="STATE_NAME___STATE_VALUE"></span>*State \_ name = valeur d’état \_*</span><span class="sxs-lookup"><span data-stu-id="89b78-128"><span id="state_name___state_value"></span><span id="STATE_NAME___STATE_VALUE"></span>*state\_name = state\_value*</span></span>
</dt> <dd>

<span data-ttu-id="89b78-129">\[dans le \] ou les affectations d’État facultatives.</span><span class="sxs-lookup"><span data-stu-id="89b78-129">\[in\] Optional state assignment(s).</span></span> <span data-ttu-id="89b78-130">La partie gauche d’une assignation est un nom d’État, la partie droite est la valeur d’État.</span><span class="sxs-lookup"><span data-stu-id="89b78-130">The left hand side of an assignment is a state name, the right hand side is the state value.</span></span> <span data-ttu-id="89b78-131">Toutes les attributions d’État doivent apparaître dans un bloc d’instructions (entre accolades).</span><span class="sxs-lookup"><span data-stu-id="89b78-131">All state assignments must appear within a statement block (in curly brackets).</span></span> <span data-ttu-id="89b78-132">Chaque instruction est séparée par un point-virgule.</span><span class="sxs-lookup"><span data-stu-id="89b78-132">Each statement is separated with a semicolon.</span></span> <span data-ttu-id="89b78-133">Le tableau suivant répertorie les noms d’État possibles.</span><span class="sxs-lookup"><span data-stu-id="89b78-133">The following table lists the possible state names.</span></span>


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



<span data-ttu-id="89b78-134">La partie droite de chaque expression correspond à la valeur affectée à chaque État.</span><span class="sxs-lookup"><span data-stu-id="89b78-134">The right side of each expression is the value assigned to each state.</span></span> <span data-ttu-id="89b78-135">Consultez la structure DESC de l' [**\_ \_ échantillonneur d3d11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_sampler_desc) pour connaître les valeurs d’État possibles pour Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="89b78-135">See the [**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_sampler_desc) structure for the possible state values for Direct3D 11.</span></span> <span data-ttu-id="89b78-136">Il y a une relation 1 à 1 entre les noms d’État et les membres de la structure.</span><span class="sxs-lookup"><span data-stu-id="89b78-136">There is a 1 to 1 relationship between the state names and the members of the structure.</span></span> <span data-ttu-id="89b78-137">Consultez l’exemple qui suit.</span><span class="sxs-lookup"><span data-stu-id="89b78-137">See the following example.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="89b78-138">Notes</span><span class="sxs-lookup"><span data-stu-id="89b78-138">Remarks</span></span>

<span data-ttu-id="89b78-139">Lorsque vous implémentez un effet, l’état de l’échantillonneur est l’un des différents types d’État que vous devrez peut-être configurer dans le pipeline pour le rendu.</span><span class="sxs-lookup"><span data-stu-id="89b78-139">When you implement an effect, sampler state is one of several types of state that you might need to set up in the pipeline for rendering.</span></span> <span data-ttu-id="89b78-140">Pour obtenir la liste de tous les États possibles que vous pouvez définir dans un effet, consultez :</span><span class="sxs-lookup"><span data-stu-id="89b78-140">For a list of all the possible states that you can set in an effect, see:</span></span>

-   <span data-ttu-id="89b78-141">Direct3D 10 utilise des [groupes d’États](/windows/desktop/direct3d10/d3d10-effect-states).</span><span class="sxs-lookup"><span data-stu-id="89b78-141">Direct3D 10 uses [state groups](/windows/desktop/direct3d10/d3d10-effect-states).</span></span>
-   <span data-ttu-id="89b78-142">Direct3D 9 utilise des [États](/windows/desktop/direct3d9/effect-states)individuels.</span><span class="sxs-lookup"><span data-stu-id="89b78-142">Direct3D 9 uses individual [states](/windows/desktop/direct3d9/effect-states).</span></span>

## <a name="example"></a><span data-ttu-id="89b78-143">Exemple</span><span class="sxs-lookup"><span data-stu-id="89b78-143">Example</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="89b78-144">Différences entre Direct3D 9 et Direct3D 10 :</span><span class="sxs-lookup"><span data-stu-id="89b78-144">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="89b78-145">Voici un exemple partiel d’un échantillonneur Direct3D 9 issu de l’exemple <a href="https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx">BasicHLSL</a>.</span><span class="sxs-lookup"><span data-stu-id="89b78-145">Here is a partial example of a Direct3D 9 sampler from <a href="https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx">BasicHLSL Sample</a>.</span></span><br/> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
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

<p><span data-ttu-id="89b78-146">Voici un exemple partiel d’un échantillonneur Direct3D 10 à partir de l' <a href="https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx">exemple BasicHLSL10</a>.</span><span class="sxs-lookup"><span data-stu-id="89b78-146">Here is a partial example of a Direct3D 10 sampler from <a href="https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx">BasicHLSL10 Sample</a>.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
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



 

<span data-ttu-id="89b78-147">Voici un exemple partiel de la déclaration de l’état de comparaison de l’échantillonneur et de l’appel d’un échantillonneur de comparaison dans Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="89b78-147">Here is a partial example of declaring sampler-comparison state, and calling a comparison sampler in Direct3D 10.</span></span>


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



## <a name="see-also"></a><span data-ttu-id="89b78-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89b78-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89b78-149">Types de données (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="89b78-149">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 


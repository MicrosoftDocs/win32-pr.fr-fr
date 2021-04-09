---
description: Une technique d’effet est déclarée avec la syntaxe suivante.
ms.assetid: 84f9b74d-8397-4cd5-91a0-7f910ba7b19e
title: Syntaxe d’effet technique (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f781a0e1ea247e9ffae02e6afc9de77c8e0c6b68
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110542"
---
# <a name="effect-technique-syntax-direct3d-10"></a><span data-ttu-id="39c93-103">Syntaxe d’effet technique (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="39c93-103">Effect Technique Syntax (Direct3D 10)</span></span>

<span data-ttu-id="39c93-104">Une technique d’effet est déclarée avec la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="39c93-104">An effect technique is declared with the following syntax.</span></span>

<span data-ttu-id="39c93-105"> \[  < *Annotations* TechniqueName technique10 > \]</span><span class="sxs-lookup"><span data-stu-id="39c93-105">technique10 *TechniqueName* \[ <*Annotations* > \]</span></span>

<span data-ttu-id="39c93-106">{</span><span class="sxs-lookup"><span data-stu-id="39c93-106">{</span></span>

<dl> <span data-ttu-id="39c93-107">passer  des \[  < *Annotations* PassName > \]</span><span class="sxs-lookup"><span data-stu-id="39c93-107">pass *PassName* \[ <*Annotations* > \]</span></span>  
<span data-ttu-id="39c93-108">{</span><span class="sxs-lookup"><span data-stu-id="39c93-108">{</span></span>
<dl> <span data-ttu-id="39c93-109">\[*SetStateGroup*; \] \[ *SetStateGroup*;\]</span><span class="sxs-lookup"><span data-stu-id="39c93-109">\[ *SetStateGroup*; \] \[ *SetStateGroup*; \]</span></span>  
<span data-ttu-id="39c93-110">...</span><span class="sxs-lookup"><span data-stu-id="39c93-110">...</span></span>  
<span data-ttu-id="39c93-111">\[*SetStateGroup*;\]</span><span class="sxs-lookup"><span data-stu-id="39c93-111">\[ *SetStateGroup*; \]</span></span>
</dl> </dd> }  
</dl>

<span data-ttu-id="39c93-112">}</span><span class="sxs-lookup"><span data-stu-id="39c93-112">}</span></span>

## <a name="parameters"></a><span data-ttu-id="39c93-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39c93-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39c93-114"><span id="technique10"></span><span id="TECHNIQUE10"></span>technique10</span><span class="sxs-lookup"><span data-stu-id="39c93-114"><span id="technique10"></span><span id="TECHNIQUE10"></span>technique10</span></span>
</dt> <dd>

<span data-ttu-id="39c93-115">Mot clé requis.</span><span class="sxs-lookup"><span data-stu-id="39c93-115">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="39c93-116"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>*TechniqueName*</span><span class="sxs-lookup"><span data-stu-id="39c93-116"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>*TechniqueName*</span></span>
</dt> <dd>

<span data-ttu-id="39c93-117">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="39c93-117">Optional.</span></span> <span data-ttu-id="39c93-118">Chaîne ASCII qui identifie de façon unique le nom de la technique d’effet.</span><span class="sxs-lookup"><span data-stu-id="39c93-118">An ASCII string that uniquely identifies the name of the effect technique.</span></span>

</dd> <dt>

<span data-ttu-id="39c93-119"><span id="Annotations"></span><span id="annotations"></span><span id="ANNOTATIONS"></span>*Annotations*</span><span class="sxs-lookup"><span data-stu-id="39c93-119"><span id="Annotations"></span><span id="annotations"></span><span id="ANNOTATIONS"></span>*Annotations*</span></span>
</dt> <dd>

<span data-ttu-id="39c93-120">\[\]facultatif.</span><span class="sxs-lookup"><span data-stu-id="39c93-120">\[in\] Optional.</span></span> <span data-ttu-id="39c93-121">Un ou plusieurs éléments d’informations fournies par l’utilisateur (métadonnées) qui sont ignorés par le système d’effet.</span><span class="sxs-lookup"><span data-stu-id="39c93-121">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="39c93-122">Pour obtenir la syntaxe, consultez [syntaxe d’annotation (Direct3D 10)](d3d10-effect-annotation-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="39c93-122">For syntax, see [Annotation Syntax (Direct3D 10)](d3d10-effect-annotation-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="39c93-123"><span id="pass"></span><span id="PASS"></span>directes</span><span class="sxs-lookup"><span data-stu-id="39c93-123"><span id="pass"></span><span id="PASS"></span>pass</span></span>
</dt> <dd>

<span data-ttu-id="39c93-124">Mot clé requis.</span><span class="sxs-lookup"><span data-stu-id="39c93-124">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="39c93-125"><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span>*PassName*</span><span class="sxs-lookup"><span data-stu-id="39c93-125"><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span>*PassName*</span></span>
</dt> <dd>

<span data-ttu-id="39c93-126">\[\]facultatif.</span><span class="sxs-lookup"><span data-stu-id="39c93-126">\[in\] Optional.</span></span> <span data-ttu-id="39c93-127">Chaîne ASCII qui identifie de façon unique le nom de la passe.</span><span class="sxs-lookup"><span data-stu-id="39c93-127">An ASCII string that uniquely identifies the name of the pass.</span></span>

</dd> <dt>

<span data-ttu-id="39c93-128"><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span>*SetStateGroup*</span><span class="sxs-lookup"><span data-stu-id="39c93-128"><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span>*SetStateGroup*</span></span>
</dt> <dd>

<span data-ttu-id="39c93-129">\[dans, \] définissez un ou plusieurs groupes d’États tels que :</span><span class="sxs-lookup"><span data-stu-id="39c93-129">\[in\] Set one or more state groups such as:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39c93-130">StateGroup</span><span class="sxs-lookup"><span data-stu-id="39c93-130">StateGroup</span></span></th>
<th><span data-ttu-id="39c93-131">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39c93-131">Syntax</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="39c93-132">État de fusion</span><span class="sxs-lookup"><span data-stu-id="39c93-132">Blend State</span></span></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetBlendState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="39c93-133">Consultez [<strong>OMSetBlendState</strong>] (/Windows/Desktop/API/D3D10/NF-D3D10-id3d10device-omsetblendstate) pour la liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="39c93-133">See [<strong>OMSetBlendState</strong>](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetblendstate) for the argument list.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39c93-134">État du stencil de profondeur</span><span class="sxs-lookup"><span data-stu-id="39c93-134">Depth-stencil State</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetDepthStencilState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="39c93-135">Consultez <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetdepthstencilstate"><strong>OMSetDepthStencilState</strong></a> pour obtenir la liste des arguments.</span><span class="sxs-lookup"><span data-stu-id="39c93-135">See <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetdepthstencilstate"><strong>OMSetDepthStencilState</strong></a> for the argument list.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39c93-136">État du rastériseur</span><span class="sxs-lookup"><span data-stu-id="39c93-136">Rasterizer State</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetRasterizerState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="39c93-137">Consultez [<strong>RSSetState</strong>] (/Windows/Desktop/API/D3D10/NF-D3D10-id3d10device-rssetstate) pour la liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="39c93-137">See [<strong>RSSetState</strong>](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-rssetstate) for the argument list.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39c93-138">État du nuanceur</span><span class="sxs-lookup"><span data-stu-id="39c93-138">Shader State</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( CompileShader( shader_profile, ShaderFunction( args ) ) );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="39c93-139">or</span><span class="sxs-lookup"><span data-stu-id="39c93-139">or</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( CompileShader( NULL ) );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="39c93-140">or</span><span class="sxs-lookup"><span data-stu-id="39c93-140">or</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( NULL );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="39c93-141">SetXXXShader est l’un des <strong>SetVertexShader</strong>, <strong>SetGeometryShader</strong>ou <strong>SetPixelShader</strong> (qui sont similaires aux méthodes d’API <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader"><strong>VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetshader"><strong>GSSetShader</strong></a>et <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetshader"><strong>PSSetShader</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="39c93-141">SetXXXShader is one of <strong>SetVertexShader</strong>, <strong>SetGeometryShader</strong>, or <strong>SetPixelShader</strong> (which are similar to the API methods <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader"><strong>VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetshader"><strong>GSSetShader</strong></a>, and <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetshader"><strong>PSSetShader</strong></a>).</span></span></p></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

<span data-ttu-id="39c93-142">Les groupes d’États d’effet sont répertoriés en [État d’effet](d3d10-effect-states.md).</span><span class="sxs-lookup"><span data-stu-id="39c93-142">Effect state groups are listed in [effect state](d3d10-effect-states.md).</span></span>

## <a name="examples"></a><span data-ttu-id="39c93-143">Exemples</span><span class="sxs-lookup"><span data-stu-id="39c93-143">Examples</span></span>

<span data-ttu-id="39c93-144">Cet exemple (de l' [exemple CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) définit l’état de fusion.</span><span class="sxs-lookup"><span data-stu-id="39c93-144">This example (from [CubeMapGS sample](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) sets blending state.</span></span>


```
BlendState NoBlend
{ 
    BlendEnable[0] = False;
};

...

technique10
{
    pass p2 
    {
        ...
        SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
    }
}
```



<span data-ttu-id="39c93-145">Cet exemple configure l’état du rastériseur pour afficher un objet en mode filaire.</span><span class="sxs-lookup"><span data-stu-id="39c93-145">This example sets up the rasterizer state to render an object in wireframe.</span></span>


```
RasterizerState rsWireframe { FillMode = WireFrame; };

...

technique10
{
    pass p1 
    {
        ....
        SetRasterizerState( rsWireframe );
    }
}
```



<span data-ttu-id="39c93-146">Cet exemple définit l’état du nuanceur (à partir de l' [exemple BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)); qui utilise un nuanceur de sommets et de pixels.</span><span class="sxs-lookup"><span data-stu-id="39c93-146">This example sets shader state (from [BasicHLSL10 sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)); which uses a vertex and pixel shader.</span></span>


```
technique10 RenderSceneWithTexture1Light
{
    pass P0
    {
        SetVertexShader( CompileShader( vs_4_0, RenderSceneVS( 1, true, true ) ) );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, RenderScenePS( true ) ) );
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="39c93-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="39c93-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39c93-148">Format d’effet</span><span class="sxs-lookup"><span data-stu-id="39c93-148">Effect Format</span></span>](d3d10-effect-format.md)
</dt> </dl>

 

 




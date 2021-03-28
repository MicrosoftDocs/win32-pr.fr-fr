---
title: Syntaxe d’effet technique (Direct3D 11)
description: Une technique d’effet est déclarée avec la syntaxe décrite dans cette section.
ms.assetid: 54a6ebd1-a6b4-473b-bf53-a3323445de71
keywords:
- technique11, effet Direct3D 11
- réussite, effet Direct3D 11
- CompileShader, effet Direct3D 11
- SetStateGroup, effet Direct3D 11
- SetBlendState, effet Direct3D 11
- SetDepthStencilState, effet Direct3D 11
- SetRasterizerState, effet Direct3D 11
- SetVertexShader, effet Direct3D 11
- SetGeometryShader, effet Direct3D 11
- SetPixelShader, effet Direct3D 11
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73fb668f308869ef9cca5cce99d522f18a287f3c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101109"
---
# <a name="effect-technique-syntax-direct3d-11"></a><span data-ttu-id="a06e7-113">Syntaxe d’effet technique (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="a06e7-113">Effect Technique Syntax (Direct3D 11)</span></span>

<span data-ttu-id="a06e7-114">Une technique d’effet est déclarée avec la syntaxe décrite dans cette section.</span><span class="sxs-lookup"><span data-stu-id="a06e7-114">An effect technique is declared with the syntax described in this section.</span></span>

<span data-ttu-id="a06e7-115"> \[  < *Annotations* TechniqueName TechniqueVersion > \]</span><span class="sxs-lookup"><span data-stu-id="a06e7-115">TechniqueVersion *TechniqueName* \[ <*Annotations* > \]</span></span>

<span data-ttu-id="a06e7-116">{</span><span class="sxs-lookup"><span data-stu-id="a06e7-116">{</span></span>

<dl> <span data-ttu-id="a06e7-117">passer  des \[  < *Annotations* PassName > \]</span><span class="sxs-lookup"><span data-stu-id="a06e7-117">pass *PassName* \[ <*Annotations* > \]</span></span>  
<span data-ttu-id="a06e7-118">{</span><span class="sxs-lookup"><span data-stu-id="a06e7-118">{</span></span>
<dl> <span data-ttu-id="a06e7-119">\[*SetStateGroup*; \] \[ *SetStateGroup*;\]</span><span class="sxs-lookup"><span data-stu-id="a06e7-119">\[ *SetStateGroup*; \] \[ *SetStateGroup*; \]</span></span>  
<span data-ttu-id="a06e7-120">...</span><span class="sxs-lookup"><span data-stu-id="a06e7-120">...</span></span>  
<span data-ttu-id="a06e7-121">\[*SetStateGroup*;\]</span><span class="sxs-lookup"><span data-stu-id="a06e7-121">\[ *SetStateGroup*; \]</span></span>
</dl> </dd> }  
</dl>

<span data-ttu-id="a06e7-122">}</span><span class="sxs-lookup"><span data-stu-id="a06e7-122">}</span></span>

## <a name="parameters"></a><span data-ttu-id="a06e7-123">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a06e7-123">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a06e7-124">Élément</span><span class="sxs-lookup"><span data-stu-id="a06e7-124">Item</span></span></th>
<th><span data-ttu-id="a06e7-125">Description</span><span class="sxs-lookup"><span data-stu-id="a06e7-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a06e7-126"><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion</span><span class="sxs-lookup"><span data-stu-id="a06e7-126"><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion</span></span><br/></td>
<td><span data-ttu-id="a06e7-127">Technique10 ou technique11.</span><span class="sxs-lookup"><span data-stu-id="a06e7-127">Either technique10 or technique11.</span></span> <span data-ttu-id="a06e7-128">Les techniques qui utilisent les nouvelles fonctionnalités de Direct3D 11 (nuanceurs 5_0, BindInterfaces, etc.) doivent utiliser technique11.</span><span class="sxs-lookup"><span data-stu-id="a06e7-128">Techniques which use functionality new to Direct3D 11 (5_0 shaders, BindInterfaces, etc) must use technique11.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a06e7-129"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span><em>TechniqueName</em></span><span class="sxs-lookup"><span data-stu-id="a06e7-129"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span><em>TechniqueName</em></span></span><br/></td>
<td><span data-ttu-id="a06e7-130">facultatif.</span><span class="sxs-lookup"><span data-stu-id="a06e7-130">Optional.</span></span> <span data-ttu-id="a06e7-131">Chaîne ASCII qui identifie de façon unique le nom de la technique d’effet.</span><span class="sxs-lookup"><span data-stu-id="a06e7-131">An ASCII string that uniquely identifies the name of the effect technique.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a06e7-132"><span id="______________Annotations__"></span><span id="______________annotations__"></span><span id="______________ANNOTATIONS__"></span> <<em>Annotations</em> ></span><span class="sxs-lookup"><span data-stu-id="a06e7-132"><span id="______________Annotations__"></span><span id="______________annotations__"></span><span id="______________ANNOTATIONS__"></span> <<em>Annotations</em> ></span></span><br/></td>
<td><span data-ttu-id="a06e7-133">[in] Facultatif.</span><span class="sxs-lookup"><span data-stu-id="a06e7-133">[in] Optional.</span></span> <span data-ttu-id="a06e7-134">Un ou plusieurs éléments d’informations fournies par l’utilisateur (métadonnées) qui sont ignorés par le système d’effet.</span><span class="sxs-lookup"><span data-stu-id="a06e7-134">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="a06e7-135">Pour obtenir la syntaxe, consultez <a href="d3d11-effect-annotation-syntax.md">syntaxe d’annotation (Direct3D 11)</a>.</span><span class="sxs-lookup"><span data-stu-id="a06e7-135">For syntax, see <a href="d3d11-effect-annotation-syntax.md">Annotation Syntax (Direct3D 11)</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a06e7-136"><span id="pass"></span><span id="PASS"></span>directes</span><span class="sxs-lookup"><span data-stu-id="a06e7-136"><span id="pass"></span><span id="PASS"></span>pass</span></span><br/></td>
<td><span data-ttu-id="a06e7-137">Mot clé requis.</span><span class="sxs-lookup"><span data-stu-id="a06e7-137">Required keyword.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a06e7-138"><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span><em>PassName</em></span><span class="sxs-lookup"><span data-stu-id="a06e7-138"><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span><em>PassName</em></span></span><br/></td>
<td><span data-ttu-id="a06e7-139">[in] Facultatif.</span><span class="sxs-lookup"><span data-stu-id="a06e7-139">[in] Optional.</span></span> <span data-ttu-id="a06e7-140">Chaîne ASCII qui identifie de façon unique le nom de la passe.</span><span class="sxs-lookup"><span data-stu-id="a06e7-140">An ASCII string that uniquely identifies the name of the pass.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a06e7-141"><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span><em>SetStateGroup</em></span><span class="sxs-lookup"><span data-stu-id="a06e7-141"><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span><em>SetStateGroup</em></span></span><br/></td>
<td><span data-ttu-id="a06e7-142">dans Définissez un ou plusieurs groupes d’États tels que :</span><span class="sxs-lookup"><span data-stu-id="a06e7-142">[in] Set one or more state groups such as:</span></span> <br/> 
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a06e7-143">StateGroup</span><span class="sxs-lookup"><span data-stu-id="a06e7-143">StateGroup</span></span></th>
<th><span data-ttu-id="a06e7-144">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a06e7-144">Syntax</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a06e7-145">État de fusion</span><span class="sxs-lookup"><span data-stu-id="a06e7-145">Blend State</span></span></td>
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

<p><span data-ttu-id="a06e7-146">Consultez [<strong>ID3D11DeviceContext :: OMSetBlendState</strong>] (/Windows/Desktop/API/d3d11/NF-d3d11-id3d11devicecontext-omsetblendstate) pour la liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="a06e7-146">See [<strong>ID3D11DeviceContext::OMSetBlendState</strong>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetblendstate) for the argument list.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a06e7-147">État du stencil de profondeur</span><span class="sxs-lookup"><span data-stu-id="a06e7-147">Depth-stencil State</span></span></td>
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
<p><span data-ttu-id="a06e7-148">Consultez <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate"><strong>ID3D11DeviceContext :: OMSetDepthStencilState</strong></a> pour obtenir la liste des arguments.</span><span class="sxs-lookup"><span data-stu-id="a06e7-148">See <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate"><strong>ID3D11DeviceContext::OMSetDepthStencilState</strong></a> for the argument list.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a06e7-149">État du rastériseur</span><span class="sxs-lookup"><span data-stu-id="a06e7-149">Rasterizer State</span></span></td>
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
<p><span data-ttu-id="a06e7-150">Consultez [<strong>ID3D11DeviceContext :: RSSetState</strong>] (/Windows/Desktop/API/d3d11/NF-d3d11-id3d11devicecontext-rssetstate) pour la liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="a06e7-150">See [<strong>ID3D11DeviceContext::RSSetState</strong>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetstate) for the argument list.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a06e7-151">État du nuanceur</span><span class="sxs-lookup"><span data-stu-id="a06e7-151">Shader State</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( Shader );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="a06e7-152">SetXXXShader est l’un des SetVertexShader, SetDomainShader, SetHullShader, SetGeometryShader, SetPixelShader ou SetComputeShader (qui sont similaires aux méthodes d’API <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader"><strong>ID3D11DeviceContext :: VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader"><strong>ID3D11DeviceContext ::D ssetshader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader"><strong>ID3D11DeviceContext :: HSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetshader"><strong>ID3D11DeviceContext :: GSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader"><strong>ID3D11DeviceContext ::P ssetshader</strong></a> et <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetshader"><strong>ID3D11DeviceContext :: CSSetShader</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="a06e7-152">SetXXXShader is one of SetVertexShader, SetDomainShader, SetHullShader, SetGeometryShader, SetPixelShader or SetComputeShader (which are similar to the API methods <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader"><strong>ID3D11DeviceContext::VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader"><strong>ID3D11DeviceContext::DSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader"><strong>ID3D11DeviceContext::HSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetshader"><strong>ID3D11DeviceContext::GSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader"><strong>ID3D11DeviceContext::PSSetShader</strong></a> and <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetshader"><strong>ID3D11DeviceContext::CSSetShader</strong></a>).</span></span></p>
<p><span data-ttu-id="a06e7-153">Le nuanceur est une variable de nuanceur, qui peut être obtenue de plusieurs façons :</span><span class="sxs-lookup"><span data-stu-id="a06e7-153">Shader is a shader variable, which can be obtained in many ways:</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( CompileShader( shader_profile, ShaderFunction( args ) ) );
SetXXXShader( CompileShader( NULL ) );
SetXXXShader( NULL );
SetXXXShader( myShaderVar );
SetXXXShader( myShaderArray[2] );
SetXXXShader( myShaderArray[uIndex] );
SetGeometryShader( ConstructGSWithSO( Shader, strStream0 ) );
SetGeometryShader( ConstructGSWithSO( Shader, strStream0, strStream1, strStream2, strStream3, RastStream ) );</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a06e7-154">État de la cible de rendu</span><span class="sxs-lookup"><span data-stu-id="a06e7-154">Render Target State</span></span></td>
<td><span data-ttu-id="a06e7-155">Valeurs possibles :</span><span class="sxs-lookup"><span data-stu-id="a06e7-155">One of:</span></span>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetRenderTargets( RTV0, DSV );
SetRenderTargets( RTV0, RTV1, DSV );
...
SetRenderTargets( RTV0, RTV1, RTV2, RTV3, RTV4, RTV5, RTV6, RTV7, DSV );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="a06e7-156">Semblable à <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets"><strong>ID3D11DeviceContext :: OMSetRenderTargets</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a06e7-156">Similar to <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets"><strong>ID3D11DeviceContext::OMSetRenderTargets</strong></a>.</span></span></p></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a><span data-ttu-id="a06e7-157">Exemples</span><span class="sxs-lookup"><span data-stu-id="a06e7-157">Examples</span></span>

<span data-ttu-id="a06e7-158">Cet exemple définit l’état de fusion.</span><span class="sxs-lookup"><span data-stu-id="a06e7-158">This example sets blending state.</span></span>


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



<span data-ttu-id="a06e7-159">Cet exemple configure l’état du rastériseur pour afficher un objet en mode filaire.</span><span class="sxs-lookup"><span data-stu-id="a06e7-159">This example sets up the rasterizer state to render an object in wireframe.</span></span>


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



<span data-ttu-id="a06e7-160">Cet exemple définit l’état du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="a06e7-160">This example sets shader state.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a06e7-161">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a06e7-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a06e7-162">Format d’effet</span><span class="sxs-lookup"><span data-stu-id="a06e7-162">Effect Format</span></span>](d3d11-effect-format.md)
</dt> <dt>

[<span data-ttu-id="a06e7-163">Syntaxe des groupes d’effets (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="a06e7-163">Effect Group Syntax (Direct3D 11)</span></span>](d3d11-effect-group-syntax.md)
</dt> <dt>

[<span data-ttu-id="a06e7-164">Groupes d’États d’effet</span><span class="sxs-lookup"><span data-stu-id="a06e7-164">Effect State Groups</span></span>](d3d11-effect-states.md)
</dt> </dl>

 

 






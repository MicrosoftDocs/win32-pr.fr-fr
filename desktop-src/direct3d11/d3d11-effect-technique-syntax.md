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
ms.openlocfilehash: 5b62876aea57864dfc495410e85ec2a9db24cbe1
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625555"
---
# <a name="effect-technique-syntax-direct3d-11"></a>Syntaxe d’effet technique (Direct3D 11)

Une technique d’effet est déclarée avec la syntaxe décrite dans cette section.

 \[  < *Annotations* TechniqueName TechniqueVersion > \]

{

<dl> passer  des \[  < *Annotations* PassName > \]  
{
<dl> \[*SetStateGroup*; \] \[ *SetStateGroup*;\]  
...  
\[*SetStateGroup*;\]
</dl> </dd> }  
</dl>

}

## <a name="parameters"></a>Paramètres



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Élément</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion<br/></td>
<td>Technique10 ou technique11. Les techniques qui utilisent les nouvelles fonctionnalités de Direct3D 11 (nuanceurs 5_0, BindInterfaces, etc.) doivent utiliser technique11.<br/></td>
</tr>
<tr class="even">
<td><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span><em>TechniqueName</em><br/></td>
<td>Optionnel. Chaîne ASCII qui identifie de façon unique le nom de la technique d’effet.<br/></td>
</tr>
<tr class="odd">
<td><span id="______________Annotations__"></span><span id="______________annotations__"></span><span id="______________ANNOTATIONS__"></span> <<em>Annotations</em> ><br/></td>
<td>[in] Facultatif. Un ou plusieurs éléments d’informations fournies par l’utilisateur (métadonnées) qui sont ignorés par le système d’effet. Pour obtenir la syntaxe, consultez <a href="d3d11-effect-annotation-syntax.md">syntaxe d’annotation (Direct3D 11)</a>.<br/></td>
</tr>
<tr class="even">
<td><span id="pass"></span><span id="PASS"></span>directes<br/></td>
<td>Mot clé requis.<br/></td>
</tr>
<tr class="odd">
<td><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span><em>PassName</em><br/></td>
<td>[in] Facultatif. Chaîne ASCII qui identifie de façon unique le nom de la passe.<br/></td>
</tr>
<tr class="even">
<td><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span><em>SetStateGroup</em><br/></td>
<td>dans Définissez un ou plusieurs groupes d’États tels que : <br/> 
<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>StateGroup</th>
<th>Syntax</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>État de fusion</td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetBlendState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

<p>Consultez [<strong>ID3D11DeviceContext :: OMSetBlendState</strong>] (/Windows/Desktop/API/d3d11/NF-d3d11-id3d11devicecontext-omsetblendstate) pour la liste d’arguments.</p></td>
</tr>
<tr class="even">
<td>État du stencil de profondeur</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetDepthStencilState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>Consultez <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate"><strong>ID3D11DeviceContext :: OMSetDepthStencilState</strong></a> pour obtenir la liste des arguments.</p></td>
</tr>
<tr class="odd">
<td>État du rastériseur</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetRasterizerState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>Consultez [<strong>ID3D11DeviceContext :: RSSetState</strong>] (/Windows/Desktop/API/d3d11/NF-d3d11-id3d11devicecontext-rssetstate) pour la liste d’arguments.</p></td>
</tr>
<tr class="even">
<td>État du nuanceur</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( Shader );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>SetXXXShader est l’un des SetVertexShader, SetDomainShader, SetHullShader, SetGeometryShader, SetPixelShader ou SetComputeShader (qui sont similaires aux méthodes d’API <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader"><strong>ID3D11DeviceContext :: VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader"><strong>ID3D11DeviceContext ::D ssetshader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader"><strong>ID3D11DeviceContext :: HSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetshader"><strong>ID3D11DeviceContext :: GSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader"><strong>ID3D11DeviceContext ::P ssetshader</strong></a> et <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetshader"><strong>ID3D11DeviceContext :: CSSetShader</strong></a>).</p>
<p>Le nuanceur est une variable de nuanceur, qui peut être obtenue de plusieurs façons :</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
<td>État de la cible de rendu</td>
<td>Valeurs possibles :
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
<p>Semblable à <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets"><strong>ID3D11DeviceContext :: OMSetRenderTargets</strong></a>.</p></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a>Exemples

Cet exemple définit l’état de fusion.


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



Cet exemple configure l’état du rastériseur pour afficher un objet en mode filaire.


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



Cet exemple définit l’état du nuanceur.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Format d’effet](d3d11-effect-format.md)
</dt> <dt>

[Syntaxe des groupes d’effets (Direct3D 11)](d3d11-effect-group-syntax.md)
</dt> <dt>

[Groupes d’États d’effet](d3d11-effect-states.md)
</dt> </dl>

 

 






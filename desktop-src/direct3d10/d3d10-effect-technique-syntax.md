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
# <a name="effect-technique-syntax-direct3d-10"></a>Syntaxe d’effet technique (Direct3D 10)

Une technique d’effet est déclarée avec la syntaxe suivante.

 \[  < *Annotations* TechniqueName technique10 > \]

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

<dl> <dt>

<span id="technique10"></span><span id="TECHNIQUE10"></span>technique10
</dt> <dd>

Mot clé requis.

</dd> <dt>

<span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>*TechniqueName*
</dt> <dd>

Optionnel. Chaîne ASCII qui identifie de façon unique le nom de la technique d’effet.

</dd> <dt>

<span id="Annotations"></span><span id="annotations"></span><span id="ANNOTATIONS"></span>*Annotations*
</dt> <dd>

\[\]facultatif. Un ou plusieurs éléments d’informations fournies par l’utilisateur (métadonnées) qui sont ignorés par le système d’effet. Pour obtenir la syntaxe, consultez [syntaxe d’annotation (Direct3D 10)](d3d10-effect-annotation-syntax.md).

</dd> <dt>

<span id="pass"></span><span id="PASS"></span>directes
</dt> <dd>

Mot clé requis.

</dd> <dt>

<span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span>*PassName*
</dt> <dd>

\[\]facultatif. Chaîne ASCII qui identifie de façon unique le nom de la passe.

</dd> <dt>

<span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span>*SetStateGroup*
</dt> <dd>

\[dans, \] définissez un ou plusieurs groupes d’États tels que :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>StateGroup</th>
<th>Syntaxe</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>État de fusion</td>
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

<p>Consultez [<strong>OMSetBlendState</strong>] (/Windows/Desktop/API/D3D10/NF-D3D10-id3d10device-omsetblendstate) pour la liste d’arguments.</p></td>
</tr>
<tr class="even">
<td>État du stencil de profondeur</td>
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
<p>Consultez <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetdepthstencilstate"><strong>OMSetDepthStencilState</strong></a> pour obtenir la liste des arguments.</p></td>
</tr>
<tr class="odd">
<td>État du rastériseur</td>
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
<p>Consultez [<strong>RSSetState</strong>] (/Windows/Desktop/API/D3D10/NF-D3D10-id3d10device-rssetstate) pour la liste d’arguments.</p></td>
</tr>
<tr class="even">
<td>État du nuanceur</td>
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
<p>or</p>
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
<p>or</p>
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
<p>SetXXXShader est l’un des <strong>SetVertexShader</strong>, <strong>SetGeometryShader</strong>ou <strong>SetPixelShader</strong> (qui sont similaires aux méthodes d’API <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader"><strong>VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetshader"><strong>GSSetShader</strong></a>et <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetshader"><strong>PSSetShader</strong></a>).</p></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

Les groupes d’États d’effet sont répertoriés en [État d’effet](d3d10-effect-states.md).

## <a name="examples"></a>Exemples

Cet exemple (de l' [exemple CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) définit l’état de fusion.


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



Cet exemple définit l’état du nuanceur (à partir de l' [exemple BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)); qui utilise un nuanceur de sommets et de pixels.


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

[Format d’effet](d3d10-effect-format.md)
</dt> </dl>

 

 




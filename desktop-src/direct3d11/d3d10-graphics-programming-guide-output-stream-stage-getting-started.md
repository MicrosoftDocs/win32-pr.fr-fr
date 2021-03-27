---
title: Prise en main avec l’étape de Stream-Output
description: Cette section décrit comment utiliser un nuanceur Geometry avec l’étape de sortie de flux.
ms.assetid: 37146486-5922-4833-850c-cc4a51de0957
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 909b3ba37e8b80201a4afc3e5bf18f016fed38a0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971742"
---
# <a name="getting-started-with-the-stream-output-stage"></a>Prise en main avec l’étape de Stream-Output

Cette section décrit comment utiliser un nuanceur Geometry avec l’étape de sortie de flux.

## <a name="compile-a-geometry-shader"></a>Compiler un nuanceur Geometry

Ce nuanceur Geometry (GS) calcule une face normale pour chaque triangle et génère les données de la position, de la normale et de la coordonnée de texture.


```
struct GSPS_INPUT
{
    float4 Pos : SV_POSITION;
    float3 Norm : TEXCOORD0;
    float2 Tex : TEXCOORD1;
};

[maxvertexcount(12)]
void GS( triangle GSPS_INPUT input[3], inout TriangleStream<GSPS_INPUT> TriStream )
{
    GSPS_INPUT output;
    
    //
    // Calculate the face normal
    //
    float3 faceEdgeA = input[1].Pos - input[0].Pos;
    float3 faceEdgeB = input[2].Pos - input[0].Pos;
    float3 faceNormal = normalize( cross(faceEdgeA, faceEdgeB) );
    float3 ExplodeAmt = faceNormal*Explode;
    
    //
    // Calculate the face center
    //
    float3 centerPos = (input[0].Pos.xyz + input[1].Pos.xyz + input[2].Pos.xyz)/3.0;
    float2 centerTex = (input[0].Tex + input[1].Tex + input[2].Tex)/3.0;
    centerPos += faceNormal*Explode;
    
    //
    // Output the pyramid
    //
    for( int i=0; i<3; i++ )
    {
        output.Pos = input[i].Pos + float4(ExplodeAmt,0);
        output.Pos = mul( output.Pos, View );
        output.Pos = mul( output.Pos, Projection );
        output.Norm = input[i].Norm;
        output.Tex = input[i].Tex;
        TriStream.Append( output );
        
        int iNext = (i+1)%3;
        output.Pos = input[iNext].Pos + float4(ExplodeAmt,0);
        output.Pos = mul( output.Pos, View );
        output.Pos = mul( output.Pos, Projection );
        output.Norm = input[iNext].Norm;
        output.Tex = input[iNext].Tex;
        TriStream.Append( output );
        
        output.Pos = float4(centerPos,1) + float4(ExplodeAmt,0);
        output.Pos = mul( output.Pos, View );
        output.Pos = mul( output.Pos, Projection );
        output.Norm = faceNormal;
        output.Tex = centerTex;
        TriStream.Append( output );
        
        TriStream.RestartStrip();
    }
    
    for( int i=2; i>=0; i-- )
    {
        output.Pos = input[i].Pos + float4(ExplodeAmt,0);
        output.Pos = mul( output.Pos, View );
        output.Pos = mul( output.Pos, Projection );
        output.Norm = -input[i].Norm;
        output.Tex = input[i].Tex;
        TriStream.Append( output );
    }
    TriStream.RestartStrip();
}
```



En gardant ce code à l’esprit, considérez qu’un nuanceur Geometry ressemble à un nuanceur de sommets ou de pixels, mais avec les exceptions suivantes : le type retourné par la fonction, les déclarations de paramètre d’entrée et la fonction intrinsèque.



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
<td><span id="Function_return_type"></span><span id="function_return_type"></span><span id="FUNCTION_RETURN_TYPE"></span>Type de retour de fonction<br/></td>
<td>Le type de retour de la fonction effectue une opération, déclare le nombre maximal de vertex qui peuvent être générés par le nuanceur. Dans ce cas, <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>maxvertexcount(12)</code></pre></td>
</tr>
</tbody>
</table>

définit la sortie sur un maximum de 12 sommets.</td>
</tr>
<tr class="even">
<td><p><span id="Input_parameter_declarations"></span><span id="input_parameter_declarations"></span><span id="INPUT_PARAMETER_DECLARATIONS"></span>Déclarations des paramètres d’entrée</p></td>
<td><p>Cette fonction accepte deux paramètres d’entrée :</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>triangle GSPS_INPUT input[3] , inout TriangleStream<GSPS_INPUT> TriStream</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>Le premier paramètre est un tableau de vertex (3 dans ce cas) défini par une structure GSPS_INPUT (qui définit les données par vertex comme une position, une coordonnée normale et une coordonnée de texture). Le premier paramètre utilise également le mot clé triangle, ce qui signifie que l’étape assembleur d’entrée doit sortir les données du nuanceur Geometry sous la forme d’un des types de primitives de triangle (liste de triangles ou bande triangulaire).</p>
<p>Le deuxième paramètre est un flux de triangle défini par le type TriangleStream <GSPS_INPUT> . Cela signifie que le paramètre est un tableau de triangles, chacun composé de trois vertex (qui contiennent les données des membres de GSPS_INPUT).</p>
<p>Utilisez les mots clés triangle et trianglestream pour identifier des triangles individuels ou un flux de triangles dans un GS.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Intrinsic_function"></span><span id="intrinsic_function"></span><span id="INTRINSIC_FUNCTION"></span>Fonction intrinsèque</p></td>
<td><p>Les lignes de code de la fonction de nuanceur utilisent des fonctions intrinsèques HLSL (Common-Shader-Core), à l’exception des deux dernières lignes, qui appellent Append et RestartStrip. Ces fonctions sont uniquement disponibles pour un nuanceur Geometry. Ajouter informe le nuanceur Geometry pour ajouter la sortie à la bande actuelle. RestartStrip crée une nouvelle bande primitive. Une nouvelle bande est implicitement créée à chaque appel de l’étape GS.</p></td>
</tr>
</tbody>
</table>



 

Le reste du nuanceur semble très similaire à un nuanceur de sommets ou de pixels. Le nuanceur Geometry utilise une structure pour déclarer des paramètres d’entrée et marque le membre position avec la \_ sémantique de position SV pour indiquer au matériel qu’il s’agit de données positionnelles. La structure d’entrée identifie les deux autres paramètres d’entrée comme des coordonnées de texture (même si l’une d’entre elles contient un visage normal). Vous pouvez utiliser votre propre sémantique personnalisée pour la face normale si vous préférez.

Après avoir conçu le nuanceur Geometry, appelez [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) pour compiler comme indiqué dans l’exemple de code suivant.


```
DWORD dwShaderFlags = D3DCOMPILE_ENABLE_STRICTNESS;
ID3DBlob** ppShader;

D3DCompile( pSrcData, sizeof( pSrcData ), 
  "Tutorial13.fx", NULL, NULL, "GS", "gs_4_0", 
  dwShaderFlags, 0, &ppShader, NULL );
```



Tout comme les nuanceurs vertex et pixel, vous avez besoin d’un indicateur de nuanceur pour indiquer au compilateur comment vous souhaitez que le nuanceur soit compilé (pour le débogage, optimisé pour la vitesse, etc.), la fonction de point d’entrée et le modèle de nuanceur à valider. Cet exemple crée un nuanceur Geometry généré à partir du fichier Tutorial13. FX, à l’aide de la fonction GS. Le nuanceur est compilé pour le modèle de nuanceur 4,0.

## <a name="create-a-geometry-shader-object-with-stream-output"></a>Créer un objet Geometry-Shader avec une sortie de flux

Une fois que vous savez que vous allez diffuser en continu les données à partir de la géométrie et que vous avez correctement compilé le nuanceur, l’étape suivante consiste à appeler [**ID3D11Device :: CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) pour créer l’objet de nuanceur Geometry.

Mais tout d’abord, vous devez déclarer la signature d’entrée de l’étape de sortie à la vapeur (SO). Cette signature correspond à ou valide les sorties GS et les entrées SO au moment de la création de l’objet. Le code suivant est un exemple de la déclaration SO.


```
D3D11_SO_DECLARATION_ENTRY pDecl[] =
{
    // semantic name, semantic index, start component, component count, output slot
    { "SV_POSITION", 0, 0, 4, 0 },   // output all components of position
    { "TEXCOORD0", 0, 0, 3, 0 },     // output the first 3 of the normal
    { "TEXCOORD1", 0, 0, 2, 0 },     // output the first 2 texture coordinates
};

D3D11Device->CreateGeometryShaderWithStreamOut( pShaderBytecode, ShaderBytecodesize, pDecl, 
    sizeof(pDecl), NULL, 0, 0, NULL, &pStreamOutGS );
```



Cette fonction accepte plusieurs paramètres, notamment :

-   Pointeur vers le nuanceur Geometry compilé (ou le nuanceur de sommets si aucun nuanceur Geometry n’est présent et que les données sont transmises directement à partir du nuanceur de sommets). Pour plus d’informations sur la façon d’obtenir ce pointeur, consultez [obtention d’un pointeur vers un nuanceur compilé](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-using-shaders-10).
-   Pointeur vers un tableau de déclarations qui décrivent les données d’entrée pour l’étape de sortie de flux. (Pour plus d' [**d3d11, consultez la \_ \_ \_ rubrique entrée de déclaration**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry).) Vous pouvez fournir jusqu’à 64 déclarations, une pour chaque type d’élément différent à générer à partir de l’étape SO. Le tableau d’entrées de déclaration décrit la disposition des données, indépendamment du fait qu’une seule mémoire tampon ou plusieurs mémoires tampons soient liées pour la sortie du flux.
-   Nombre d’éléments écrits par l’étape SO.
-   Pointeur vers l’objet de nuanceur Geometry créé (voir [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)).

Dans ce cas, la valeur de la Stride de la mémoire tampon est NULL, l’index du flux à envoyer au rastériseur est 0, et l’interface de liaison de classe a la valeur NULL.

La déclaration de sortie de flux définit la façon dont les données sont écrites dans une ressource de mémoire tampon. Vous pouvez ajouter autant de composants que vous le souhaitez à la déclaration de sortie. Utilisez l’étape SO pour écrire dans une ressource de mémoire tampon unique ou dans de nombreuses ressources de mémoire tampon. Pour une seule mémoire tampon, l’étape SO peut écrire de nombreux éléments différents par vertex. Pour plusieurs mémoires tampons, l’étape SO ne peut écrire qu’un seul élément de données par vertex dans chaque mémoire tampon.

Pour utiliser l’étape SO sans utiliser de nuanceur Geometry, appelez [**ID3D11Device :: CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) et transmettez un pointeur à un nuanceur de sommets au paramètre *pShaderBytecode* .

## <a name="set-the-output-targets"></a>Définir les cibles de sortie

La dernière étape consiste à définir les tampons intermédiaires. Les données peuvent être transmises dans une ou plusieurs mémoires tampons en mémoire pour une utilisation ultérieure. Le code suivant montre comment créer une mémoire tampon unique qui peut être utilisée pour les données de vertex, ainsi que pour la phase de création de flux de données dans.


```
ID3D11Buffer *m_pBuffer;
int m_nBufferSize = 1000000;

D3D11_BUFFER_DESC bufferDesc =
{
    m_nBufferSize,
    D3D11_USAGE_DEFAULT,
    D3D11_BIND_STREAM_OUTPUT,
    0,
    0,
    0
};
D3D11Device->CreateBuffer( &bufferDesc, NULL, &m_pBuffer );
```



Créez une mémoire tampon en appelant [**ID3D11Device :: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer). Cet exemple illustre l’utilisation par défaut, qui est typique pour une ressource de mémoire tampon censée être mise à jour assez fréquemment par l’UC. L’indicateur de liaison identifie l’étape de pipeline à laquelle la ressource peut être liée. Toutes les ressources utilisées par l’étape doivent également être créées avec l’indicateur de liaison D3D10 de la \_ sortie de liaison de \_ flux \_ .

Une fois la mémoire tampon créée, définissez-la sur l’appareil actuel en appelant [**ID3D11DeviceContext :: SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets):


```
UINT offset[1] = 0;
D3D11Device->SOSetTargets( 1, &m_pBuffer, offset );
```



Cet appel prend le nombre de mémoires tampons, un pointeur vers les mémoires tampons et un tableau d’offsets (un offset dans chaque mémoire tampon qui indique où commencer l’écriture des données). Les données sont écrites dans ces mémoires tampons de sortie de diffusion en continu lorsqu’une fonction de dessin est appelée. Une variable interne effectue le suivi de la position à laquelle commencer l’écriture de données dans les mémoires tampons de sortie de diffusion en continu, et les variables continuent à s’incrémenter jusqu’à ce que [**SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets) soit à nouveau appelée et qu’une nouvelle valeur de décalage soit spécifiée.

Toutes les données écrites dans les mémoires tampons cibles seront des valeurs de 32 bits.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Étape de sortie de flux](d3d10-graphics-programming-guide-output-stream-stage.md)
</dt> </dl>

 


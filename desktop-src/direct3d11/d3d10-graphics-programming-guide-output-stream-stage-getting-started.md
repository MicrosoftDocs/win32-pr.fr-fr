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
# <a name="getting-started-with-the-stream-output-stage"></a><span data-ttu-id="a9e90-103">Prise en main avec l’étape de Stream-Output</span><span class="sxs-lookup"><span data-stu-id="a9e90-103">Getting Started with the Stream-Output Stage</span></span>

<span data-ttu-id="a9e90-104">Cette section décrit comment utiliser un nuanceur Geometry avec l’étape de sortie de flux.</span><span class="sxs-lookup"><span data-stu-id="a9e90-104">This section describes how to use a geometry shader with the stream output stage.</span></span>

## <a name="compile-a-geometry-shader"></a><span data-ttu-id="a9e90-105">Compiler un nuanceur Geometry</span><span class="sxs-lookup"><span data-stu-id="a9e90-105">Compile a Geometry Shader</span></span>

<span data-ttu-id="a9e90-106">Ce nuanceur Geometry (GS) calcule une face normale pour chaque triangle et génère les données de la position, de la normale et de la coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="a9e90-106">This geometry shader (GS) calculates a face normal for each triangle, and outputs position, normal and texture coordinate data.</span></span>


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



<span data-ttu-id="a9e90-107">En gardant ce code à l’esprit, considérez qu’un nuanceur Geometry ressemble à un nuanceur de sommets ou de pixels, mais avec les exceptions suivantes : le type retourné par la fonction, les déclarations de paramètre d’entrée et la fonction intrinsèque.</span><span class="sxs-lookup"><span data-stu-id="a9e90-107">Keeping that code in mind, consider that a geometry shader looks much like a vertex or pixel shader, but with the following exceptions: the type returned by the function, the input parameter declarations, and the intrinsic function.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a9e90-108">Élément</span><span class="sxs-lookup"><span data-stu-id="a9e90-108">Item</span></span></th>
<th><span data-ttu-id="a9e90-109">Description</span><span class="sxs-lookup"><span data-stu-id="a9e90-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a9e90-110"><span id="Function_return_type"></span><span id="function_return_type"></span><span id="FUNCTION_RETURN_TYPE"></span>Type de retour de fonction</span><span class="sxs-lookup"><span data-stu-id="a9e90-110"><span id="Function_return_type"></span><span id="function_return_type"></span><span id="FUNCTION_RETURN_TYPE"></span>Function return type</span></span><br/></td>
<td><span data-ttu-id="a9e90-111">Le type de retour de la fonction effectue une opération, déclare le nombre maximal de vertex qui peuvent être générés par le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="a9e90-111">The function return type does one thing, declares the maximum number of vertices that can be output by the shader.</span></span> <span data-ttu-id="a9e90-112">Dans ce cas, <span data-codelanguage=""></span>
</span><span class="sxs-lookup"><span data-stu-id="a9e90-112">In this case, <span data-codelanguage=""></span>
</span></span><table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>maxvertexcount(12)</code></pre></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a9e90-113">définit la sortie sur un maximum de 12 sommets.</span><span class="sxs-lookup"><span data-stu-id="a9e90-113">defines the output to be a maximum of 12 vertices.</span></span></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9e90-114"><span id="Input_parameter_declarations"></span><span id="input_parameter_declarations"></span><span id="INPUT_PARAMETER_DECLARATIONS"></span>Déclarations des paramètres d’entrée</span><span class="sxs-lookup"><span data-stu-id="a9e90-114"><span id="Input_parameter_declarations"></span><span id="input_parameter_declarations"></span><span id="INPUT_PARAMETER_DECLARATIONS"></span>Input parameter declarations</span></span></p></td>
<td><p><span data-ttu-id="a9e90-115">Cette fonction accepte deux paramètres d’entrée :</span><span class="sxs-lookup"><span data-stu-id="a9e90-115">This function takes two input parameters:</span></span></p>
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
<p><span data-ttu-id="a9e90-116">Le premier paramètre est un tableau de vertex (3 dans ce cas) défini par une structure GSPS_INPUT (qui définit les données par vertex comme une position, une coordonnée normale et une coordonnée de texture).</span><span class="sxs-lookup"><span data-stu-id="a9e90-116">The first parameter is an array of vertices (3 in this case) defined by a GSPS_INPUT structure (which defines per-vertex data as a position, a normal and a texture coordinate).</span></span> <span data-ttu-id="a9e90-117">Le premier paramètre utilise également le mot clé triangle, ce qui signifie que l’étape assembleur d’entrée doit sortir les données du nuanceur Geometry sous la forme d’un des types de primitives de triangle (liste de triangles ou bande triangulaire).</span><span class="sxs-lookup"><span data-stu-id="a9e90-117">The first parameter also uses the triangle keyword, which means the input assembler stage must output data to the geometry shader as one of the triangle primitive types (triangle list or triangle strip).</span></span></p>
<p><span data-ttu-id="a9e90-118">Le deuxième paramètre est un flux de triangle défini par le type TriangleStream <GSPS_INPUT> .</span><span class="sxs-lookup"><span data-stu-id="a9e90-118">The second parameter is a triangle stream defined by the type TriangleStream<GSPS_INPUT>.</span></span> <span data-ttu-id="a9e90-119">Cela signifie que le paramètre est un tableau de triangles, chacun composé de trois vertex (qui contiennent les données des membres de GSPS_INPUT).</span><span class="sxs-lookup"><span data-stu-id="a9e90-119">This means the parameter is an array of triangles, each of which is made up of three vertices (that contain the data from the members of GSPS_INPUT).</span></span></p>
<p><span data-ttu-id="a9e90-120">Utilisez les mots clés triangle et trianglestream pour identifier des triangles individuels ou un flux de triangles dans un GS.</span><span class="sxs-lookup"><span data-stu-id="a9e90-120">Use the triangle and trianglestream keywords to identify individual triangles or a stream of triangles in a GS.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9e90-121"><span id="Intrinsic_function"></span><span id="intrinsic_function"></span><span id="INTRINSIC_FUNCTION"></span>Fonction intrinsèque</span><span class="sxs-lookup"><span data-stu-id="a9e90-121"><span id="Intrinsic_function"></span><span id="intrinsic_function"></span><span id="INTRINSIC_FUNCTION"></span>Intrinsic function</span></span></p></td>
<td><p><span data-ttu-id="a9e90-122">Les lignes de code de la fonction de nuanceur utilisent des fonctions intrinsèques HLSL (Common-Shader-Core), à l’exception des deux dernières lignes, qui appellent Append et RestartStrip.</span><span class="sxs-lookup"><span data-stu-id="a9e90-122">The lines of code in the shader function use common-shader-core HLSL intrinsic functions except the last two lines, which call Append and RestartStrip.</span></span> <span data-ttu-id="a9e90-123">Ces fonctions sont uniquement disponibles pour un nuanceur Geometry.</span><span class="sxs-lookup"><span data-stu-id="a9e90-123">These functions are only available to a geometry shader.</span></span> <span data-ttu-id="a9e90-124">Ajouter informe le nuanceur Geometry pour ajouter la sortie à la bande actuelle. RestartStrip crée une nouvelle bande primitive.</span><span class="sxs-lookup"><span data-stu-id="a9e90-124">Append informs the geometry shader to append the output to the current strip; RestartStrip creates a new primitive strip.</span></span> <span data-ttu-id="a9e90-125">Une nouvelle bande est implicitement créée à chaque appel de l’étape GS.</span><span class="sxs-lookup"><span data-stu-id="a9e90-125">A new strip is implicitly created in every invocation of the GS stage.</span></span></p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a9e90-126">Le reste du nuanceur semble très similaire à un nuanceur de sommets ou de pixels.</span><span class="sxs-lookup"><span data-stu-id="a9e90-126">The rest of the shader looks very similar to a vertex or pixel shader.</span></span> <span data-ttu-id="a9e90-127">Le nuanceur Geometry utilise une structure pour déclarer des paramètres d’entrée et marque le membre position avec la \_ sémantique de position SV pour indiquer au matériel qu’il s’agit de données positionnelles.</span><span class="sxs-lookup"><span data-stu-id="a9e90-127">The geometry shader uses a structure to declare input parameters and marks the position member with the SV\_POSITION semantic to tell the hardware that this is positional data.</span></span> <span data-ttu-id="a9e90-128">La structure d’entrée identifie les deux autres paramètres d’entrée comme des coordonnées de texture (même si l’une d’entre elles contient un visage normal).</span><span class="sxs-lookup"><span data-stu-id="a9e90-128">The input structure identifies the other two input parameters as texture coordinates (even though one of them will contain a face normal).</span></span> <span data-ttu-id="a9e90-129">Vous pouvez utiliser votre propre sémantique personnalisée pour la face normale si vous préférez.</span><span class="sxs-lookup"><span data-stu-id="a9e90-129">You could use your own custom semantic for the face normal if you prefer.</span></span>

<span data-ttu-id="a9e90-130">Après avoir conçu le nuanceur Geometry, appelez [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) pour compiler comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="a9e90-130">Having designed the geometry shader, call [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) to compile as shown in the following code example.</span></span>


```
DWORD dwShaderFlags = D3DCOMPILE_ENABLE_STRICTNESS;
ID3DBlob** ppShader;

D3DCompile( pSrcData, sizeof( pSrcData ), 
  "Tutorial13.fx", NULL, NULL, "GS", "gs_4_0", 
  dwShaderFlags, 0, &ppShader, NULL );
```



<span data-ttu-id="a9e90-131">Tout comme les nuanceurs vertex et pixel, vous avez besoin d’un indicateur de nuanceur pour indiquer au compilateur comment vous souhaitez que le nuanceur soit compilé (pour le débogage, optimisé pour la vitesse, etc.), la fonction de point d’entrée et le modèle de nuanceur à valider.</span><span class="sxs-lookup"><span data-stu-id="a9e90-131">Just like vertex and pixel shaders, you need a shader flag to tell the compiler how you want the shader compiled (for debugging, optimized for speed, and so on), the entry point function, and the shader model to validate against.</span></span> <span data-ttu-id="a9e90-132">Cet exemple crée un nuanceur Geometry généré à partir du fichier Tutorial13. FX, à l’aide de la fonction GS.</span><span class="sxs-lookup"><span data-stu-id="a9e90-132">This example creates a geometry shader built from the Tutorial13.fx file, by using the GS function.</span></span> <span data-ttu-id="a9e90-133">Le nuanceur est compilé pour le modèle de nuanceur 4,0.</span><span class="sxs-lookup"><span data-stu-id="a9e90-133">The shader is compiled for shader model 4.0.</span></span>

## <a name="create-a-geometry-shader-object-with-stream-output"></a><span data-ttu-id="a9e90-134">Créer un objet Geometry-Shader avec une sortie de flux</span><span class="sxs-lookup"><span data-stu-id="a9e90-134">Create a Geometry-Shader Object with Stream Output</span></span>

<span data-ttu-id="a9e90-135">Une fois que vous savez que vous allez diffuser en continu les données à partir de la géométrie et que vous avez correctement compilé le nuanceur, l’étape suivante consiste à appeler [**ID3D11Device :: CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) pour créer l’objet de nuanceur Geometry.</span><span class="sxs-lookup"><span data-stu-id="a9e90-135">Once you know that you will be streaming the data from the geometry, and you have successfully compiled the shader, the next step is to call [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) to create the geometry shader object.</span></span>

<span data-ttu-id="a9e90-136">Mais tout d’abord, vous devez déclarer la signature d’entrée de l’étape de sortie à la vapeur (SO).</span><span class="sxs-lookup"><span data-stu-id="a9e90-136">But first, you need to declare the steam output (SO) stage input signature.</span></span> <span data-ttu-id="a9e90-137">Cette signature correspond à ou valide les sorties GS et les entrées SO au moment de la création de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a9e90-137">This signature matches or validates the GS outputs and the SO inputs at the time of object creation.</span></span> <span data-ttu-id="a9e90-138">Le code suivant est un exemple de la déclaration SO.</span><span class="sxs-lookup"><span data-stu-id="a9e90-138">The following code is an example of the SO declaration.</span></span>


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



<span data-ttu-id="a9e90-139">Cette fonction accepte plusieurs paramètres, notamment :</span><span class="sxs-lookup"><span data-stu-id="a9e90-139">This function takes several parameters including:</span></span>

-   <span data-ttu-id="a9e90-140">Pointeur vers le nuanceur Geometry compilé (ou le nuanceur de sommets si aucun nuanceur Geometry n’est présent et que les données sont transmises directement à partir du nuanceur de sommets).</span><span class="sxs-lookup"><span data-stu-id="a9e90-140">A pointer to the compiled geometry shader (or vertex shader if no geometry shader will be present and data will be streamed out directly from the vertex shader).</span></span> <span data-ttu-id="a9e90-141">Pour plus d’informations sur la façon d’obtenir ce pointeur, consultez [obtention d’un pointeur vers un nuanceur compilé](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-using-shaders-10).</span><span class="sxs-lookup"><span data-stu-id="a9e90-141">For information about how to get this pointer, see [Getting a Pointer to a Compiled Shader](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-using-shaders-10).</span></span>
-   <span data-ttu-id="a9e90-142">Pointeur vers un tableau de déclarations qui décrivent les données d’entrée pour l’étape de sortie de flux.</span><span class="sxs-lookup"><span data-stu-id="a9e90-142">A pointer to an array of declarations that describe the input data for the stream output stage.</span></span> <span data-ttu-id="a9e90-143">(Pour plus d' [**d3d11, consultez la \_ \_ \_ rubrique entrée de déclaration**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry).) Vous pouvez fournir jusqu’à 64 déclarations, une pour chaque type d’élément différent à générer à partir de l’étape SO.</span><span class="sxs-lookup"><span data-stu-id="a9e90-143">(See [**D3D11\_SO\_DECLARATION\_ENTRY**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry).) You can supply up to 64 declarations, one for each different type of element to be output from the SO stage.</span></span> <span data-ttu-id="a9e90-144">Le tableau d’entrées de déclaration décrit la disposition des données, indépendamment du fait qu’une seule mémoire tampon ou plusieurs mémoires tampons soient liées pour la sortie du flux.</span><span class="sxs-lookup"><span data-stu-id="a9e90-144">The array of declaration entries describes the data layout regardless of whether only a single buffer or multiple buffers are to be bound for stream output.</span></span>
-   <span data-ttu-id="a9e90-145">Nombre d’éléments écrits par l’étape SO.</span><span class="sxs-lookup"><span data-stu-id="a9e90-145">The number of elements that are written out by the SO stage.</span></span>
-   <span data-ttu-id="a9e90-146">Pointeur vers l’objet de nuanceur Geometry créé (voir [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)).</span><span class="sxs-lookup"><span data-stu-id="a9e90-146">A pointer to the geometry shader object that is created (see [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)).</span></span>

<span data-ttu-id="a9e90-147">Dans ce cas, la valeur de la Stride de la mémoire tampon est NULL, l’index du flux à envoyer au rastériseur est 0, et l’interface de liaison de classe a la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="a9e90-147">In this situation, the buffer stride is NULL, the index of the stream to be sent to the rasterizer is 0, and the class linkage interface is NULL.</span></span>

<span data-ttu-id="a9e90-148">La déclaration de sortie de flux définit la façon dont les données sont écrites dans une ressource de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="a9e90-148">The stream output declaration defines the way that data is written to a buffer resource.</span></span> <span data-ttu-id="a9e90-149">Vous pouvez ajouter autant de composants que vous le souhaitez à la déclaration de sortie.</span><span class="sxs-lookup"><span data-stu-id="a9e90-149">You can add as many components as you want to the output declaration.</span></span> <span data-ttu-id="a9e90-150">Utilisez l’étape SO pour écrire dans une ressource de mémoire tampon unique ou dans de nombreuses ressources de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="a9e90-150">Use the SO stage to write to a single buffer resource or many buffer resources.</span></span> <span data-ttu-id="a9e90-151">Pour une seule mémoire tampon, l’étape SO peut écrire de nombreux éléments différents par vertex.</span><span class="sxs-lookup"><span data-stu-id="a9e90-151">For a single buffer, the SO stage can write many different elements per-vertex.</span></span> <span data-ttu-id="a9e90-152">Pour plusieurs mémoires tampons, l’étape SO ne peut écrire qu’un seul élément de données par vertex dans chaque mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="a9e90-152">For multiple buffers, the SO stage can only write a single element of per-vertex data to each buffer.</span></span>

<span data-ttu-id="a9e90-153">Pour utiliser l’étape SO sans utiliser de nuanceur Geometry, appelez [**ID3D11Device :: CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) et transmettez un pointeur à un nuanceur de sommets au paramètre *pShaderBytecode* .</span><span class="sxs-lookup"><span data-stu-id="a9e90-153">To use the SO stage without using a geometry shader, call [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) and pass a pointer to a vertex shader to the *pShaderBytecode* parameter.</span></span>

## <a name="set-the-output-targets"></a><span data-ttu-id="a9e90-154">Définir les cibles de sortie</span><span class="sxs-lookup"><span data-stu-id="a9e90-154">Set the Output Targets</span></span>

<span data-ttu-id="a9e90-155">La dernière étape consiste à définir les tampons intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="a9e90-155">The last step is to set the SO stage buffers.</span></span> <span data-ttu-id="a9e90-156">Les données peuvent être transmises dans une ou plusieurs mémoires tampons en mémoire pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a9e90-156">Data can be streamed into one or more buffers in memory for use later.</span></span> <span data-ttu-id="a9e90-157">Le code suivant montre comment créer une mémoire tampon unique qui peut être utilisée pour les données de vertex, ainsi que pour la phase de création de flux de données dans.</span><span class="sxs-lookup"><span data-stu-id="a9e90-157">The following code shows how to create a single buffer that can be used for vertex data, as well as for the SO stage to stream data into.</span></span>


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



<span data-ttu-id="a9e90-158">Créez une mémoire tampon en appelant [**ID3D11Device :: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer).</span><span class="sxs-lookup"><span data-stu-id="a9e90-158">Create a buffer by calling [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer).</span></span> <span data-ttu-id="a9e90-159">Cet exemple illustre l’utilisation par défaut, qui est typique pour une ressource de mémoire tampon censée être mise à jour assez fréquemment par l’UC.</span><span class="sxs-lookup"><span data-stu-id="a9e90-159">This example illustrates default usage, which is typical for a buffer resource that is expected to be updated fairly frequently by the CPU.</span></span> <span data-ttu-id="a9e90-160">L’indicateur de liaison identifie l’étape de pipeline à laquelle la ressource peut être liée.</span><span class="sxs-lookup"><span data-stu-id="a9e90-160">The binding flag identifies the pipeline stage that the resource can be bound to.</span></span> <span data-ttu-id="a9e90-161">Toutes les ressources utilisées par l’étape doivent également être créées avec l’indicateur de liaison D3D10 de la \_ sortie de liaison de \_ flux \_ .</span><span class="sxs-lookup"><span data-stu-id="a9e90-161">Any resource used by the SO stage must also be created with the bind flag D3D10\_BIND\_STREAM\_OUTPUT.</span></span>

<span data-ttu-id="a9e90-162">Une fois la mémoire tampon créée, définissez-la sur l’appareil actuel en appelant [**ID3D11DeviceContext :: SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets):</span><span class="sxs-lookup"><span data-stu-id="a9e90-162">Once the buffer is successfully created, set it to the current device by calling [**ID3D11DeviceContext::SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets):</span></span>


```
UINT offset[1] = 0;
D3D11Device->SOSetTargets( 1, &m_pBuffer, offset );
```



<span data-ttu-id="a9e90-163">Cet appel prend le nombre de mémoires tampons, un pointeur vers les mémoires tampons et un tableau d’offsets (un offset dans chaque mémoire tampon qui indique où commencer l’écriture des données).</span><span class="sxs-lookup"><span data-stu-id="a9e90-163">This call takes the number of buffers, a pointer to the buffers, and an array of offsets (one offset into each of the buffers that indicates where to begin writing data).</span></span> <span data-ttu-id="a9e90-164">Les données sont écrites dans ces mémoires tampons de sortie de diffusion en continu lorsqu’une fonction de dessin est appelée.</span><span class="sxs-lookup"><span data-stu-id="a9e90-164">Data will be written to these streaming-output buffers when a draw function is called.</span></span> <span data-ttu-id="a9e90-165">Une variable interne effectue le suivi de la position à laquelle commencer l’écriture de données dans les mémoires tampons de sortie de diffusion en continu, et les variables continuent à s’incrémenter jusqu’à ce que [**SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets) soit à nouveau appelée et qu’une nouvelle valeur de décalage soit spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a9e90-165">An internal variable keeps track of the position for where to begin writing data to the streaming-output buffers, and that variables will continue to increment until [**SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets) is called again and a new offset value is specified.</span></span>

<span data-ttu-id="a9e90-166">Toutes les données écrites dans les mémoires tampons cibles seront des valeurs de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a9e90-166">All data written out to the target buffers will be 32-bit values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9e90-167">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a9e90-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9e90-168">Étape de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="a9e90-168">Stream-Output Stage</span></span>](d3d10-graphics-programming-guide-output-stream-stage.md)
</dt> </dl>

 


---
title: Syntaxe du flux de sortie
description: Un nuanceur Geometry avec flux sortant est déclaré avec une syntaxe particulière.
ms.assetid: 58cf6503-0dde-4c88-837d-ae0e0eda17d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535ea78d1b2109e343f01800b3a3d5e1bf6efaba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990620"
---
# <a name="stream-out-syntax"></a><span data-ttu-id="80aec-103">Syntaxe du flux de sortie</span><span class="sxs-lookup"><span data-stu-id="80aec-103">Stream Out Syntax</span></span>

<span data-ttu-id="80aec-104">Un nuanceur Geometry avec flux sortant est déclaré avec une syntaxe particulière.</span><span class="sxs-lookup"><span data-stu-id="80aec-104">A geometry shader with stream out is declared with a particular syntax.</span></span> <span data-ttu-id="80aec-105">Cette rubrique décrit la syntaxe.</span><span class="sxs-lookup"><span data-stu-id="80aec-105">This topic describes the syntax.</span></span> <span data-ttu-id="80aec-106">Dans le runtime Effect, cette syntaxe est convertie en un appel à [**ID3D11Device :: CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput).</span><span class="sxs-lookup"><span data-stu-id="80aec-106">In the effect runtime, this syntax will be converted to a call to [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput).</span></span>

## <a name="construct-syntax"></a><span data-ttu-id="80aec-107">Syntaxe de construction</span><span class="sxs-lookup"><span data-stu-id="80aec-107">Construct Syntax</span></span>


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0" )
```





| <span data-ttu-id="80aec-108">Nom</span><span class="sxs-lookup"><span data-stu-id="80aec-108">Name</span></span>                   | <span data-ttu-id="80aec-109">Description</span><span class="sxs-lookup"><span data-stu-id="80aec-109">Description</span></span>                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80aec-110">**StreamingShaderVar**</span><span class="sxs-lookup"><span data-stu-id="80aec-110">**StreamingShaderVar**</span></span> | <span data-ttu-id="80aec-111">facultatif.</span><span class="sxs-lookup"><span data-stu-id="80aec-111">Optional.</span></span> <span data-ttu-id="80aec-112">Chaîne ASCI qui identifie de façon unique le nom d’une variable de nuanceur Geometry avec un flux sortant. Cela est facultatif, car ConstructGSWithSO peut être placé directement dans un appel SetGeometryShader ou BindInterfaces.</span><span class="sxs-lookup"><span data-stu-id="80aec-112">An ASCI string that uniquely identifies the name of a geometry shader variable with stream out. This is optional because ConstructGSWithSO can be placed directly in a SetGeometryShader or BindInterfaces call.</span></span> |
| <span data-ttu-id="80aec-113">**ShaderVar**</span><span class="sxs-lookup"><span data-stu-id="80aec-113">**ShaderVar**</span></span>          | <span data-ttu-id="80aec-114">Une variable de nuanceur Geometry ou vertex.</span><span class="sxs-lookup"><span data-stu-id="80aec-114">A geometry shader or vertex shader variable.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="80aec-115">**OutputDecl0**</span><span class="sxs-lookup"><span data-stu-id="80aec-115">**OutputDecl0**</span></span>        | <span data-ttu-id="80aec-116">Une chaîne qui définit les sorties de nuanceur dans le flux 0 sont transmises en continu. Voir ci-dessous pour connaître la syntaxe.</span><span class="sxs-lookup"><span data-stu-id="80aec-116">A string defining which shader outputs in stream 0 are streamed out. See below for syntax.</span></span>                                                                                                                                 |



 

<span data-ttu-id="80aec-117">Il s’agit de la syntaxe définie dans \_ les \_ fichiers FX 4 0.</span><span class="sxs-lookup"><span data-stu-id="80aec-117">This is the syntax was defined in fx\_4\_0 files.</span></span> <span data-ttu-id="80aec-118">Notez que dans \_ \_ les nuanciers GS 4 0 et vs \_ x, il n’y a qu’un seul flux de données.</span><span class="sxs-lookup"><span data-stu-id="80aec-118">Note that in gs\_4\_0 and vs\_x shaders, there is only one stream of data.</span></span> <span data-ttu-id="80aec-119">Le nuanceur résultant produira un flux à la fois dans l’unité de diffusion en continu et l’unité de rastérisation.</span><span class="sxs-lookup"><span data-stu-id="80aec-119">The resulting shader will output one stream to both the stream out unit and the rasterizer unit.</span></span>


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0", "OutputDecl1", "OutputDecl2", 
"OutputDecl3", RasterizedStream )
```





| <span data-ttu-id="80aec-120">Nom</span><span class="sxs-lookup"><span data-stu-id="80aec-120">Name</span></span>                   | <span data-ttu-id="80aec-121">Description</span><span class="sxs-lookup"><span data-stu-id="80aec-121">Description</span></span>                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80aec-122">**StreamingShaderVar**</span><span class="sxs-lookup"><span data-stu-id="80aec-122">**StreamingShaderVar**</span></span> | <span data-ttu-id="80aec-123">facultatif.</span><span class="sxs-lookup"><span data-stu-id="80aec-123">Optional.</span></span> <span data-ttu-id="80aec-124">Chaîne ASCI qui identifie de façon unique le nom d’une variable de nuanceur Geometry avec un flux sortant. Cela est facultatif, car ConstructGSWithSO peut être placé directement dans un appel SetGeometryShader ou BindInterfaces.</span><span class="sxs-lookup"><span data-stu-id="80aec-124">An ASCI string that uniquely identifies the name of a geometry shader variable with stream out. This is optional because ConstructGSWithSO can be placed directly in a SetGeometryShader or BindInterfaces call.</span></span> |
| <span data-ttu-id="80aec-125">**ShaderVar**</span><span class="sxs-lookup"><span data-stu-id="80aec-125">**ShaderVar**</span></span>          | <span data-ttu-id="80aec-126">Une variable de nuanceur Geometry ou vertex.</span><span class="sxs-lookup"><span data-stu-id="80aec-126">A geometry shader or vertex shader variable.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="80aec-127">**OutputDecl0**</span><span class="sxs-lookup"><span data-stu-id="80aec-127">**OutputDecl0**</span></span>        | <span data-ttu-id="80aec-128">Une chaîne qui définit les sorties de nuanceur dans le flux 0 sont transmises en continu. Voir ci-dessous pour connaître la syntaxe.</span><span class="sxs-lookup"><span data-stu-id="80aec-128">A string defining which shader outputs in stream 0 are streamed out. See below for syntax.</span></span>                                                                                                                                 |
| <span data-ttu-id="80aec-129">**OutputDecl1**</span><span class="sxs-lookup"><span data-stu-id="80aec-129">**OutputDecl1**</span></span>        | <span data-ttu-id="80aec-130">Une chaîne qui définit les sorties de nuanceur dans le flux 1 sont transmises en continu. Voir ci-dessous pour connaître la syntaxe.</span><span class="sxs-lookup"><span data-stu-id="80aec-130">A string defining which shader outputs in stream 1 are streamed out. See below for syntax.</span></span>                                                                                                                                 |
| <span data-ttu-id="80aec-131">**OutputDecl2**</span><span class="sxs-lookup"><span data-stu-id="80aec-131">**OutputDecl2**</span></span>        | <span data-ttu-id="80aec-132">Une chaîne qui définit les sorties de nuanceur dans le flux 2 sont transmises en continu. Voir ci-dessous pour connaître la syntaxe.</span><span class="sxs-lookup"><span data-stu-id="80aec-132">A string defining which shader outputs in stream 2 are streamed out. See below for syntax.</span></span>                                                                                                                                 |
| <span data-ttu-id="80aec-133">**OutputDecl3**</span><span class="sxs-lookup"><span data-stu-id="80aec-133">**OutputDecl3**</span></span>        | <span data-ttu-id="80aec-134">Une chaîne qui définit les sorties de nuanceur dans le flux 3 sont transmises en continu. Voir ci-dessous pour connaître la syntaxe.</span><span class="sxs-lookup"><span data-stu-id="80aec-134">A string defining which shader outputs in stream 3 are streamed out. See below for syntax.</span></span>                                                                                                                                 |
| <span data-ttu-id="80aec-135">**RasterizedStream**</span><span class="sxs-lookup"><span data-stu-id="80aec-135">**RasterizedStream**</span></span>   | <span data-ttu-id="80aec-136">Entier spécifiant le flux qui sera envoyé au rastériseur.</span><span class="sxs-lookup"><span data-stu-id="80aec-136">An integer specifying which stream will be sent to the rasterizer.</span></span>                                                                                                                                                         |



 

<span data-ttu-id="80aec-137">Notez que \_ \_ les nuanceurs GS 5 0 peuvent définir jusqu’à quatre flux de données.</span><span class="sxs-lookup"><span data-stu-id="80aec-137">Note that gs\_5\_0 shaders can define up to four streams of data.</span></span> <span data-ttu-id="80aec-138">Le nuanceur résultant produira un flux de sortie vers l’unité d’extraction de flux pour chaque déclaration de sortie non **null** et un flux de l’unité de rastérisation.</span><span class="sxs-lookup"><span data-stu-id="80aec-138">The resulting shader will output one stream to the stream out unit for each non-**NULL** output declaration and one stream the rasterizer unit.</span></span>

## <a name="stream-out-declaration-syntax"></a><span data-ttu-id="80aec-139">Syntaxe de déclaration de flux de sortie</span><span class="sxs-lookup"><span data-stu-id="80aec-139">Stream Out Declaration Syntax</span></span>


```
" [ Buffer: ] Semantic[ SemanticIndex ] [ .Mask ]; [ ... ; ] ... [ ... ;]"
```





| <span data-ttu-id="80aec-140">Nom</span><span class="sxs-lookup"><span data-stu-id="80aec-140">Name</span></span>              | <span data-ttu-id="80aec-141">Description</span><span class="sxs-lookup"><span data-stu-id="80aec-141">Description</span></span>                                                                                           |
|-------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80aec-142">**Buffer**</span><span class="sxs-lookup"><span data-stu-id="80aec-142">**Buffer**</span></span>        | <span data-ttu-id="80aec-143">facultatif.</span><span class="sxs-lookup"><span data-stu-id="80aec-143">Optional.</span></span> <span data-ttu-id="80aec-144">Un entier, 0 <= buffer < 4, spécifiant la mémoire tampon de sortie de flux vers laquelle la valeur doit être redirigée.</span><span class="sxs-lookup"><span data-stu-id="80aec-144">An integer, 0 <= Buffer < 4, specifying which stream out buffer the value will go to.</span></span> |
| <span data-ttu-id="80aec-145">**Équivalent**</span><span class="sxs-lookup"><span data-stu-id="80aec-145">**Semantic**</span></span>      | <span data-ttu-id="80aec-146">Chaîne, avec SemanticIndex, spécifiant la valeur à générer.</span><span class="sxs-lookup"><span data-stu-id="80aec-146">A string, along with SemanticIndex, specifying which value to output.</span></span>                                 |
| <span data-ttu-id="80aec-147">**SemanticIndex**</span><span class="sxs-lookup"><span data-stu-id="80aec-147">**SemanticIndex**</span></span> | <span data-ttu-id="80aec-148">facultatif.</span><span class="sxs-lookup"><span data-stu-id="80aec-148">Optional.</span></span> <span data-ttu-id="80aec-149">Index associé à la sémantique.</span><span class="sxs-lookup"><span data-stu-id="80aec-149">The index associated with Semantic.</span></span>                                                         |
| <span data-ttu-id="80aec-150">**Filtrage**</span><span class="sxs-lookup"><span data-stu-id="80aec-150">**Mask**</span></span>          | <span data-ttu-id="80aec-151">facultatif.</span><span class="sxs-lookup"><span data-stu-id="80aec-151">Optional.</span></span> <span data-ttu-id="80aec-152">Masque de composant indiquant les composants de la valeur à générer.</span><span class="sxs-lookup"><span data-stu-id="80aec-152">A component mask, indicating which components of the value to output.</span></span>                       |



 

<span data-ttu-id="80aec-153">Il existe une sémantique spéciale, nommée « $SKIP », qui indique une sémantique vide, laissant la mémoire correspondante dans le flux sans toucher.</span><span class="sxs-lookup"><span data-stu-id="80aec-153">There is one special Semantic, labeled "$SKIP" which indicates an empty semantic, leaving the corresponding memory in the stream out buffer untouched.</span></span> <span data-ttu-id="80aec-154">La sémantique $SKIP ne peut pas avoir de SemanticIndex, mais peut avoir un masque.</span><span class="sxs-lookup"><span data-stu-id="80aec-154">The $SKIP semantic cannot have a SemanticIndex, but can have a Mask.</span></span>

<span data-ttu-id="80aec-155">La déclaration out du flux entier peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="80aec-155">The entire stream out declaration can be **NULL**.</span></span>

## <a name="example"></a><span data-ttu-id="80aec-156">Exemple</span><span class="sxs-lookup"><span data-stu-id="80aec-156">Example</span></span>


```
struct GSOutput
{
int4 Pos : Position;
int4 Color : Color;
int4 Texcoord : Texcoord;
};

[maxvertexcount(1)]
void gsBase (inout PointStream<GSOutput> OutputStream, inout PointStream<GSOutput> OutputStream1)
{
GSOutput output;
output.Pos = int4(1,2,3,4);
output.Color = int4(5,6,7,8);
output.Texcoord = int4(9,10,11,12);
OutputStream.Append(output);

output.Pos = int4(1,2,3,4);
    output.Color = int4(5,6,7,8);
output.Texcoord = int4(9,10,11,12);
OutputStream1.Append(output);
};


GeometryShader pGSComp = CompileShader(gs_5_0, gsBase());
GeometryShader pGSwSO = ConstructGSWithSO(pGSComp, "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                                   "3:Texcoord.xyzw; 3:$SKIP.x;", NULL, NULL, 1);

// The following two passes perform the same operation
technique11 SOPoints
{
    pass 
    {
        SetGeometryShader(ConstructGSWithSO(pGSComp, "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                                     "3:Texcoord.xyzw; 3:$SKIP.x;", NULL, NULL, 1));
    }
    pass 
    {
        SetGeometryShader(pGSwSO);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="80aec-157">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="80aec-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80aec-158">Effets (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="80aec-158">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 





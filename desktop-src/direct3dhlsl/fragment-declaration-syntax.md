---
title: Syntaxe de la déclaration de fragment (Direct3D 9 HLSL)
description: Chaque fonction HLSL (High Level Shader Language) de Microsoft peut être convertie en fragment de nuanceur avec l’ajout d’une déclaration de fragment.
ms.assetid: 34ceef8c-8fb9-4c73-86cc-014b7a2ee4d7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9c9090caec35bfc5e46d7024bf6de44d865d4ad6
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998306"
---
# <a name="fragment-declaration-syntax-direct3d-9-hlsl"></a><span data-ttu-id="bae1e-103">Syntaxe de la déclaration de fragment (Direct3D 9 HLSL)</span><span class="sxs-lookup"><span data-stu-id="bae1e-103">Fragment Declaration Syntax (Direct3D 9 HLSL)</span></span>

<span data-ttu-id="bae1e-104">Chaque fonction HLSL (High Level Shader Language) de Microsoft peut être convertie en fragment de nuanceur avec l’ajout d’une déclaration de fragment.</span><span class="sxs-lookup"><span data-stu-id="bae1e-104">Each Microsoft High Level Shader Language (HLSL) function can be converted into a shader fragment with the addition of a fragment declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="bae1e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bae1e-105">Syntax</span></span>


```
fragmentKeyword FragmentName = compile_fragment shaderProfile FunctionName();
```



<span data-ttu-id="bae1e-106">où :</span><span class="sxs-lookup"><span data-stu-id="bae1e-106">where:</span></span>



|                   |                                                                                                                                                                                                                                                       |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bae1e-107">fragmentKeyword</span><span class="sxs-lookup"><span data-stu-id="bae1e-107">fragmentKeyword</span></span>   | <span data-ttu-id="bae1e-108">Mot clé requis.</span><span class="sxs-lookup"><span data-stu-id="bae1e-108">Required keyword.</span></span> <span data-ttu-id="bae1e-109">Pixelfragment ou vertexfragment.</span><span class="sxs-lookup"><span data-stu-id="bae1e-109">Either pixelfragment or vertexfragment.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="bae1e-110">FragmentName</span><span class="sxs-lookup"><span data-stu-id="bae1e-110">FragmentName</span></span>      | <span data-ttu-id="bae1e-111">Chaîne de texte ASCII qui spécifie le nom du fragment compilé.</span><span class="sxs-lookup"><span data-stu-id="bae1e-111">An ASCII text string that specifies the compiled fragment name.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="bae1e-112">fragment de compilation \_</span><span class="sxs-lookup"><span data-stu-id="bae1e-112">compile\_fragment</span></span> | <span data-ttu-id="bae1e-113">Mot clé requis.</span><span class="sxs-lookup"><span data-stu-id="bae1e-113">Required keyword.</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="bae1e-114">shaderProfile</span><span class="sxs-lookup"><span data-stu-id="bae1e-114">shaderProfile</span></span>     | <span data-ttu-id="bae1e-115">Modèle de nuanceur à compiler.</span><span class="sxs-lookup"><span data-stu-id="bae1e-115">The shader model to compile against.</span></span> <span data-ttu-id="bae1e-116">Tout profil de nuanceur de sommets valide (consultez [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) ou profil de nuanceur de pixels (voir [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)).</span><span class="sxs-lookup"><span data-stu-id="bae1e-116">Any valid vertex shader profile (see [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) or pixel shader profile (see [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)).</span></span> |
| <span data-ttu-id="bae1e-117">Nomfonction ()</span><span class="sxs-lookup"><span data-stu-id="bae1e-117">FunctionName()</span></span>    | <span data-ttu-id="bae1e-118">Nom de la fonction de nuanceur, suivi de parenthèses.</span><span class="sxs-lookup"><span data-stu-id="bae1e-118">The shader function name, followed by parentheses.</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="bae1e-119">Les paramètres de fragment partagés sont marqués en ajoutant un \_ préfixe’r’à leur sémantique.</span><span class="sxs-lookup"><span data-stu-id="bae1e-119">Shared fragment parameters are marked by adding an 'r\_' prefix to their semantic.</span></span>


```
void AmbientDiffuse( float3 vPosWorld: r_PosWorld,
                     float3 vNormalWorld: r_NormalWorld,
                     out float4 vColor: COLOR0 )
{  
    // Compute the light vector
    float3 vLight = normalize( g_vLightPosition - vPosWorld );
    
    // Compute the ambient and diffuse components of illumination
    vColor = g_vLightColor * g_vMaterialAmbient;
    vColor += g_vLightColor * g_vMaterialDiffuse * saturate( dot( vLight, vNormalWorld ) );
}
vertexfragment AmbientDiffuseFragment = compile_fragment vs_1_1 AmbientDiffuse();
```



<span data-ttu-id="bae1e-120">Dans cet exemple, les \_ sémantiques r PosWorld et r \_ NormalWorld identifient que ces deux paramètres sont des paramètres partagés parmi d’autres fragments.</span><span class="sxs-lookup"><span data-stu-id="bae1e-120">In this example, the r\_PosWorld and r\_NormalWorld semantics identify that these two parameters are shared parameters among other fragments.</span></span>

> [!Note]  
> <span data-ttu-id="bae1e-121">L’éditeur de liens de fragment était une technologie Microsoft Direct3D 9 dans D3DX 9.</span><span class="sxs-lookup"><span data-stu-id="bae1e-121">Fragment linker was a Microsoft Direct3D 9 technology in D3DX 9.</span></span> <span data-ttu-id="bae1e-122">Fragment Linker était un outil (Flink.exe), une API D3DX 9 et une amélioration HLSL.</span><span class="sxs-lookup"><span data-stu-id="bae1e-122">Fragment linker was a tool (Flink.exe), a D3DX 9 API, and an HLSL enhancement.</span></span> <span data-ttu-id="bae1e-123">L’éditeur de liens de fragment a été supprimé depuis la version du SDK DirectX du 2009 août.</span><span class="sxs-lookup"><span data-stu-id="bae1e-123">Fragment linker was dropped as of the August 2009 DirectX SDK release.</span></span> <span data-ttu-id="bae1e-124">L’éditeur de liens fragment n’est jamais appliqué à Microsoft Direct3D 10, Microsoft Direct3D 10,1 ou Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="bae1e-124">Fragment linker never applied to Microsoft Direct3D 10, Microsoft Direct3D 10.1, or Microsoft Direct3D 11.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="bae1e-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bae1e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bae1e-126">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bae1e-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 

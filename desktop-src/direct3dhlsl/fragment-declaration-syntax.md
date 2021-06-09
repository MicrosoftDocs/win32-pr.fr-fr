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
ms.openlocfilehash: 60ac1153ff3491bc904f4f759f6653cb4243adff
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825726"
---
# <a name="fragment-declaration-syntax-direct3d-9-hlsl"></a><span data-ttu-id="b1535-103">Syntaxe de la déclaration de fragment (Direct3D 9 HLSL)</span><span class="sxs-lookup"><span data-stu-id="b1535-103">Fragment Declaration Syntax (Direct3D 9 HLSL)</span></span>

<span data-ttu-id="b1535-104">Chaque fonction HLSL (High Level Shader Language) de Microsoft peut être convertie en fragment de nuanceur avec l’ajout d’une déclaration de fragment.</span><span class="sxs-lookup"><span data-stu-id="b1535-104">Each Microsoft High Level Shader Language (HLSL) function can be converted into a shader fragment with the addition of a fragment declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1535-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1535-105">Syntax</span></span>


```
fragmentKeyword FragmentName = compile_fragment shaderProfile FunctionName();
```



<span data-ttu-id="b1535-106">où :</span><span class="sxs-lookup"><span data-stu-id="b1535-106">where:</span></span>



| <span data-ttu-id="b1535-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1535-107">Value</span></span>                  | <span data-ttu-id="b1535-108">Description</span><span class="sxs-lookup"><span data-stu-id="b1535-108">Description</span></span>                                                                                                                                                                                                                                                      |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1535-109">fragmentKeyword</span><span class="sxs-lookup"><span data-stu-id="b1535-109">fragmentKeyword</span></span>   | <span data-ttu-id="b1535-110">Mot clé requis.</span><span class="sxs-lookup"><span data-stu-id="b1535-110">Required keyword.</span></span> <span data-ttu-id="b1535-111">Pixelfragment ou vertexfragment.</span><span class="sxs-lookup"><span data-stu-id="b1535-111">Either pixelfragment or vertexfragment.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="b1535-112">FragmentName</span><span class="sxs-lookup"><span data-stu-id="b1535-112">FragmentName</span></span>      | <span data-ttu-id="b1535-113">Chaîne de texte ASCII qui spécifie le nom du fragment compilé.</span><span class="sxs-lookup"><span data-stu-id="b1535-113">An ASCII text string that specifies the compiled fragment name.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="b1535-114">fragment de compilation \_</span><span class="sxs-lookup"><span data-stu-id="b1535-114">compile\_fragment</span></span> | <span data-ttu-id="b1535-115">Mot clé requis.</span><span class="sxs-lookup"><span data-stu-id="b1535-115">Required keyword.</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="b1535-116">shaderProfile</span><span class="sxs-lookup"><span data-stu-id="b1535-116">shaderProfile</span></span>     | <span data-ttu-id="b1535-117">Modèle de nuanceur à compiler.</span><span class="sxs-lookup"><span data-stu-id="b1535-117">The shader model to compile against.</span></span> <span data-ttu-id="b1535-118">Tout profil de nuanceur de sommets valide (consultez [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) ou profil de nuanceur de pixels (voir [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)).</span><span class="sxs-lookup"><span data-stu-id="b1535-118">Any valid vertex shader profile (see [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) or pixel shader profile (see [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)).</span></span> |
| <span data-ttu-id="b1535-119">Nomfonction ()</span><span class="sxs-lookup"><span data-stu-id="b1535-119">FunctionName()</span></span>    | <span data-ttu-id="b1535-120">Nom de la fonction de nuanceur, suivi de parenthèses.</span><span class="sxs-lookup"><span data-stu-id="b1535-120">The shader function name, followed by parentheses.</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="b1535-121">Les paramètres de fragment partagés sont marqués en ajoutant un \_ préfixe’r’à leur sémantique.</span><span class="sxs-lookup"><span data-stu-id="b1535-121">Shared fragment parameters are marked by adding an 'r\_' prefix to their semantic.</span></span>


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



<span data-ttu-id="b1535-122">Dans cet exemple, les \_ sémantiques r PosWorld et r \_ NormalWorld identifient que ces deux paramètres sont des paramètres partagés parmi d’autres fragments.</span><span class="sxs-lookup"><span data-stu-id="b1535-122">In this example, the r\_PosWorld and r\_NormalWorld semantics identify that these two parameters are shared parameters among other fragments.</span></span>

> [!Note]  
> <span data-ttu-id="b1535-123">L’éditeur de liens de fragment était une technologie Microsoft Direct3D 9 dans D3DX 9.</span><span class="sxs-lookup"><span data-stu-id="b1535-123">Fragment linker was a Microsoft Direct3D 9 technology in D3DX 9.</span></span> <span data-ttu-id="b1535-124">Fragment Linker était un outil (Flink.exe), une API D3DX 9 et une amélioration HLSL.</span><span class="sxs-lookup"><span data-stu-id="b1535-124">Fragment linker was a tool (Flink.exe), a D3DX 9 API, and an HLSL enhancement.</span></span> <span data-ttu-id="b1535-125">L’éditeur de liens de fragment a été supprimé depuis la version du SDK DirectX du 2009 août.</span><span class="sxs-lookup"><span data-stu-id="b1535-125">Fragment linker was dropped as of the August 2009 DirectX SDK release.</span></span> <span data-ttu-id="b1535-126">L’éditeur de liens fragment n’est jamais appliqué à Microsoft Direct3D 10, Microsoft Direct3D 10,1 ou Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="b1535-126">Fragment linker never applied to Microsoft Direct3D 10, Microsoft Direct3D 10.1, or Microsoft Direct3D 11.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b1535-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b1535-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1535-128">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b1535-128">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 

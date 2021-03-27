---
title: Syntaxe des fonctions Effect (Direct3D 11)
description: Une fonction Effect est écrite en langage HLSL et est déclarée avec la syntaxe décrite dans cette section.
ms.assetid: 5e12ba65-98bf-4f21-be75-602687157eb1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f569211d5f178b96cf7415478010285e7a836b58
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727380"
---
# <a name="effect-function-syntax-direct3d-11"></a><span data-ttu-id="d3587-103">Syntaxe des fonctions Effect (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="d3587-103">Effect Function Syntax (Direct3D 11)</span></span>

<span data-ttu-id="d3587-104">Une fonction Effect est écrite en langage HLSL et est déclarée avec la syntaxe décrite dans cette section.</span><span class="sxs-lookup"><span data-stu-id="d3587-104">An effect function is written in HLSL and is declared with the syntax described in this section.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3587-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3587-105">Syntax</span></span>

<span data-ttu-id="d3587-106"> *Nomdefonction nomfonction* ( \[ *argumentlist* \] )</span><span class="sxs-lookup"><span data-stu-id="d3587-106">*ReturnType* *FunctionName* ( \[ *ArgumentList* \] )</span></span>

<span data-ttu-id="d3587-107">{</span><span class="sxs-lookup"><span data-stu-id="d3587-107">{</span></span>

<dl> <span data-ttu-id="d3587-108">\[ *Instructions* \]</span><span class="sxs-lookup"><span data-stu-id="d3587-108">\[ *Statements* \]</span></span>
</dl>

<span data-ttu-id="d3587-109">};</span><span class="sxs-lookup"><span data-stu-id="d3587-109">};</span></span>



| <span data-ttu-id="d3587-110">Nom</span><span class="sxs-lookup"><span data-stu-id="d3587-110">Name</span></span>         | <span data-ttu-id="d3587-111">Description</span><span class="sxs-lookup"><span data-stu-id="d3587-111">Description</span></span>                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3587-112">ReturnType</span><span class="sxs-lookup"><span data-stu-id="d3587-112">ReturnType</span></span>   | <span data-ttu-id="d3587-113">Tout [type HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax)</span><span class="sxs-lookup"><span data-stu-id="d3587-113">Any [HLSL type](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax)</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="d3587-114">FunctionName</span><span class="sxs-lookup"><span data-stu-id="d3587-114">FunctionName</span></span> | <span data-ttu-id="d3587-115">Chaîne ASCII qui identifie de façon unique le nom de la fonction de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="d3587-115">An ASCII string that uniquely identifies the name of the shader function.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="d3587-116">ArgumentList</span><span class="sxs-lookup"><span data-stu-id="d3587-116">ArgumentList</span></span> | <span data-ttu-id="d3587-117">Un ou plusieurs arguments, séparés par des virgules (consultez [arguments de fonction (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters)).</span><span class="sxs-lookup"><span data-stu-id="d3587-117">One or more arguments, separated by commas (see [Function Arguments (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters)).</span></span>                                                                                                                             |
| <span data-ttu-id="d3587-118">Instructions</span><span class="sxs-lookup"><span data-stu-id="d3587-118">Statements</span></span>   | <span data-ttu-id="d3587-119">Une ou plusieurs instructions (consultez [instructions (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-statements)) qui composent le corps de la fonction.</span><span class="sxs-lookup"><span data-stu-id="d3587-119">One or more statements (see [Statements (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-statements)) that make up the body of the function.</span></span> <span data-ttu-id="d3587-120">Si une fonction est définie sans corps, elle est considérée comme un prototype ; et doivent être redéfinis avec un corps avant l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="d3587-120">If a function is defined without a body, it is considered to be a prototype; and must be redefined with a body before use.</span></span> |



 

<span data-ttu-id="d3587-121">Une fonction Effect peut être un nuanceur ou il peut simplement s’agir d’une fonction appelée par un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="d3587-121">An effect function may be a shader or it may simply be a function called by a shader.</span></span> <span data-ttu-id="d3587-122">Une fonction est identifiée de manière unique par son nom, les types de ses paramètres et la plateforme cible ; par conséquent, les fonctions peuvent être surchargées.</span><span class="sxs-lookup"><span data-stu-id="d3587-122">A function is uniquely identified by its name, the types of its parameters, and the target platform; therefore, functions can be overloaded.</span></span> <span data-ttu-id="d3587-123">Toute fonction HLSL valide doit respecter ce format ; pour obtenir une liste plus détaillée de la syntaxe des fonctions HLSL, consultez [fonctions (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-functions).</span><span class="sxs-lookup"><span data-stu-id="d3587-123">Any valid HLSL function should fit this format; for a more detailed list of syntax for HLSL functions, see [Functions (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-functions).</span></span>

## <a name="example"></a><span data-ttu-id="d3587-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="d3587-124">Example</span></span>

<span data-ttu-id="d3587-125">Voici un exemple de fonction de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="d3587-125">The following is an example of a pixel shader function.</span></span>


```
       
PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                         uniform bool bTexture ) 
{ 
    PS_OUTPUT Output;

    // Lookup mesh texture and modulate it with diffuse
    if( bTexture )
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) *  
                              In.Diffuse;
    else
        Output.RGBColor = In.Diffuse;

    return Output;
}
```



## <a name="related-topics"></a><span data-ttu-id="d3587-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d3587-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3587-127">Format d’effet</span><span class="sxs-lookup"><span data-stu-id="d3587-127">Effect Format</span></span>](d3d11-effect-format.md)
</dt> </dl>

 

 
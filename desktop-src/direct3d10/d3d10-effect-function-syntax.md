---
description: Une fonction Effect est écrite en langage HLSL et est déclarée avec la syntaxe suivante.
ms.assetid: 5ac85f09-50ac-4e8f-b4d2-ae8306b59348
title: Syntaxe des fonctions Effect (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88521eeb85d1e5f54500a045fe5dcfd81d6be2cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483200"
---
# <a name="effect-function-syntax-direct3d-10"></a><span data-ttu-id="d58c0-103">Syntaxe des fonctions Effect (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="d58c0-103">Effect Function Syntax (Direct3D 10)</span></span>

<span data-ttu-id="d58c0-104">Une fonction Effect est écrite en langage HLSL et est déclarée avec la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="d58c0-104">An effect function is written in HLSL and is declared with the following syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="d58c0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d58c0-105">Syntax</span></span>

<span data-ttu-id="d58c0-106"> *Nomdefonction nomfonction* ( \[ *argumentlist* \] )</span><span class="sxs-lookup"><span data-stu-id="d58c0-106">*ReturnType* *FunctionName* ( \[ *ArgumentList* \] )</span></span>

<span data-ttu-id="d58c0-107">{</span><span class="sxs-lookup"><span data-stu-id="d58c0-107">{</span></span>

<dl> <span data-ttu-id="d58c0-108">\[ *Instructions* \]</span><span class="sxs-lookup"><span data-stu-id="d58c0-108">\[ *Statements* \]</span></span>
</dl>

<span data-ttu-id="d58c0-109">};</span><span class="sxs-lookup"><span data-stu-id="d58c0-109">};</span></span>



| <span data-ttu-id="d58c0-110">Nom</span><span class="sxs-lookup"><span data-stu-id="d58c0-110">Name</span></span>         | <span data-ttu-id="d58c0-111">Description</span><span class="sxs-lookup"><span data-stu-id="d58c0-111">Description</span></span>                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d58c0-112">ReturnType</span><span class="sxs-lookup"><span data-stu-id="d58c0-112">ReturnType</span></span>   | <span data-ttu-id="d58c0-113">Tout [type HLSL](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md)</span><span class="sxs-lookup"><span data-stu-id="d58c0-113">Any [HLSL type](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md)</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="d58c0-114">FunctionName</span><span class="sxs-lookup"><span data-stu-id="d58c0-114">FunctionName</span></span> | <span data-ttu-id="d58c0-115">Chaîne ASCII qui identifie de façon unique le nom de la fonction de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="d58c0-115">An ASCII string that uniquely identifies the name of the shader function.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="d58c0-116">ArgumentList</span><span class="sxs-lookup"><span data-stu-id="d58c0-116">ArgumentList</span></span> | <span data-ttu-id="d58c0-117">Un ou plusieurs arguments, séparés par des virgules (consultez [arguments de fonction (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-function-parameters.md)).</span><span class="sxs-lookup"><span data-stu-id="d58c0-117">One or more arguments, separated by commas (see [Function Arguments (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-function-parameters.md)).</span></span>                                                                                                                             |
| <span data-ttu-id="d58c0-118">Instructions</span><span class="sxs-lookup"><span data-stu-id="d58c0-118">Statements</span></span>   | <span data-ttu-id="d58c0-119">Une ou plusieurs instructions (consultez [instructions (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-statements.md)) qui composent le corps de la fonction.</span><span class="sxs-lookup"><span data-stu-id="d58c0-119">One or more statements (see [Statements (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-statements.md)) that make up the body of the function.</span></span> <span data-ttu-id="d58c0-120">Si une fonction est définie sans corps, elle est considérée comme un prototype ; et doivent être redéfinis avec un corps avant l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="d58c0-120">If a function is defined without a body, it is considered to be a prototype; and must be redefined with a body before use.</span></span> |



 

<span data-ttu-id="d58c0-121">Une fonction Effect peut être un nuanceur ou il peut simplement s’agir d’une fonction appelée par un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="d58c0-121">An effect function may be a shader or it may simply be a function called by a shader.</span></span> <span data-ttu-id="d58c0-122">Une fonction est identifiée de manière unique par son nom, les types de ses paramètres et la plateforme cible ; par conséquent, les fonctions peuvent être surchargées.</span><span class="sxs-lookup"><span data-stu-id="d58c0-122">A function is uniquely identified by its name, the types of its parameters, and the target platform; therefore, functions can be overloaded.</span></span> <span data-ttu-id="d58c0-123">Toute fonction HLSL valide doit respecter ce format ; pour obtenir une liste plus détaillée de la syntaxe des fonctions HLSL, consultez [fonctions (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-functions.md).</span><span class="sxs-lookup"><span data-stu-id="d58c0-123">Any valid HLSL function should fit this format; for a more detailed list of syntax for HLSL functions, see [Functions (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-functions.md).</span></span>

## <a name="example"></a><span data-ttu-id="d58c0-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="d58c0-124">Example</span></span>

<span data-ttu-id="d58c0-125">L' [exemple BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) utilise à la fois un nuanceur de pixels et un nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="d58c0-125">The [BasicHLSL10 sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) uses both a pixel shader and a vertex shader.</span></span> <span data-ttu-id="d58c0-126">La fonction de nuanceur de pixels est appelée RenderScenePS et est illustrée ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="d58c0-126">The pixel shader function is called RenderScenePS and is shown below.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d58c0-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d58c0-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d58c0-128">Format d’effet</span><span class="sxs-lookup"><span data-stu-id="d58c0-128">Effect Format</span></span>](d3d10-effect-format.md)
</dt> </dl>

 

 

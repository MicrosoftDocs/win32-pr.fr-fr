---
title: Syntaxe de la déclaration des fonctions
description: Les fonctions HLSL sont déclarées avec la syntaxe suivante.
ms.assetid: f8968de2-7b2d-4a2e-8312-cec5b652f700
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 847194c08b865542cff1deb20c8518a7e4b62ab9
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119044"
---
# <a name="function-declaration-syntax"></a><span data-ttu-id="27417-103">Syntaxe de la déclaration des fonctions</span><span class="sxs-lookup"><span data-stu-id="27417-103">Function Declaration Syntax</span></span>

<span data-ttu-id="27417-104">Les fonctions HLSL sont déclarées avec la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="27417-104">HLSL functions are declared with the following syntax.</span></span>

<span data-ttu-id="27417-105">\[*StorageClass* \] \[clipplanes () \] \[ \] \_ *nom* de valeur de retour précis ( \[ *argumentlist* \] ) \[ : *sémantique* \] { \[ *StatementBlock* \] };</span><span class="sxs-lookup"><span data-stu-id="27417-105">\[*StorageClass*\] \[clipplanes()\] \[precise\] Return\_Value *Name* ( \[*ArgumentList*\] ) \[: *Semantic*\] {   \[*StatementBlock*\] };</span></span>



 

## <a name="parameters"></a><span data-ttu-id="27417-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="27417-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27417-107"><span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*StorageClass*</span><span class="sxs-lookup"><span data-stu-id="27417-107"><span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*StorageClass*</span></span>
</dt> <dd>

<span data-ttu-id="27417-108">Modificateur qui redéfinit une déclaration de fonction.</span><span class="sxs-lookup"><span data-stu-id="27417-108">Modifier that redefines a function declaration.</span></span> <span data-ttu-id="27417-109">**inline** est actuellement la seule valeur de modificateur.</span><span class="sxs-lookup"><span data-stu-id="27417-109">**inline** is currently the only modifier value.</span></span> <span data-ttu-id="27417-110">La valeur du modificateur doit être **inline** , car il s’agit également de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="27417-110">The modifier value must be **inline** because it is also the default value.</span></span> <span data-ttu-id="27417-111">Par conséquent, une fonction est Inline, que **vous spécifiiez inline et** que toutes les fonctions en HLSL soient Inline.</span><span class="sxs-lookup"><span data-stu-id="27417-111">Therefore, a function is inline regardless of whether you specify **inline**, and all functions in HLSL are inline.</span></span> <span data-ttu-id="27417-112">Une fonction inline génère une copie du corps de la fonction (lors de la compilation) pour chaque appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="27417-112">An inline function generates a copy of the function body (when compiling) for each function call.</span></span> <span data-ttu-id="27417-113">Cela permet de réduire la surcharge liée à l’appel de la fonction.</span><span class="sxs-lookup"><span data-stu-id="27417-113">This is done to decrease the overhead of calling the function.</span></span>

</dd> <dt>

<span data-ttu-id="27417-114"><span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*Clipplanes*</span><span class="sxs-lookup"><span data-stu-id="27417-114"><span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*Clipplanes*</span></span>
</dt> <dd>

<span data-ttu-id="27417-115">Liste facultative de plans de clip, qui correspond à 6 plans de clip spécifiés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="27417-115">Optional list of clip planes, which is up to 6 user-specified clip planes.</span></span> <span data-ttu-id="27417-116">Il s’agit d’un mécanisme de remplacement pour [SV \_ ClipDistance](dx-graphics-hlsl-semantics.md) qui fonctionne sur le [niveau de fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x et supérieur.</span><span class="sxs-lookup"><span data-stu-id="27417-116">This is an alternate mechanism for [SV\_ClipDistance](dx-graphics-hlsl-semantics.md) that works on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span>

</dd> <dt>

<span data-ttu-id="27417-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nomme*</span><span class="sxs-lookup"><span data-stu-id="27417-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="27417-118">Chaîne ASCII qui identifie de façon unique le nom de la fonction de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="27417-118">An ASCII string that uniquely identifies the name of the shader function.</span></span>

</dd> <dt>

<span data-ttu-id="27417-119"><span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*ArgumentList*</span><span class="sxs-lookup"><span data-stu-id="27417-119"><span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*ArgumentList*</span></span>
</dt> <dd>

<span data-ttu-id="27417-120">Liste d’arguments facultative, qui est une liste séparée par des virgules des [arguments](dx-graphics-hlsl-function-parameters.md) passés dans une fonction.</span><span class="sxs-lookup"><span data-stu-id="27417-120">Optional argument list, which is a comma-separated list of [arguments](dx-graphics-hlsl-function-parameters.md) passed into a function.</span></span>

</dd> <dt>

<span data-ttu-id="27417-121"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Équivalent*</span><span class="sxs-lookup"><span data-stu-id="27417-121"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantic*</span></span>
</dt> <dd>

<span data-ttu-id="27417-122">Chaîne facultative qui identifie l’utilisation prévue des données de retour (voir [sémantique (DirectX HLSL)](dx-graphics-hlsl-semantics.md)).</span><span class="sxs-lookup"><span data-stu-id="27417-122">Optional string that identifies the intended usage of the return data (see [Semantics (DirectX HLSL)](dx-graphics-hlsl-semantics.md)).</span></span>

</dd> <dt>

<span data-ttu-id="27417-123"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span><span class="sxs-lookup"><span data-stu-id="27417-123"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span></span>
</dt> <dd>

<span data-ttu-id="27417-124">[Instructions](dx-graphics-hlsl-statement-blocks.md) facultatives qui composent le corps de la fonction.</span><span class="sxs-lookup"><span data-stu-id="27417-124">Optional [statements](dx-graphics-hlsl-statement-blocks.md) that make up the body of the function.</span></span> <span data-ttu-id="27417-125">Une fonction définie sans corps est appelée un prototype de fonction. le corps d’une fonction prototype doit être défini ailleurs avant que la fonction puisse être appelée.</span><span class="sxs-lookup"><span data-stu-id="27417-125">A function defined without a body is called a function prototype; the body of a prototype function must be defined elsewhere before the function can be called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27417-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="27417-126">Return Value</span></span>

<span data-ttu-id="27417-127">Le type de retour peut être l’un de ces [types HLSL](dx-graphics-hlsl-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="27417-127">The return type can be any one of these [HLSL types](dx-graphics-hlsl-data-types.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="27417-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="27417-128">Remarks</span></span>

<span data-ttu-id="27417-129">La syntaxe de cette page décrit presque tous les types de fonctions HLSL, y compris les nuanceurs vertex, les nuanceurs de pixels et les fonctions d’assistance.</span><span class="sxs-lookup"><span data-stu-id="27417-129">The syntax on this page describes almost every type of HLSL function, this includes vertex shaders, pixel shaders, and helper functions.</span></span> <span data-ttu-id="27417-130">Bien qu’un nuanceur Geometry soit également implémenté avec une fonction, sa syntaxe est un peu plus compliquée. il existe donc une page distincte qui définit une déclaration de fonction de nuanceur Geometry (voir [Geometry-Shader Object (DirectX HLSL)](dx-graphics-hlsl-geometry-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="27417-130">While a geometry shader is also implemented with a function, its syntax is a little more complicated, so there is a separate page that defines a geometry shader function declaration (see [Geometry-Shader Object (DirectX HLSL)](dx-graphics-hlsl-geometry-shader.md)).</span></span>

<span data-ttu-id="27417-131">Une fonction peut être surchargée tant qu’elle reçoit une combinaison unique de types de paramètres et/ou l’ordre des paramètres.</span><span class="sxs-lookup"><span data-stu-id="27417-131">A function can be overloaded as long as it is given a unique combination of parameter types and/or parameter order.</span></span> <span data-ttu-id="27417-132">Le langage HLSL implémente également un certain nombre de fonctions intégrées ou [**intrinsèques**](dx-graphics-hlsl-intrinsic-functions.md).</span><span class="sxs-lookup"><span data-stu-id="27417-132">HLSL also implements a number of built in, or [**intrinsic functions**](dx-graphics-hlsl-intrinsic-functions.md).</span></span>

<span data-ttu-id="27417-133">Vous pouvez spécifier des plans de clips spécifiques à l’utilisateur avec l’attribut **clipplanes** .</span><span class="sxs-lookup"><span data-stu-id="27417-133">You can specify user-specific clip planes with the **clipplanes** attribute.</span></span> <span data-ttu-id="27417-134">Windows applique ces plans de séquences à toutes les primitives dessinées.</span><span class="sxs-lookup"><span data-stu-id="27417-134">Windows applies these clip planes to all of the primitives drawn.</span></span> <span data-ttu-id="27417-135">L’attribut **clipplanes** fonctionne comme [SV \_ ClipDistance](dx-graphics-hlsl-semantics.md) , mais fonctionne sur toutes les [fonctionnalités](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) matérielles 9 \_ x et supérieures.</span><span class="sxs-lookup"><span data-stu-id="27417-135">The **clipplanes** attribute works like [SV\_ClipDistance](dx-graphics-hlsl-semantics.md) but works on all hardware [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span> <span data-ttu-id="27417-136">Pour plus d’informations, consultez l' [image des plans d’utilisateur sur le matériel de niveau de fonctionnalité 9](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9).</span><span class="sxs-lookup"><span data-stu-id="27417-136">For more info, see [User clip planes on feature level 9 hardware](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9).</span></span>

## <a name="examples"></a><span data-ttu-id="27417-137">Exemples</span><span class="sxs-lookup"><span data-stu-id="27417-137">Examples</span></span>

<span data-ttu-id="27417-138">Cet exemple provient de BasicHLSL10. FX de l' [exemple BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="27417-138">This example is from BasicHLSL10.fx from the [BasicHLSL10 Sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).</span></span>


```hlsl
struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; 
    float4 Diffuse    : COLOR0;
    float2 TextureUV  : TEXCOORD0;
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
    VS_OUTPUT Output;
    ...
    return Output;    
}
```



<span data-ttu-id="27417-139">Cet exemple de AdvancedParticles. FX de l' [exemple AdvancedParticles](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx)illustre l’utilisation d’une sémantique pour le type de retour.</span><span class="sxs-lookup"><span data-stu-id="27417-139">This example from AdvancedParticles.fx from the [AdvancedParticles Sample](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx), illustrates using a semantic for the return type.</span></span>


```hlsl
//
// PS for particles
//
float4 PSPointSprite(PSSceneIn input) : SV_Target
{   
    return g_txDiffuse.Sample( g_samLinear, input.tex ) * input.color;
}
```



## <a name="related-topics"></a><span data-ttu-id="27417-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="27417-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27417-141">Fonctions (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="27417-141">Functions (DirectX HLSL)</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 

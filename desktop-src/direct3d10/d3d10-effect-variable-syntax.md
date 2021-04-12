---
description: Une variable Effect est déclarée avec la syntaxe suivante.
ms.assetid: 53939c65-3725-44cc-bec6-775c3b921770
title: Syntaxe de la variable Effect (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8068571ff393e83ba0ae11eb2f9cb62f0bbb49df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393100"
---
# <a name="effect-variable-syntax-direct3d-10"></a><span data-ttu-id="b0b80-103">Syntaxe de la variable Effect (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="b0b80-103">Effect Variable Syntax (Direct3D 10)</span></span>

<span data-ttu-id="b0b80-104">Une variable Effect est déclarée avec la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="b0b80-104">An effect variable is declared with the following syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0b80-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0b80-105">Syntax</span></span>

<span data-ttu-id="b0b80-106">*Type de données* *VariableName* \[ :  \]  <  *Annotations* SemanticName > ;</span><span class="sxs-lookup"><span data-stu-id="b0b80-106">*DataType* *VariableName* \[ : *SemanticName* \] < *Annotations* >;</span></span>



| <span data-ttu-id="b0b80-107">Nom</span><span class="sxs-lookup"><span data-stu-id="b0b80-107">Name</span></span>         | <span data-ttu-id="b0b80-108">Description</span><span class="sxs-lookup"><span data-stu-id="b0b80-108">Description</span></span>                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0b80-109">DataType</span><span class="sxs-lookup"><span data-stu-id="b0b80-109">DataType</span></span>     | <span data-ttu-id="b0b80-110">N’importe quel type de [base](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md) ou de [texture](../direct3dhlsl/dx-graphics-hlsl-to-type.md) .</span><span class="sxs-lookup"><span data-stu-id="b0b80-110">Any [basic](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md) or [texture](../direct3dhlsl/dx-graphics-hlsl-to-type.md) type.</span></span>                                                                        |
| <span data-ttu-id="b0b80-111">VariableName</span><span class="sxs-lookup"><span data-stu-id="b0b80-111">VariableName</span></span> | <span data-ttu-id="b0b80-112">Chaîne ASCII qui identifie de façon unique le nom de la variable d’effet.</span><span class="sxs-lookup"><span data-stu-id="b0b80-112">An ASCII string that uniquely identifies the name of the effect variable.</span></span>                                                                                                                   |
| <span data-ttu-id="b0b80-113">SemanticName</span><span class="sxs-lookup"><span data-stu-id="b0b80-113">SemanticName</span></span> | <span data-ttu-id="b0b80-114">Chaîne ASCII qui indique des informations supplémentaires sur la façon dont une variable doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="b0b80-114">A ASCII string that denotes additional information about how a variable should be used.</span></span> <span data-ttu-id="b0b80-115">Une sémantique est une chaîne ASCII qui peut être une valeur système prédéfinie ou une chaîne personnalisée de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b0b80-115">A semantic is an ASCII string that can be either a predefined system-value or a custom-user string.</span></span> |
| <span data-ttu-id="b0b80-116">Annotations</span><span class="sxs-lookup"><span data-stu-id="b0b80-116">Annotations</span></span>  | <span data-ttu-id="b0b80-117">Un ou plusieurs éléments d’informations fournies par l’utilisateur (métadonnées) qui sont ignorés par le système d’effet.</span><span class="sxs-lookup"><span data-stu-id="b0b80-117">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="b0b80-118">Pour obtenir la syntaxe, consultez [syntaxe d’annotation (Direct3D 10)](d3d10-effect-annotation-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="b0b80-118">For syntax, see [Annotation Syntax (Direct3D 10)](d3d10-effect-annotation-syntax.md).</span></span>     |



 

<span data-ttu-id="b0b80-119">Une variable Effect déclarée en dehors de toutes les fonctions est considérée comme globale dans la portée. les variables déclarées dans une fonction sont locales à cette fonction.</span><span class="sxs-lookup"><span data-stu-id="b0b80-119">An effect variable that is declared outside of all functions, is considered global in scope; variables declared within a function are local to that function.</span></span>

## <a name="example"></a><span data-ttu-id="b0b80-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="b0b80-120">Example</span></span>

<span data-ttu-id="b0b80-121">L' [exemple BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) utilise des variables globales sans sémantique pour les couleurs matérielles, les propriétés de lumière et les matrices de transformation.</span><span class="sxs-lookup"><span data-stu-id="b0b80-121">The [BasicHLSL10 sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) uses global variables without semantics for material colors, light properties and transformation matrices.</span></span>

<span data-ttu-id="b0b80-122">Cet exemple illustre des variables d’effet global.</span><span class="sxs-lookup"><span data-stu-id="b0b80-122">This example illustrates global effect variables.</span></span>


```
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
float3 g_LightDir[3];               // Light's direction in world space
float4x4 g_mWorld;                  // World matrix for object
```



<span data-ttu-id="b0b80-123">Cet exemple illustre des variables d’effet qui sont locales à une fonction de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="b0b80-123">This example illustrates effect variables that are local to a shader function.</span></span>


```
VS_OUTPUT RenderSceneVS( ... )
{
    float3 vNormalWorldSpace;
    float4 vAnimatedPos;

    // shader body
}
```



<span data-ttu-id="b0b80-124">Cet exemple illustre les paramètres de fonction qui ont une sémantique.</span><span class="sxs-lookup"><span data-stu-id="b0b80-124">This example illustrates function parameters that have semantics.</span></span>


```
VS_OUTPUT RenderSceneVS( float4 vPos : SV_POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
  ...
}
```



<span data-ttu-id="b0b80-125">Cet exemple illustre la déclaration d’une variable de texture.</span><span class="sxs-lookup"><span data-stu-id="b0b80-125">This example illustrates declaring a texture variable.</span></span>


```
Texture2D g_MeshTexture;            // Color texture for mesh
```



<span data-ttu-id="b0b80-126">L’échantillonnage d’une texture s’effectue à l’aide d’un échantillon de texture.</span><span class="sxs-lookup"><span data-stu-id="b0b80-126">Sampling a texture is done with a texture sampler.</span></span> <span data-ttu-id="b0b80-127">Pour configurer un échantillonneur dans un effet, consultez le [type d’échantillonneur](../direct3dhlsl/dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="b0b80-127">To set up a sampler in an effect, see the [sampler type](../direct3dhlsl/dx-graphics-hlsl-sampler.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0b80-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b0b80-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0b80-129">Format d’effet</span><span class="sxs-lookup"><span data-stu-id="b0b80-129">Effect Format</span></span>](d3d10-effect-format.md)
</dt> </dl>

 

 

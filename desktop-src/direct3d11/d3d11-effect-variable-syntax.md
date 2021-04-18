---
title: Syntaxe de la variable Effect (Direct3D 11)
description: Une variable Effect est déclarée avec la syntaxe décrite dans cette section.
ms.assetid: c0cfc9dd-2df3-4f38-a0e4-2e494456b3c9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67710642060ffea642434ba2d23a77cec2fb8bc3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463178"
---
# <a name="effect-variable-syntax-direct3d-11"></a><span data-ttu-id="572c3-103">Syntaxe de la variable Effect (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="572c3-103">Effect Variable Syntax (Direct3D 11)</span></span>

<span data-ttu-id="572c3-104">Une variable Effect est déclarée avec la syntaxe décrite dans cette section.</span><span class="sxs-lookup"><span data-stu-id="572c3-104">An effect variable is declared with the syntax described in this section.</span></span>

## <a name="syntax"></a><span data-ttu-id="572c3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="572c3-105">Syntax</span></span>

<span data-ttu-id="572c3-106">Syntaxe de base :</span><span class="sxs-lookup"><span data-stu-id="572c3-106">Basic syntax:</span></span>

<span data-ttu-id="572c3-107">*Type de données* *VariableName* \[ *:* \]  <  *Annotations* SemanticName  >  \[ = InitialValue \] ;</span><span class="sxs-lookup"><span data-stu-id="572c3-107">*DataType* *VariableName* \[ *: SemanticName* \] < *Annotations* > \[ = InitialValue \];</span></span>

<span data-ttu-id="572c3-108">Pour connaître la syntaxe complète [, consultez Syntaxe de variable (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax) .</span><span class="sxs-lookup"><span data-stu-id="572c3-108">See [Variable Syntax (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax) for full syntax.</span></span>



| <span data-ttu-id="572c3-109">Nom</span><span class="sxs-lookup"><span data-stu-id="572c3-109">Name</span></span>         | <span data-ttu-id="572c3-110">Description</span><span class="sxs-lookup"><span data-stu-id="572c3-110">Description</span></span>                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="572c3-111">DataType</span><span class="sxs-lookup"><span data-stu-id="572c3-111">DataType</span></span>     | <span data-ttu-id="572c3-112">Tout type d’accès de [base](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax), de [texture](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-type), non ordonné, de nuanceur ou de bloc d’État.</span><span class="sxs-lookup"><span data-stu-id="572c3-112">Any [basic](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax), [texture](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-type), unordered access view, shader or state block type.</span></span>                            |
| <span data-ttu-id="572c3-113">VariableName</span><span class="sxs-lookup"><span data-stu-id="572c3-113">VariableName</span></span> | <span data-ttu-id="572c3-114">Chaîne ASCII qui identifie de façon unique le nom de la variable d’effet.</span><span class="sxs-lookup"><span data-stu-id="572c3-114">An ASCII string that uniquely identifies the name of the effect variable.</span></span>                                                                                                                   |
| <span data-ttu-id="572c3-115">SemanticName</span><span class="sxs-lookup"><span data-stu-id="572c3-115">SemanticName</span></span> | <span data-ttu-id="572c3-116">Chaîne ASCII qui indique des informations supplémentaires sur la façon dont une variable doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="572c3-116">A ASCII string that denotes additional information about how a variable should be used.</span></span> <span data-ttu-id="572c3-117">Une sémantique est une chaîne ASCII qui peut être une valeur système prédéfinie ou une chaîne personnalisée de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="572c3-117">A semantic is an ASCII string that can be either a predefined system-value or a custom-user string.</span></span> |
| <span data-ttu-id="572c3-118">Annotations</span><span class="sxs-lookup"><span data-stu-id="572c3-118">Annotations</span></span>  | <span data-ttu-id="572c3-119">Un ou plusieurs éléments d’informations fournies par l’utilisateur (métadonnées) qui sont ignorés par le système d’effet.</span><span class="sxs-lookup"><span data-stu-id="572c3-119">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="572c3-120">Pour obtenir la syntaxe, consultez [syntaxe d’annotation (Direct3D 11)](d3d11-effect-annotation-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="572c3-120">For syntax, see [Annotation Syntax (Direct3D 11)](d3d11-effect-annotation-syntax.md).</span></span>     |
| <span data-ttu-id="572c3-121">InitialValue</span><span class="sxs-lookup"><span data-stu-id="572c3-121">InitialValue</span></span> | <span data-ttu-id="572c3-122">Valeur par défaut de la variable.</span><span class="sxs-lookup"><span data-stu-id="572c3-122">The default value of the variable.</span></span>                                                                                                                                                          |



 

<span data-ttu-id="572c3-123">Une variable Effect déclarée en dehors de toutes les fonctions est considérée comme globale dans la portée. les variables déclarées dans une fonction sont locales à cette fonction.</span><span class="sxs-lookup"><span data-stu-id="572c3-123">An effect variable that is declared outside of all functions, is considered global in scope; variables declared within a function are local to that function.</span></span>

## <a name="example"></a><span data-ttu-id="572c3-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="572c3-124">Example</span></span>

<span data-ttu-id="572c3-125">Cet exemple illustre les variables numériques à effet global.</span><span class="sxs-lookup"><span data-stu-id="572c3-125">This example illustrates global effect numeric variables.</span></span>


```
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
float3 g_LightDir[3];               // Light's direction in world space
float4x4 g_mWorld;                  // World matrix for object
```



<span data-ttu-id="572c3-126">Cet exemple illustre des variables d’effet qui sont locales à une fonction de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="572c3-126">This example illustrates effect variables that are local to a shader function.</span></span>


```
VS_OUTPUT RenderSceneVS( ... )
{
    float3 vNormalWorldSpace;
    float4 vAnimatedPos;

    // shader body
}
```



<span data-ttu-id="572c3-127">Cet exemple illustre les paramètres de fonction qui ont une sémantique.</span><span class="sxs-lookup"><span data-stu-id="572c3-127">This example illustrates function parameters that have semantics.</span></span>


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



<span data-ttu-id="572c3-128">Cet exemple illustre la déclaration d’une variable de texture globale.</span><span class="sxs-lookup"><span data-stu-id="572c3-128">This example illustrates declaring a global texture variable.</span></span>


```
Texture2D g_MeshTexture;            // Color texture for mesh
```



<span data-ttu-id="572c3-129">L’échantillonnage d’une texture s’effectue à l’aide d’un échantillon de texture.</span><span class="sxs-lookup"><span data-stu-id="572c3-129">Sampling a texture is done with a texture sampler.</span></span> <span data-ttu-id="572c3-130">Pour configurer un échantillonneur dans un effet, consultez le [type d’échantillonneur](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).</span><span class="sxs-lookup"><span data-stu-id="572c3-130">To set up a sampler in an effect, see the [sampler type](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).</span></span>

<span data-ttu-id="572c3-131">Cet exemple illustre la déclaration de variables de vue d’accès non ordonnées globales.</span><span class="sxs-lookup"><span data-stu-id="572c3-131">This example illustrates declaring global unordered access view variables.</span></span>


```
RWStructuredBuffer<uint> bc : register(u2) < string name="bc"; >;
RWBuffer<uint> bRW;
struct S
{
   uint key;
   uint value;
};
AppendStructuredBuffer<S> asb : register(u5);
RWByteAddressBuffer rwbab : register(u1);
RWStructuredBuffer<uint> rwsb : register(u3);
RWTexture1D<float> rwt1d : register(u1);
RWTexture1DArray<uint> rwt1da : register(u4);
RWTexture2D<uint> rwt2d : register(u2);
RWTexture2DArray<uint> rwt2da : register(u6);
RWTexture3D<uint> rwt3d : register(u7); 
 This example illustrates declaring global shader variables.
VertexShader pVS = CompileShader( vs_5_0, VS() );
HullShader pHS = NULL;
DomainShader pDS = NULL;
GeometryShader pGS = ConstructGSWithSO( CompileShader( gs_5_0, VS() ), 
                                        "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                        "3:Texcoord.xyzw; 3:$SKIP.x;", 
                                        NULL, 
                                        NULL, 
                                        1 );
PixelShader pPS = NULL;
ComputeShader pCS = NULL;
This example illustrates declaring global state block variables.
BlendState myBS[2] < bool IsValid = true; >
{
  {
    BlendEnable[0] = false;
  },
  {
    BlendEnable[0] = true;
    SrcBlendAlpha[0] = Inv_Src_Alpha;
  }
};

RasterizerState myRS
{
      FillMode = Solid;
      CullMode = NONE;
      MultisampleEnable = true;
      DepthClipEnable = false;
};

DepthStencilState myDS
{
    DepthEnable = false;
    DepthWriteMask = Zero;
    DepthFunc = Less;
};
sampler mySS[2] : register(s3) 
{
    {
        Filter = ANISOTROPIC;
        MaxAnisotropy = 3;
    },
    {
        Filter = ANISOTROPIC;
        MaxAnisotropy = 4;
    }
};
  
  
```



## <a name="related-topics"></a><span data-ttu-id="572c3-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="572c3-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="572c3-133">Format d’effet</span><span class="sxs-lookup"><span data-stu-id="572c3-133">Effect Format</span></span>](d3d11-effect-format.md)
</dt> </dl>

 

 
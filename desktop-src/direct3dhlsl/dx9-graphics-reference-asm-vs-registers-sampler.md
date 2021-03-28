---
title: Échantillonneur (Direct3D 9 ASM-vs)
description: Un échantillonneur est un Pseudo-registre d’entrée pour un nuanceur de sommets, qui est utilisé pour identifier la phase d’échantillonnage. Il existe quatre échantillonneurs de nuanceur de sommets S0 à S3. Quatre surfaces de texture peuvent être lues dans une seule passe de nuanceur.
ms.assetid: a4588ced-24e2-4d4e-93e4-35a985bafaa4
keywords:
- Échantillonneur, type (Direct3D 9 ASM-vs)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 685f261da9d56dc29c0632d01cabbf29cd13a00f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382743"
---
# <a name="sampler-direct3d-9-asm-vs"></a><span data-ttu-id="262e2-106">Échantillonneur (Direct3D 9 ASM-vs)</span><span class="sxs-lookup"><span data-stu-id="262e2-106">Sampler (Direct3D 9 asm-vs)</span></span>

<span data-ttu-id="262e2-107">Un échantillonneur est un Pseudo-registre d’entrée pour un nuanceur de sommets, qui est utilisé pour identifier la phase d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="262e2-107">A sampler is a input pseudo-register for a vertex shader, which is used to identify the sampling stage.</span></span> <span data-ttu-id="262e2-108">Il existe quatre échantillonneurs de nuanceur vertex : S0 à S3.</span><span class="sxs-lookup"><span data-stu-id="262e2-108">There are four vertex shader samplers: s0 to s3.</span></span> <span data-ttu-id="262e2-109">Quatre surfaces de texture peuvent être lues dans une seule passe de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="262e2-109">Four texture surfaces can be read in a single shader pass.</span></span>

<span data-ttu-id="262e2-110">L’échantillonneur (Direct3D 9 ASM-vs) est un Pseudo-Registre, car vous ne pouvez pas y lire ou écrire directement.</span><span class="sxs-lookup"><span data-stu-id="262e2-110">Sampler (Direct3D 9 asm-vs)s are pseudo registers because you cannot directly read or write to them.</span></span>

<span data-ttu-id="262e2-111">Une unité d’échantillonnage correspond à la phase d’échantillonnage de texture, en encapsulant l’état spécifique à l’échantillonnage fourni par [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span><span class="sxs-lookup"><span data-stu-id="262e2-111">A sampling unit corresponds to the texture sampling stage, encapsulating the sampling-specific state provided by [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span></span> <span data-ttu-id="262e2-112">Chaque échantillonneur identifie de façon unique une surface de texture unique, qui est définie sur l’échantillonneur correspondant à l’aide de [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span><span class="sxs-lookup"><span data-stu-id="262e2-112">Each sampler uniquely identifies a single texture surface, which is set to the corresponding sampler using the [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span></span> <span data-ttu-id="262e2-113">Toutefois, la même surface de texture peut être définie sur plusieurs échantillonneurs.</span><span class="sxs-lookup"><span data-stu-id="262e2-113">However, the same texture surface can be set at multiple samplers.</span></span>

<span data-ttu-id="262e2-114">Au moment du tracé, une texture ne peut pas être définie simultanément comme une cible de rendu et une texture à une étape.</span><span class="sxs-lookup"><span data-stu-id="262e2-114">At draw time, a texture cannot be simultaneously set as a render target and a texture at a stage.</span></span>

<span data-ttu-id="262e2-115">Étant donné qu’il y a quatre échantillonneurs, jusqu’à quatre surfaces de texture peuvent être lues à partir d’une seule passe de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="262e2-115">Because there are four samplers, up to four texture surfaces can be read from in a single shader pass.</span></span> <span data-ttu-id="262e2-116">Un échantillonneur peut apparaître comme le seul argument dans l’instruction de chargement de texture : [texldl-vs](texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="262e2-116">A sampler might appear as the only argument in the texture load instruction: [texldl - vs](texldl---vs.md).</span></span>

<span data-ttu-id="262e2-117">Dans vs \_ 3 \_ 0, si un échantillonneur est utilisé, il doit être déclaré au début du programme du nuanceur à l’aide de l’instruction [DCL \_ samplerType (SM3-vs ASM)](dcl-samplertype---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="262e2-117">In vs\_3\_0, if a sampler is used, it needs to be declared at the beginning of the shader program using the [dcl\_samplerType (sm3 - vs asm)](dcl-samplertype---vs.md) instruction.</span></span>



| <span data-ttu-id="262e2-118">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="262e2-118">Vertex shader versions</span></span> | <span data-ttu-id="262e2-119">1\_1</span><span class="sxs-lookup"><span data-stu-id="262e2-119">1\_1</span></span> | <span data-ttu-id="262e2-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="262e2-120">2\_0</span></span> | <span data-ttu-id="262e2-121">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="262e2-121">2\_sw</span></span> | <span data-ttu-id="262e2-122">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="262e2-122">2\_x</span></span> | <span data-ttu-id="262e2-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="262e2-123">3\_0</span></span> | <span data-ttu-id="262e2-124">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="262e2-124">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="262e2-125">Échantillonneur</span><span class="sxs-lookup"><span data-stu-id="262e2-125">Sampler</span></span>                |      |      |       |      | <span data-ttu-id="262e2-126">x</span><span class="sxs-lookup"><span data-stu-id="262e2-126">x</span></span>    | <span data-ttu-id="262e2-127">x</span><span class="sxs-lookup"><span data-stu-id="262e2-127">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="262e2-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="262e2-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="262e2-129">Registres de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="262e2-129">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> <dt>

[<span data-ttu-id="262e2-130">Textures de vertex dans vs \_ 3 \_ 0 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="262e2-130">Vertex Textures in vs\_3\_0 (DirectX HLSL)</span></span>](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0)
</dt> </dl>

 

 
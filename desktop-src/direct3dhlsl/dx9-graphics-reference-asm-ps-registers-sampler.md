---
title: Échantillonneur (Direct3D 9 ASM-PS)
description: Un échantillonneur est un Pseudo-registre d’entrée pour un nuanceur de pixels, qui est utilisé pour identifier la phase d’échantillonnage.
ms.assetid: 37cc28ae-fbd0-4f81-9e8e-f9609980d84e
keywords:
- Échantillonneur, type (Direct3D 9 ASM-PS)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77875eed0827ad6bcb6d89111b13b6a31232dd86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031418"
---
# <a name="sampler-direct3d-9-asm-ps"></a><span data-ttu-id="803f3-104">Échantillonneur (Direct3D 9 ASM-PS)</span><span class="sxs-lookup"><span data-stu-id="803f3-104">Sampler (Direct3D 9 asm-ps)</span></span>

<span data-ttu-id="803f3-105">Un échantillonneur est un Pseudo-registre d’entrée pour un nuanceur de pixels, qui est utilisé pour identifier la phase d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="803f3-105">A sampler is a input pseudo-register for a pixel shader, which is used to identify the sampling stage.</span></span> <span data-ttu-id="803f3-106">Il y a 16 registres de l’étape d’échantillonnage du nuanceur de pixels : S0 à S15.</span><span class="sxs-lookup"><span data-stu-id="803f3-106">There are 16 pixel shader sampling stage registers: s0 to s15.</span></span> <span data-ttu-id="803f3-107">Par conséquent, jusqu’à 16 surfaces de texture peuvent être lues dans une seule passe de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="803f3-107">Therefore, up to 16 texture surfaces can be read in a single shader pass.</span></span> <span data-ttu-id="803f3-108">Les instructions qui utilisent un registre d’échantillonnage sont texld et texldp.</span><span class="sxs-lookup"><span data-stu-id="803f3-108">The instructions that use a sampler register are texld and texldp.</span></span>

<span data-ttu-id="803f3-109">L’échantillonneur doit être déclaré avant d’être utilisé avec l’instruction [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="803f3-109">Sampler must be declared before use with the [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md) instruction.</span></span>



| <span data-ttu-id="803f3-110">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="803f3-110">Pixel shader versions</span></span> | <span data-ttu-id="803f3-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="803f3-111">1\_1</span></span> | <span data-ttu-id="803f3-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="803f3-112">1\_2</span></span> | <span data-ttu-id="803f3-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="803f3-113">1\_3</span></span> | <span data-ttu-id="803f3-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="803f3-114">1\_4</span></span> | <span data-ttu-id="803f3-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="803f3-115">2\_0</span></span> | <span data-ttu-id="803f3-116">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="803f3-116">2\_sw</span></span> | <span data-ttu-id="803f3-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="803f3-117">2\_x</span></span> | <span data-ttu-id="803f3-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="803f3-118">3\_0</span></span> | <span data-ttu-id="803f3-119">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="803f3-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="803f3-120">Échantillonneur</span><span class="sxs-lookup"><span data-stu-id="803f3-120">Sampler</span></span>               |      |      |      |      | <span data-ttu-id="803f3-121">x</span><span class="sxs-lookup"><span data-stu-id="803f3-121">x</span></span>    | <span data-ttu-id="803f3-122">x</span><span class="sxs-lookup"><span data-stu-id="803f3-122">x</span></span>     | <span data-ttu-id="803f3-123">x</span><span class="sxs-lookup"><span data-stu-id="803f3-123">x</span></span>    | <span data-ttu-id="803f3-124">x</span><span class="sxs-lookup"><span data-stu-id="803f3-124">x</span></span>    | <span data-ttu-id="803f3-125">x</span><span class="sxs-lookup"><span data-stu-id="803f3-125">x</span></span>     |



 

<span data-ttu-id="803f3-126">Les échantillonneurs sont des Pseudo-registres, car vous ne pouvez pas les lire ou les écrire directement.</span><span class="sxs-lookup"><span data-stu-id="803f3-126">Samplers are pseudo registers because you cannot directly read or write to them.</span></span>

<span data-ttu-id="803f3-127">Une unité d’échantillonnage correspond à la phase d’échantillonnage de texture, en encapsulant l’état spécifique à l’échantillonnage fourni par [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span><span class="sxs-lookup"><span data-stu-id="803f3-127">A sampling unit corresponds to the texture sampling stage, encapsulating the sampling-specific state provided by [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span></span> <span data-ttu-id="803f3-128">Chaque échantillonneur identifie de façon unique une surface de texture unique, qui est définie sur l’échantillonneur correspondant à l’aide de [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span><span class="sxs-lookup"><span data-stu-id="803f3-128">Each sampler uniquely identifies a single texture surface, which is set to the corresponding sampler using the [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span></span> <span data-ttu-id="803f3-129">Toutefois, la même surface de texture peut être définie sur plusieurs échantillonneurs.</span><span class="sxs-lookup"><span data-stu-id="803f3-129">However, the same texture surface can be set at multiple samplers.</span></span>

<span data-ttu-id="803f3-130">Au moment du tracé, une texture ne peut pas être définie simultanément comme une cible de rendu et une texture à une étape.</span><span class="sxs-lookup"><span data-stu-id="803f3-130">At draw time, a texture cannot be simultaneously set as a render target and a texture at a stage.</span></span>

<span data-ttu-id="803f3-131">Un échantillonneur peut apparaître comme le seul argument dans l’instruction de chargement de texture : [texldl-PS](texldl---ps.md).</span><span class="sxs-lookup"><span data-stu-id="803f3-131">A sampler might appear as the only argument in the texture load instruction: [texldl - ps](texldl---ps.md).</span></span>

<span data-ttu-id="803f3-132">Dans PS \_ 3 \_ 0, si un échantillonneur est utilisé, il doit être déclaré au début du programme du nuanceur à l’aide de l’instruction [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="803f3-132">In ps\_3\_0, if a sampler is used, it needs to be declared at the beginning of the shader program using the [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md) instruction.</span></span>

<span data-ttu-id="803f3-133">L’échantillonnage d’une texture avec une dimension supérieure à celle présente dans les coordonnées de texture n’est pas conforme.</span><span class="sxs-lookup"><span data-stu-id="803f3-133">Sampling a texture with a higher dimension than is present in the texture coordinates is illegal.</span></span> <span data-ttu-id="803f3-134">L’échantillonnage d’une texture avec une dimension inférieure à celle qui est présente dans les coordonnées de texture ignore les coordonnées de texture supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="803f3-134">Sampling a texture with a lower dimension than is present in the texture coordinates will ignore the extra texture coordinates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="803f3-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="803f3-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="803f3-136">Inscrit</span><span class="sxs-lookup"><span data-stu-id="803f3-136">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 
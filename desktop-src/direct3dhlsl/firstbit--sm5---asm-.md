---
title: firstbit (SM5-ASM)
description: Recherche le premier bit défini dans un nombre, soit à partir de LSB, soit à l’octet MSB.
ms.assetid: E3066676-5218-470A-944A-7B221E1BF64D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b88fa9291ce64fcc8c94510bd09bed31e7b7f96
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313747"
---
# <a name="firstbit-sm5---asm"></a><span data-ttu-id="95489-103">firstbit (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="95489-103">firstbit (sm5 - asm)</span></span>

<span data-ttu-id="95489-104">Recherche le premier bit défini dans un nombre, soit à partir de LSB, soit à l’octet MSB.</span><span class="sxs-lookup"><span data-stu-id="95489-104">Finds the first bit set in a number, either from LSB or MSB.</span></span>



| <span data-ttu-id="95489-105">firstbit { \_ Hi </span><span class="sxs-lookup"><span data-stu-id="95489-105">firstbit{\_hi</span></span>\|<span data-ttu-id="95489-106">\_Lo</span><span class="sxs-lookup"><span data-stu-id="95489-106">\_lo\</span></span>|<span data-ttu-id="95489-107">\_Chi} dest \[ . Mask \] , src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="95489-107">\_shi} dest\[.mask\], src0\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="95489-108">Élément</span><span class="sxs-lookup"><span data-stu-id="95489-108">Item</span></span>                                                            | <span data-ttu-id="95489-109">Description</span><span class="sxs-lookup"><span data-stu-id="95489-109">Description</span></span>                                                                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95489-110"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="95489-110"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="95489-111">\[dans \] la position entière du premier bit défini dans *src0* à partir de LSB pour FIRSTBIT \_ Lo ou MSB pour firstbit \_ Hi.</span><span class="sxs-lookup"><span data-stu-id="95489-111">\[in\] The integer position of the first bit set in *src0* starting from the LSB for firstbit\_lo or MSB for firstbit\_hi.</span></span><br/> |
| <span data-ttu-id="95489-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="95489-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="95489-113">\[dans \] l’entier d’entrée.</span><span class="sxs-lookup"><span data-stu-id="95489-113">\[in\] The input integer.</span></span><br/>                                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="95489-114">Notes</span><span class="sxs-lookup"><span data-stu-id="95489-114">Remarks</span></span>

<span data-ttu-id="95489-115">Cette opération retourne la position entière du premier bit défini dans l’entrée 32 bits à partir de LSB pour firstbit \_ Lo ou MSB pour firstbit \_ Hi.</span><span class="sxs-lookup"><span data-stu-id="95489-115">This operation returns the integer position of the first bit set in the 32-bit input starting from the LSB for firstbit\_lo or MSB for firstbit\_hi.</span></span> <span data-ttu-id="95489-116">Par exemple \_ , firstbit Lo sur 0x00000001 retourne 0.</span><span class="sxs-lookup"><span data-stu-id="95489-116">For example firstbit\_lo on 0x00000001 returns 0.</span></span> <span data-ttu-id="95489-117">firstbit \_ Hi sur 0x10000000 retourne 3.</span><span class="sxs-lookup"><span data-stu-id="95489-117">firstbit\_hi on 0x10000000 returns 3.</span></span>

<span data-ttu-id="95489-118">firstbit \_ Chi (s pour signed) retourne le premier 0 de l’MSB si le nombre est négatif ; sinon, il retourne les 1 premiers du MSB.</span><span class="sxs-lookup"><span data-stu-id="95489-118">firstbit\_shi (s for signed) returns the first 0 from the MSB if the number is negative; otherwise it returns the first 1 from the MSB.</span></span>

<span data-ttu-id="95489-119">Toutes les variantes de l’instruction retournent ~ 0 (0xFFFFFFFF dans le registre 32 bits) si aucune correspondance n’est trouvée.</span><span class="sxs-lookup"><span data-stu-id="95489-119">All variants of the instruction return ~0 (0xffffffff in 32-bit register) if no match is found.</span></span>

<span data-ttu-id="95489-120">Utilisez cette instruction pour énumérer rapidement les bits Set dans un champ de bits ou pour trouver la puissance la plus grande de 2 dans un nombre.</span><span class="sxs-lookup"><span data-stu-id="95489-120">Use this instruction to quickly enumerate set bits in a bitfield, or find the largest power of 2 in a number.</span></span>

<span data-ttu-id="95489-121">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="95489-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="95489-122">Sommet</span><span class="sxs-lookup"><span data-stu-id="95489-122">Vertex</span></span> | <span data-ttu-id="95489-123">Forme</span><span class="sxs-lookup"><span data-stu-id="95489-123">Hull</span></span> | <span data-ttu-id="95489-124">Domain</span><span class="sxs-lookup"><span data-stu-id="95489-124">Domain</span></span> | <span data-ttu-id="95489-125">Géométrie</span><span class="sxs-lookup"><span data-stu-id="95489-125">Geometry</span></span> | <span data-ttu-id="95489-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="95489-126">Pixel</span></span> | <span data-ttu-id="95489-127">Compute</span><span class="sxs-lookup"><span data-stu-id="95489-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="95489-128">X</span><span class="sxs-lookup"><span data-stu-id="95489-128">X</span></span>      | <span data-ttu-id="95489-129">X</span><span class="sxs-lookup"><span data-stu-id="95489-129">X</span></span>    | <span data-ttu-id="95489-130">X</span><span class="sxs-lookup"><span data-stu-id="95489-130">X</span></span>      | <span data-ttu-id="95489-131">X</span><span class="sxs-lookup"><span data-stu-id="95489-131">X</span></span>        | <span data-ttu-id="95489-132">X</span><span class="sxs-lookup"><span data-stu-id="95489-132">X</span></span>     | <span data-ttu-id="95489-133">X</span><span class="sxs-lookup"><span data-stu-id="95489-133">X</span></span>       |



 

## <a name="mimimum-shader-model"></a><span data-ttu-id="95489-134">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="95489-134">Mimimum Shader Model</span></span>

<span data-ttu-id="95489-135">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="95489-135">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="95489-136">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="95489-136">Shader Model</span></span>                                              | <span data-ttu-id="95489-137">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="95489-137">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="95489-138">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="95489-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="95489-139">Oui</span><span class="sxs-lookup"><span data-stu-id="95489-139">yes</span></span>       |
| [<span data-ttu-id="95489-140">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="95489-140">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="95489-141">non</span><span class="sxs-lookup"><span data-stu-id="95489-141">no</span></span>        |
| [<span data-ttu-id="95489-142">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="95489-142">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="95489-143">non</span><span class="sxs-lookup"><span data-stu-id="95489-143">no</span></span>        |
| [<span data-ttu-id="95489-144">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="95489-144">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="95489-145">non</span><span class="sxs-lookup"><span data-stu-id="95489-145">no</span></span>        |
| [<span data-ttu-id="95489-146">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="95489-146">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="95489-147">non</span><span class="sxs-lookup"><span data-stu-id="95489-147">no</span></span>        |
| [<span data-ttu-id="95489-148">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="95489-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="95489-149">non</span><span class="sxs-lookup"><span data-stu-id="95489-149">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="95489-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="95489-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95489-151">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="95489-151">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 






---
title: texldd-PS
description: Échantillonne une texture avec d’autres entrées de dégradé.
ms.assetid: 6d6b3180-d82e-4be4-929b-e5a6431bec38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 72f3c4aaf9ac7e6beaad1343c024aa28bd2a85ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104381982"
---
# <a name="texldd---ps"></a><span data-ttu-id="31cc3-103">texldd-PS</span><span class="sxs-lookup"><span data-stu-id="31cc3-103">texldd - ps</span></span>

<span data-ttu-id="31cc3-104">Échantillonne une texture avec d’autres entrées de dégradé.</span><span class="sxs-lookup"><span data-stu-id="31cc3-104">Samples a texture with additional gradient inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="31cc3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31cc3-105">Syntax</span></span>



| <span data-ttu-id="31cc3-106">texldd, DST, src0, src1, src2, src3</span><span class="sxs-lookup"><span data-stu-id="31cc3-106">texldd, dst, src0, src1, src2, src3</span></span> |
|-------------------------------------|



 

<span data-ttu-id="31cc3-107">Où :</span><span class="sxs-lookup"><span data-stu-id="31cc3-107">Where:</span></span>

-   <span data-ttu-id="31cc3-108">l’heure d’été est un registre de destination.</span><span class="sxs-lookup"><span data-stu-id="31cc3-108">dst is a destination register.</span></span>
-   <span data-ttu-id="31cc3-109">src0 est un registre source qui fournit les coordonnées de texture pour l’échantillon de texture.</span><span class="sxs-lookup"><span data-stu-id="31cc3-109">src0 is a source register that provides the texture coordinates for the texture sample.</span></span> <span data-ttu-id="31cc3-110">Consultez [Registre de coordonnées de texture](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span><span class="sxs-lookup"><span data-stu-id="31cc3-110">See [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span></span>
-   <span data-ttu-id="31cc3-111">src1 identifie le ou les registres de l’échantillonneur \# de source, où \# spécifie le numéro d’échantillonnage de texture à échantillonner.</span><span class="sxs-lookup"><span data-stu-id="31cc3-111">src1 identifies the source sampler register (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="31cc3-112">L’échantillonneur s’est associé à une texture et à un état de contrôle défini par l’énumération [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) (par exemple,</span><span class="sxs-lookup"><span data-stu-id="31cc3-112">The sampler has associated with it a texture and a control state defined by the [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) enumeration (ex.</span></span> <span data-ttu-id="31cc3-113">D3DSAMP \_ MINFILTER).</span><span class="sxs-lookup"><span data-stu-id="31cc3-113">D3DSAMP\_MINFILTER).</span></span>
-   <span data-ttu-id="31cc3-114">src2 est un registre de source d’entrée qui spécifie le dégradé x.</span><span class="sxs-lookup"><span data-stu-id="31cc3-114">src2 is an input source register that specifies the x gradient.</span></span>
-   <span data-ttu-id="31cc3-115">src3 est un registre de source d’entrée qui spécifie le dégradé y.</span><span class="sxs-lookup"><span data-stu-id="31cc3-115">src3 is an input source register that specifies the y gradient.</span></span>

## <a name="remarks"></a><span data-ttu-id="31cc3-116">Notes</span><span class="sxs-lookup"><span data-stu-id="31cc3-116">Remarks</span></span>



| <span data-ttu-id="31cc3-117">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="31cc3-117">Pixel shader versions</span></span> | <span data-ttu-id="31cc3-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="31cc3-118">1\_1</span></span> | <span data-ttu-id="31cc3-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="31cc3-119">1\_2</span></span> | <span data-ttu-id="31cc3-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="31cc3-120">1\_3</span></span> | <span data-ttu-id="31cc3-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="31cc3-121">1\_4</span></span> | <span data-ttu-id="31cc3-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="31cc3-122">2\_0</span></span> | <span data-ttu-id="31cc3-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="31cc3-123">2\_x</span></span> | <span data-ttu-id="31cc3-124">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="31cc3-124">2\_sw</span></span> | <span data-ttu-id="31cc3-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="31cc3-125">3\_0</span></span> | <span data-ttu-id="31cc3-126">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="31cc3-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="31cc3-127">texldd</span><span class="sxs-lookup"><span data-stu-id="31cc3-127">texldd</span></span>                |      |      |      |      |      | <span data-ttu-id="31cc3-128">x \*</span><span class="sxs-lookup"><span data-stu-id="31cc3-128">x \*</span></span> | <span data-ttu-id="31cc3-129">x</span><span class="sxs-lookup"><span data-stu-id="31cc3-129">x</span></span>     | <span data-ttu-id="31cc3-130">x</span><span class="sxs-lookup"><span data-stu-id="31cc3-130">x</span></span>    | <span data-ttu-id="31cc3-131">x</span><span class="sxs-lookup"><span data-stu-id="31cc3-131">x</span></span>     |



 

<span data-ttu-id="31cc3-132">\* Cette instruction est uniquement prise en charge par PS \_ 2 \_ a.</span><span class="sxs-lookup"><span data-stu-id="31cc3-132">\* This instruction is only supported by ps\_2\_a.</span></span> <span data-ttu-id="31cc3-133">Elle n’est pas prise en charge par PS \_ 2 \_ b.</span><span class="sxs-lookup"><span data-stu-id="31cc3-133">It is not supported by ps\_2\_b.</span></span> <span data-ttu-id="31cc3-134">Pour plus d’informations sur les profils, consultez [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile).</span><span class="sxs-lookup"><span data-stu-id="31cc3-134">For more information about profiles, see [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile).</span></span>

<span data-ttu-id="31cc3-135">Cette instruction échantillonne une texture à l’aide des coordonnées de texture sur src0, l’échantillonneur spécifié par src1 et les dégradés DSX et DSY provenant de src2 et src3.</span><span class="sxs-lookup"><span data-stu-id="31cc3-135">This instruction samples a texture using the texture coordinates at src0, the sampler specified by src1, and the gradients DSX and DSY coming from src2 and src3.</span></span> <span data-ttu-id="31cc3-136">Les valeurs de gradient x et y sont utilisées pour sélectionner le niveau de mipmap approprié de la texture pour l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="31cc3-136">The x and y gradient values are used to select the appropriate mipmap level of the texture for sampling.</span></span>

<span data-ttu-id="31cc3-137">Toutes les sources prennent en charge des Swizzles arbitraires.</span><span class="sxs-lookup"><span data-stu-id="31cc3-137">All sources support arbitrary swizzles.</span></span>

<span data-ttu-id="31cc3-138">Tous les masques d’écriture sont valides sur la destination.</span><span class="sxs-lookup"><span data-stu-id="31cc3-138">All write masks are valid on the destination.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31cc3-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="31cc3-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31cc3-140">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="31cc3-140">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
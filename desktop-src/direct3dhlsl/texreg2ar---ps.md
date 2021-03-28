---
title: texreg2ar-PS
description: Interprète les composants de couleur alpha et rouges du Registre source en tant que données d’adresse de texture (u, v) pour échantillonner la texture à l’étape correspondant au numéro de registre de destination. Le résultat est stocké dans le registre de destination.
ms.assetid: b31a2ee4-f9b9-4aee-b3be-7ccc5b8c6f3e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 93418e7e9e87178cd64c2d7238b5227de0990378
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463314"
---
# <a name="texreg2ar---ps"></a><span data-ttu-id="fa3c0-104">texreg2ar-PS</span><span class="sxs-lookup"><span data-stu-id="fa3c0-104">texreg2ar - ps</span></span>

<span data-ttu-id="fa3c0-105">Interprète les composants de couleur alpha et rouges du Registre source en tant que données d’adresse de texture (u, v) pour échantillonner la texture à l’étape correspondant au numéro de registre de destination.</span><span class="sxs-lookup"><span data-stu-id="fa3c0-105">Interprets the alpha and red color components of the source register as texture address data (u,v) to sample the texture at the stage corresponding to the destination register number.</span></span> <span data-ttu-id="fa3c0-106">Le résultat est stocké dans le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="fa3c0-106">The result is stored in the destination register.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa3c0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa3c0-107">Syntax</span></span>



| <span data-ttu-id="fa3c0-108">texreg2ar DST, SRC</span><span class="sxs-lookup"><span data-stu-id="fa3c0-108">texreg2ar dst, src</span></span> |
|--------------------|



 

<span data-ttu-id="fa3c0-109">where</span><span class="sxs-lookup"><span data-stu-id="fa3c0-109">where</span></span>

-   <span data-ttu-id="fa3c0-110">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="fa3c0-110">dst is the destination register.</span></span>
-   <span data-ttu-id="fa3c0-111">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="fa3c0-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa3c0-112">Notes</span><span class="sxs-lookup"><span data-stu-id="fa3c0-112">Remarks</span></span>



| <span data-ttu-id="fa3c0-113">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="fa3c0-113">Pixel shader versions</span></span> | <span data-ttu-id="fa3c0-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="fa3c0-114">1\_1</span></span> | <span data-ttu-id="fa3c0-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="fa3c0-115">1\_2</span></span> | <span data-ttu-id="fa3c0-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="fa3c0-116">1\_3</span></span> | <span data-ttu-id="fa3c0-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="fa3c0-117">1\_4</span></span> | <span data-ttu-id="fa3c0-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fa3c0-118">2\_0</span></span> | <span data-ttu-id="fa3c0-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="fa3c0-119">2\_x</span></span> | <span data-ttu-id="fa3c0-120">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="fa3c0-120">2\_sw</span></span> | <span data-ttu-id="fa3c0-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fa3c0-121">3\_0</span></span> | <span data-ttu-id="fa3c0-122">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="fa3c0-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="fa3c0-123">texreg2ar</span><span class="sxs-lookup"><span data-stu-id="fa3c0-123">texreg2ar</span></span>             | <span data-ttu-id="fa3c0-124">x</span><span class="sxs-lookup"><span data-stu-id="fa3c0-124">x</span></span>    | <span data-ttu-id="fa3c0-125">x</span><span class="sxs-lookup"><span data-stu-id="fa3c0-125">x</span></span>    | <span data-ttu-id="fa3c0-126">x</span><span class="sxs-lookup"><span data-stu-id="fa3c0-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="fa3c0-127">Cette instruction est utile pour les opérations de remappage de l’espace colorimétrique.</span><span class="sxs-lookup"><span data-stu-id="fa3c0-127">This instruction is useful for color-space remapping operations.</span></span>

<span data-ttu-id="fa3c0-128">Voici un exemple de la séquence que l’instruction suit :</span><span class="sxs-lookup"><span data-stu-id="fa3c0-128">Here is an example of the sequence the instruction follows:</span></span>

<dl> <span data-ttu-id="fa3c0-129">Tex t (n)</span><span class="sxs-lookup"><span data-stu-id="fa3c0-129">tex t(n)</span></span>  
<span data-ttu-id="fa3c0-130">texreg2ar t (m), t (n) où m > n</span><span class="sxs-lookup"><span data-stu-id="fa3c0-130">texreg2ar t(m), t(n) where m > n</span></span>  
<span data-ttu-id="fa3c0-131">La première instruction charge la couleur de texture (RVBA)</span><span class="sxs-lookup"><span data-stu-id="fa3c0-131">// The first instruction loads the texture color (RGBA)</span></span>  
<span data-ttu-id="fa3c0-132">dans Register TN</span><span class="sxs-lookup"><span data-stu-id="fa3c0-132">// into register tn</span></span>  
<span data-ttu-id="fa3c0-133">Tex TN</span><span class="sxs-lookup"><span data-stu-id="fa3c0-133">tex tn</span></span>  
<span data-ttu-id="fa3c0-134">La deuxième instruction remappe la couleur.</span><span class="sxs-lookup"><span data-stu-id="fa3c0-134">// The second instruction remaps the color</span></span>  
<span data-ttu-id="fa3c0-135">t (m)<sub>RVBA</sub> = TextureSample (stage m)<sub>RVBA</sub> utilisant t (n)<sub>AR</sub> comme coordonnées</span><span class="sxs-lookup"><span data-stu-id="fa3c0-135">t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using t(n)<sub>AR</sub> as coordinates</span></span>
</dl>

<span data-ttu-id="fa3c0-136">\_BX2 ne peut pas être utilisé sur le registre SRC pour les instructions texreg2ar ou [texreg2gb-PS](texreg2gb---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="fa3c0-136">\_bx2 cannot be used on the src register for texreg2ar or [texreg2gb - ps](texreg2gb---ps.md) instructions.</span></span>

<span data-ttu-id="fa3c0-137">Pour cette instruction, le registre source doit utiliser des données non signées.</span><span class="sxs-lookup"><span data-stu-id="fa3c0-137">For this instruction, the source register must use unsigned data.</span></span> <span data-ttu-id="fa3c0-138">L’utilisation de données signées ou mixtes dans le registre source produira des résultats indéfinis.</span><span class="sxs-lookup"><span data-stu-id="fa3c0-138">Use of signed or mixed data in the source register will produce undefined results.</span></span> <span data-ttu-id="fa3c0-139">Pour plus d’informations, consultez [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span><span class="sxs-lookup"><span data-stu-id="fa3c0-139">For more information, see [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa3c0-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fa3c0-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa3c0-141">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="fa3c0-141">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
---
title: texreg2gb-PS
description: Interprète les composants de couleur vert et bleu du Registre source comme des données d’adresse de texture pour échantillonner la texture à l’étape correspondant au numéro de registre de destination.
ms.assetid: 81d3fb3e-ef53-4d25-b65d-c4c9fea0c74c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8d6c428ee5a532919916f0a714db7f81a1c75c12
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971718"
---
# <a name="texreg2gb---ps"></a><span data-ttu-id="1ef37-103">texreg2gb-PS</span><span class="sxs-lookup"><span data-stu-id="1ef37-103">texreg2gb - ps</span></span>

<span data-ttu-id="1ef37-104">Interprète les composants de couleur vert et bleu du Registre source comme des données d’adresse de texture pour échantillonner la texture à l’étape correspondant au numéro de registre de destination.</span><span class="sxs-lookup"><span data-stu-id="1ef37-104">Interprets the green and blue color components of the source register as texture address data to sample the texture at the stage corresponding to the destination register number.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ef37-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ef37-105">Syntax</span></span>



| <span data-ttu-id="1ef37-106">texreg2gb DST, SRC</span><span class="sxs-lookup"><span data-stu-id="1ef37-106">texreg2gb dst, src</span></span> |
|--------------------|



 

<span data-ttu-id="1ef37-107">where</span><span class="sxs-lookup"><span data-stu-id="1ef37-107">where</span></span>

-   <span data-ttu-id="1ef37-108">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="1ef37-108">dst is the destination register.</span></span>
-   <span data-ttu-id="1ef37-109">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="1ef37-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ef37-110">Notes</span><span class="sxs-lookup"><span data-stu-id="1ef37-110">Remarks</span></span>



| <span data-ttu-id="1ef37-111">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="1ef37-111">Pixel shader versions</span></span> | <span data-ttu-id="1ef37-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="1ef37-112">1\_1</span></span> | <span data-ttu-id="1ef37-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="1ef37-113">1\_2</span></span> | <span data-ttu-id="1ef37-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="1ef37-114">1\_3</span></span> | <span data-ttu-id="1ef37-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="1ef37-115">1\_4</span></span> | <span data-ttu-id="1ef37-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1ef37-116">2\_0</span></span> | <span data-ttu-id="1ef37-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="1ef37-117">2\_x</span></span> | <span data-ttu-id="1ef37-118">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="1ef37-118">2\_sw</span></span> | <span data-ttu-id="1ef37-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1ef37-119">3\_0</span></span> | <span data-ttu-id="1ef37-120">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="1ef37-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="1ef37-121">texreg2gb</span><span class="sxs-lookup"><span data-stu-id="1ef37-121">texreg2gb</span></span>             |      | <span data-ttu-id="1ef37-122">x</span><span class="sxs-lookup"><span data-stu-id="1ef37-122">x</span></span>    | <span data-ttu-id="1ef37-123">x</span><span class="sxs-lookup"><span data-stu-id="1ef37-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="1ef37-124">Cette instruction est utile pour les opérations de remappage de l’espace colorimétrique.</span><span class="sxs-lookup"><span data-stu-id="1ef37-124">This instruction is useful for color-space remapping operations.</span></span>

<span data-ttu-id="1ef37-125">Voici un exemple de la séquence suivi par l’instruction.</span><span class="sxs-lookup"><span data-stu-id="1ef37-125">Here is an example of the sequence the instruction follows.</span></span>

<dl> <span data-ttu-id="1ef37-126">Tex t (n)</span><span class="sxs-lookup"><span data-stu-id="1ef37-126">tex t(n)</span></span>  
<span data-ttu-id="1ef37-127">texreg2gb t (m), t (n) où m > n</span><span class="sxs-lookup"><span data-stu-id="1ef37-127">texreg2gb t(m), t(n) where m > n</span></span>  
<span data-ttu-id="1ef37-128">La première instruction charge la couleur de texture (RVBA)</span><span class="sxs-lookup"><span data-stu-id="1ef37-128">// The first instruction loads the texture color (RGBA)</span></span>  
<span data-ttu-id="1ef37-129">dans Register TN</span><span class="sxs-lookup"><span data-stu-id="1ef37-129">// into register tn</span></span>  
<span data-ttu-id="1ef37-130">Tex TN</span><span class="sxs-lookup"><span data-stu-id="1ef37-130">tex tn</span></span>  
<span data-ttu-id="1ef37-131">La deuxième instruction remappe la couleur.</span><span class="sxs-lookup"><span data-stu-id="1ef37-131">// The second instruction remaps the color</span></span>  
<span data-ttu-id="1ef37-132">t (m)<sub>RVBA</sub> = TextureSample (stage m)<sub>RVBA</sub> utilisant t (n)<sub>Go</sub> en tant que coordonnées</span><span class="sxs-lookup"><span data-stu-id="1ef37-132">t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using t(n)<sub>GB</sub> as coordinates</span></span>
</dl>

<span data-ttu-id="1ef37-133">\_BX2 ne peut pas être utilisé sur le registre SRC pour les instructions [texreg2ar-PS](texreg2ar---ps.md) ou texreg2gb.</span><span class="sxs-lookup"><span data-stu-id="1ef37-133">\_bx2 cannot be used on the src register for [texreg2ar - ps](texreg2ar---ps.md) or texreg2gb instructions.</span></span>

<span data-ttu-id="1ef37-134">Pour cette instruction, le registre source doit utiliser des données non signées.</span><span class="sxs-lookup"><span data-stu-id="1ef37-134">For this instruction, the source register must use unsigned data.</span></span> <span data-ttu-id="1ef37-135">L’utilisation de données signées ou mixtes dans le registre source produira des résultats indéfinis.</span><span class="sxs-lookup"><span data-stu-id="1ef37-135">Use of signed or mixed data in the source register will produce undefined results.</span></span> <span data-ttu-id="1ef37-136">Pour plus d’informations, consultez [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span><span class="sxs-lookup"><span data-stu-id="1ef37-136">For more information, see [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ef37-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1ef37-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ef37-138">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="1ef37-138">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
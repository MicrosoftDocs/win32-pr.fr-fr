---
title: texreg2rgb-PS
description: Interprète les composants de couleur rouge, vert et bleu (RVB) du Registre source comme des données d’adresse de texture afin d’échantillonner la texture à l’étape correspondant au numéro de registre de destination. Le résultat est stocké dans le registre de destination.
ms.assetid: 8ec44014-d796-407c-8fe0-036decaf2a3d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f8bcd2bbd7e57ba9dc692f34404a5610cdc517f3
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104507719"
---
# <a name="texreg2rgb---ps"></a><span data-ttu-id="3cf3d-104">texreg2rgb-PS</span><span class="sxs-lookup"><span data-stu-id="3cf3d-104">texreg2rgb - ps</span></span>

<span data-ttu-id="3cf3d-105">Interprète les composants de couleur rouge, vert et bleu (RVB) du Registre source comme des données d’adresse de texture afin d’échantillonner la texture à l’étape correspondant au numéro de registre de destination.</span><span class="sxs-lookup"><span data-stu-id="3cf3d-105">Interprets the red, green, and blue (RGB) color components of the source register as texture address data in order to sample the texture at the stage corresponding to the destination register number.</span></span> <span data-ttu-id="3cf3d-106">Le résultat est stocké dans le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="3cf3d-106">The result is stored in the destination register.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cf3d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3cf3d-107">Syntax</span></span>



| <span data-ttu-id="3cf3d-108">texreg2rgb DST, SRC</span><span class="sxs-lookup"><span data-stu-id="3cf3d-108">texreg2rgb dst, src</span></span> |
|---------------------|



 

<span data-ttu-id="3cf3d-109">where</span><span class="sxs-lookup"><span data-stu-id="3cf3d-109">where</span></span>

-   <span data-ttu-id="3cf3d-110">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="3cf3d-110">dst is the destination register.</span></span>
-   <span data-ttu-id="3cf3d-111">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="3cf3d-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cf3d-112">Notes</span><span class="sxs-lookup"><span data-stu-id="3cf3d-112">Remarks</span></span>



| <span data-ttu-id="3cf3d-113">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="3cf3d-113">Pixel shader versions</span></span> | <span data-ttu-id="3cf3d-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="3cf3d-114">1\_1</span></span> | <span data-ttu-id="3cf3d-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="3cf3d-115">1\_2</span></span> | <span data-ttu-id="3cf3d-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="3cf3d-116">1\_3</span></span> | <span data-ttu-id="3cf3d-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="3cf3d-117">1\_4</span></span> | <span data-ttu-id="3cf3d-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3cf3d-118">2\_0</span></span> | <span data-ttu-id="3cf3d-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3cf3d-119">2\_x</span></span> | <span data-ttu-id="3cf3d-120">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="3cf3d-120">2\_sw</span></span> | <span data-ttu-id="3cf3d-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3cf3d-121">3\_0</span></span> | <span data-ttu-id="3cf3d-122">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="3cf3d-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="3cf3d-123">texreg2rgb</span><span class="sxs-lookup"><span data-stu-id="3cf3d-123">texreg2rgb</span></span>            |      | <span data-ttu-id="3cf3d-124">x</span><span class="sxs-lookup"><span data-stu-id="3cf3d-124">x</span></span>    | <span data-ttu-id="3cf3d-125">x</span><span class="sxs-lookup"><span data-stu-id="3cf3d-125">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="3cf3d-126">Cette instruction est utile pour les opérations de remappage de l’espace colorimétrique.</span><span class="sxs-lookup"><span data-stu-id="3cf3d-126">This instruction is useful for color-space remapping operations.</span></span> <span data-ttu-id="3cf3d-127">Il prend en charge les coordonnées à deux dimensions (2D) et à trois dimensions (3D).</span><span class="sxs-lookup"><span data-stu-id="3cf3d-127">It supports two-dimensional (2D) and three-dimensional (3D) coordinates.</span></span> <span data-ttu-id="3cf3d-128">Il peut être utilisé comme [texreg2ar-PS](texreg2ar---ps.md) ou [texreg2gb-PS](texreg2gb---ps.md) pour remapper les données 2D.</span><span class="sxs-lookup"><span data-stu-id="3cf3d-128">It can be used just like the [texreg2ar - ps](texreg2ar---ps.md) or [texreg2gb - ps](texreg2gb---ps.md) to remap 2D data.</span></span> <span data-ttu-id="3cf3d-129">Toutefois, cette instruction prend également en charge les données 3D afin qu’elles puissent être utilisées avec les textures de cube et de volume 3D.</span><span class="sxs-lookup"><span data-stu-id="3cf3d-129">However, this instruction also supports 3D data so it can be used with cube maps and 3D volume textures.</span></span>

<span data-ttu-id="3cf3d-130">Voici un exemple de la séquence suivi par l’instruction.</span><span class="sxs-lookup"><span data-stu-id="3cf3d-130">Here is an example of the sequence the instruction follows.</span></span>


```
 
tex t(n)
texreg2rgb t(m), t(n)     where m > n
```



<span data-ttu-id="3cf3d-131">Voici plus de détails sur la façon dont le remappage est accompli.</span><span class="sxs-lookup"><span data-stu-id="3cf3d-131">Here is more detail about how the remapping is accomplished.</span></span>

<dl> <span data-ttu-id="3cf3d-132">La première instruction charge la couleur de texture (RVBA) dans le registre TN</span><span class="sxs-lookup"><span data-stu-id="3cf3d-132">// The first instruction loads the texture color (RGBA) into register tn</span></span>  
<span data-ttu-id="3cf3d-133">Tex TN</span><span class="sxs-lookup"><span data-stu-id="3cf3d-133">tex tn</span></span>  
<span data-ttu-id="3cf3d-134">La deuxième instruction remappe la couleur.</span><span class="sxs-lookup"><span data-stu-id="3cf3d-134">// The second instruction remaps the color</span></span>  
<span data-ttu-id="3cf3d-135">t (m)<sub>RVBA</sub> = TextureSample (stage m)<sub>RVBA</sub> utilisant t (n)<sub>RGB</sub> en tant que coordonnées</span><span class="sxs-lookup"><span data-stu-id="3cf3d-135">t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using t(n)<sub>RGB</sub> as coordinates</span></span>
</dl>

## <a name="related-topics"></a><span data-ttu-id="3cf3d-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3cf3d-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cf3d-137">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="3cf3d-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





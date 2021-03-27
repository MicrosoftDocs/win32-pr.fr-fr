---
title: texm3x2depth-PS
description: Calculez la valeur de profondeur à utiliser pour le test de profondeur pour ce pixel.
ms.assetid: bacdd471-a6ee-4998-badd-93ffd4fd61d4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 26d2c3efd1a31681520828b18d606d618d8c900a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971566"
---
# <a name="texm3x2depth---ps"></a><span data-ttu-id="2a8a4-103">texm3x2depth-PS</span><span class="sxs-lookup"><span data-stu-id="2a8a4-103">texm3x2depth - ps</span></span>

<span data-ttu-id="2a8a4-104">Calculez la valeur de profondeur à utiliser pour le test de profondeur pour ce pixel.</span><span class="sxs-lookup"><span data-stu-id="2a8a4-104">Calculate the depth value to be used in depth testing for this pixel.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a8a4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a8a4-105">Syntax</span></span>



| <span data-ttu-id="2a8a4-106">texm3x2depth DST, SRC</span><span class="sxs-lookup"><span data-stu-id="2a8a4-106">texm3x2depth dst, src</span></span> |
|-----------------------|



 

<span data-ttu-id="2a8a4-107">where</span><span class="sxs-lookup"><span data-stu-id="2a8a4-107">where</span></span>

-   <span data-ttu-id="2a8a4-108">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="2a8a4-108">dst is the destination register.</span></span>
-   <span data-ttu-id="2a8a4-109">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="2a8a4-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a8a4-110">Notes</span><span class="sxs-lookup"><span data-stu-id="2a8a4-110">Remarks</span></span>



| <span data-ttu-id="2a8a4-111">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="2a8a4-111">Pixel shader versions</span></span> | <span data-ttu-id="2a8a4-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="2a8a4-112">1\_1</span></span> | <span data-ttu-id="2a8a4-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="2a8a4-113">1\_2</span></span> | <span data-ttu-id="2a8a4-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="2a8a4-114">1\_3</span></span> | <span data-ttu-id="2a8a4-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="2a8a4-115">1\_4</span></span> | <span data-ttu-id="2a8a4-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2a8a4-116">2\_0</span></span> | <span data-ttu-id="2a8a4-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2a8a4-117">2\_x</span></span> | <span data-ttu-id="2a8a4-118">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="2a8a4-118">2\_sw</span></span> | <span data-ttu-id="2a8a4-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2a8a4-119">3\_0</span></span> | <span data-ttu-id="2a8a4-120">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="2a8a4-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="2a8a4-121">texm3x2depth</span><span class="sxs-lookup"><span data-stu-id="2a8a4-121">texm3x2depth</span></span>          |      |      | <span data-ttu-id="2a8a4-122">x</span><span class="sxs-lookup"><span data-stu-id="2a8a4-122">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="2a8a4-123">Cette instruction doit être utilisée avec l’instruction [texm3x2pad-PS](texm3x2pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="2a8a4-123">This instruction must be used with the [texm3x2pad - ps](texm3x2pad---ps.md) instruction.</span></span>

<span data-ttu-id="2a8a4-124">Lors de l’utilisation de ces deux instructions, les registres de texture doivent utiliser la séquence suivante.</span><span class="sxs-lookup"><span data-stu-id="2a8a4-124">When using these two instructions, texture registers must use the following sequence.</span></span>


```
 
tex t(n)                     // Define tn as a standard 3-vector.(tn must be 
                             // defined in some way before it is used
texm3x2pad   t(m),   t(n)    // Where m > n
                             // Calculate z value
texm3x2depth t(m+1), t(n)    // Calculate w value; use both z and w to
                             // find depth
```



<span data-ttu-id="2a8a4-125">Le calcul de la profondeur s’effectue après l’utilisation d’une opération de point pour rechercher z et w.</span><span class="sxs-lookup"><span data-stu-id="2a8a4-125">The depth calculation is done after using a dot product operation to find z and w.</span></span> <span data-ttu-id="2a8a4-126">Voici plus de détails sur la façon dont le calcul de la profondeur est réalisé.</span><span class="sxs-lookup"><span data-stu-id="2a8a4-126">Here is more detail about how the depth calculation is accomplished.</span></span>

<span data-ttu-id="2a8a4-127">L’instruction texm3x2pad calcule z.</span><span class="sxs-lookup"><span data-stu-id="2a8a4-127">The texm3x2pad instruction calculates z.</span></span>

<span data-ttu-id="2a8a4-128">z = TextureCoordinates (étape m)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="2a8a4-128">z = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="2a8a4-129">L’instruction texm3x2depth calcule w.</span><span class="sxs-lookup"><span data-stu-id="2a8a4-129">The texm3x2depth instruction calculates w.</span></span>

<span data-ttu-id="2a8a4-130">w = TextureCoordinates (étape m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="2a8a4-130">w = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="2a8a4-131">Calculez la profondeur et stockez le résultat dans t (m + 1).</span><span class="sxs-lookup"><span data-stu-id="2a8a4-131">Calculate depth and store the result in t(m+1).</span></span>


```
 
if (w == 0)
  t(m+1) = 1.0
else
  t(m+1) = z/w
```



<span data-ttu-id="2a8a4-132">La profondeur calculée est marquée pour être utilisée dans le test de profondeur pour le pixel, remplaçant la valeur de test de profondeur existante pour le pixel.</span><span class="sxs-lookup"><span data-stu-id="2a8a4-132">The calculated depth is tagged to be used in the depth test for the pixel, replacing the existing depth test value for the pixel.</span></span>

<span data-ttu-id="2a8a4-133">Veillez à fixer le z/w à la plage de (0-1).</span><span class="sxs-lookup"><span data-stu-id="2a8a4-133">Be sure to clamp z/w to be in the range of (0-1).</span></span> <span data-ttu-id="2a8a4-134">Si z/w est en dehors de cette plage, le résultat stocké dans la mémoire tampon de profondeur n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="2a8a4-134">If z/w is outside this range, the result stored in the depth buffer will be undefined.</span></span>

<span data-ttu-id="2a8a4-135">Après l’exécution de texm3x2depth, l’inscription t (m + 1) n’est plus disponible pour une utilisation dans le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="2a8a4-135">After running texm3x2depth, register t(m+1) is no longer available for use in the shader.</span></span>

<span data-ttu-id="2a8a4-136">Lors de l’échantillonnage multiple, l’utilisation de cette instruction élimine la plupart des avantages de la mémoire tampon de profondeur supérieure.</span><span class="sxs-lookup"><span data-stu-id="2a8a4-136">When multisampling, using this instruction eliminates most of the benefit of the higher resolution depth buffer.</span></span> <span data-ttu-id="2a8a4-137">Étant donné que le nuanceur de pixels s’exécute une fois par pixel, la valeur de profondeur unique générée par texm3x2depth ou [texdepth-PS](texdepth---ps.md) sera utilisée pour chacun des tests de comparaison de profondeur de sous-pixel.</span><span class="sxs-lookup"><span data-stu-id="2a8a4-137">Because the pixel shader runs once per pixel, the single depth value output by texm3x2depth or [texdepth - ps](texdepth---ps.md) will be used for each of the subpixel depth comparison tests.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a8a4-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2a8a4-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a8a4-139">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="2a8a4-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





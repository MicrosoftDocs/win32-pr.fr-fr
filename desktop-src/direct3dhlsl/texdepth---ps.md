---
title: texdepth-PS
description: Calculez les valeurs de profondeur à utiliser dans le test de comparaison de mémoire tampon de profondeur pour ce pixel.
ms.assetid: f7128dbb-a5f3-4e95-b53b-7432439ae0c4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3eb5cd337108d08efee465c136adf1afb4921123
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103841641"
---
# <a name="texdepth---ps"></a><span data-ttu-id="615c0-103">texdepth-PS</span><span class="sxs-lookup"><span data-stu-id="615c0-103">texdepth - ps</span></span>

<span data-ttu-id="615c0-104">Calculez les valeurs de profondeur à utiliser dans le test de comparaison de mémoire tampon de profondeur pour ce pixel.</span><span class="sxs-lookup"><span data-stu-id="615c0-104">Calculate depth values to be used in the depth buffer comparison test for this pixel.</span></span>

## <a name="syntax"></a><span data-ttu-id="615c0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="615c0-105">Syntax</span></span>



| <span data-ttu-id="615c0-106">texdepth DST</span><span class="sxs-lookup"><span data-stu-id="615c0-106">texdepth dst</span></span> |
|--------------|



 

<span data-ttu-id="615c0-107">where</span><span class="sxs-lookup"><span data-stu-id="615c0-107">where</span></span>

-   <span data-ttu-id="615c0-108">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="615c0-108">dst is the destination register.</span></span>

## <a name="remarks"></a><span data-ttu-id="615c0-109">Notes</span><span class="sxs-lookup"><span data-stu-id="615c0-109">Remarks</span></span>



| <span data-ttu-id="615c0-110">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="615c0-110">Pixel shader versions</span></span> | <span data-ttu-id="615c0-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="615c0-111">1\_1</span></span> | <span data-ttu-id="615c0-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="615c0-112">1\_2</span></span> | <span data-ttu-id="615c0-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="615c0-113">1\_3</span></span> | <span data-ttu-id="615c0-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="615c0-114">1\_4</span></span> | <span data-ttu-id="615c0-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="615c0-115">2\_0</span></span> | <span data-ttu-id="615c0-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="615c0-116">2\_x</span></span> | <span data-ttu-id="615c0-117">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="615c0-117">2\_sw</span></span> | <span data-ttu-id="615c0-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="615c0-118">3\_0</span></span> | <span data-ttu-id="615c0-119">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="615c0-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="615c0-120">texdepth</span><span class="sxs-lookup"><span data-stu-id="615c0-120">texdepth</span></span>              |      |      |      | <span data-ttu-id="615c0-121">x</span><span class="sxs-lookup"><span data-stu-id="615c0-121">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="615c0-122">Cette instruction utilise R5. r/R5. g dans le test de comparaison de la mémoire tampon de profondeur pour ce pixel.</span><span class="sxs-lookup"><span data-stu-id="615c0-122">This instruction uses r5.r / r5.g in the depth buffer comparison test for this pixel.</span></span> <span data-ttu-id="615c0-123">Les données des canaux bleu et alpha sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="615c0-123">The data in the blue and alpha channels is ignored.</span></span> <span data-ttu-id="615c0-124">Si R5. g = 0, le résultat de R5. r/R5. g = 1,0.</span><span class="sxs-lookup"><span data-stu-id="615c0-124">If r5.g = 0, the result of r5.r / r5.g = 1.0.</span></span>

<span data-ttu-id="615c0-125">Le registre temporaire R5 est le seul registre que cette instruction peut utiliser.</span><span class="sxs-lookup"><span data-stu-id="615c0-125">Temporary register r5 is the only register that this instruction can use.</span></span>

<span data-ttu-id="615c0-126">Après l’exécution de cette instruction, le registre temporaire R5 n’est pas disponible pour une utilisation supplémentaire dans le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="615c0-126">After executing this instruction, temporary register r5 is unavailable for additional use in the shader.</span></span>

<span data-ttu-id="615c0-127">Lors de l’échantillonnage multiple, l’utilisation de cette instruction élimine la plupart des avantages de la mémoire tampon de profondeur supérieure.</span><span class="sxs-lookup"><span data-stu-id="615c0-127">When multisampling, using this instruction eliminates most of the benefit of the higher resolution depth buffer.</span></span> <span data-ttu-id="615c0-128">Étant donné que le nuanceur de pixels s’exécute une fois par pixel, la valeur de profondeur unique générée par [texm3x2depth-PS](texm3x2depth---ps.md) ou texdepth sera utilisée pour chacun des tests de comparaison de profondeur de sous-pixel.</span><span class="sxs-lookup"><span data-stu-id="615c0-128">Because the pixel shader runs once per pixel, the single depth value output by [texm3x2depth - ps](texm3x2depth---ps.md) or texdepth will be used for each of the subpixel depth comparison tests.</span></span>

## <a name="examples"></a><span data-ttu-id="615c0-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="615c0-129">Examples</span></span>

<span data-ttu-id="615c0-130">Voici un exemple d’utilisation de texdepth.</span><span class="sxs-lookup"><span data-stu-id="615c0-130">Here is an example using texdepth.</span></span>


```
ps_1_4              
texld  r0, t0        // Sample texture from texture stage 0 (dest 
                     //   register number) into r0
                     // Use texture coordinate data from t0
texcrd r1.rgb, t1    // Load a second set of texture coordinate data into r1
add    r5.rg, r0, r1 // Add the two sets of texture coordinate data
phase                // Phase marker, required when using texdepth instruction
texdepth  r5         // Calculate pixel depth as r5.r / r5.g
                     // Do other color calculations with shader output r0
```



## <a name="related-topics"></a><span data-ttu-id="615c0-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="615c0-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="615c0-132">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="615c0-132">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





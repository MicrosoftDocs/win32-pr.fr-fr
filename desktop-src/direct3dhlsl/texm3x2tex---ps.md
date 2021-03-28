---
title: texm3x2tex-PS
description: Effectue la multiplication de la dernière ligne d’une matrice matrice et utilise le résultat pour effectuer une recherche de texture. texm3x2tex doit être utilisé conjointement avec l’instruction texm3x2pad-PS.
ms.assetid: c6cfbf75-4a63-4c82-9fb6-286b51b7f883
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 62206bc4ef1e1b64ec760a240a087ec13526d896
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990769"
---
# <a name="texm3x2tex---ps"></a><span data-ttu-id="aac6c-104">texm3x2tex-PS</span><span class="sxs-lookup"><span data-stu-id="aac6c-104">texm3x2tex - ps</span></span>

<span data-ttu-id="aac6c-105">Effectue la multiplication de la dernière ligne d’une matrice matrice et utilise le résultat pour effectuer une recherche de texture.</span><span class="sxs-lookup"><span data-stu-id="aac6c-105">Performs the final row of a 3x2 matrix multiply and uses the result to do a texture lookup.</span></span> <span data-ttu-id="aac6c-106">texm3x2tex doit être utilisé conjointement avec l’instruction [texm3x2pad-PS](texm3x2pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="aac6c-106">texm3x2tex must be used in conjunction with the [texm3x2pad - ps](texm3x2pad---ps.md) instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="aac6c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aac6c-107">Syntax</span></span>



| <span data-ttu-id="aac6c-108">texm3x2tex DST, SRC</span><span class="sxs-lookup"><span data-stu-id="aac6c-108">texm3x2tex dst, src</span></span> |
|---------------------|



 

<span data-ttu-id="aac6c-109">where</span><span class="sxs-lookup"><span data-stu-id="aac6c-109">where</span></span>

-   <span data-ttu-id="aac6c-110">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="aac6c-110">dst is the destination register.</span></span>
-   <span data-ttu-id="aac6c-111">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="aac6c-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="aac6c-112">Notes</span><span class="sxs-lookup"><span data-stu-id="aac6c-112">Remarks</span></span>



| <span data-ttu-id="aac6c-113">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="aac6c-113">Pixel shader versions</span></span> | <span data-ttu-id="aac6c-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="aac6c-114">1\_1</span></span> | <span data-ttu-id="aac6c-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="aac6c-115">1\_2</span></span> | <span data-ttu-id="aac6c-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="aac6c-116">1\_3</span></span> | <span data-ttu-id="aac6c-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="aac6c-117">1\_4</span></span> | <span data-ttu-id="aac6c-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="aac6c-118">2\_0</span></span> | <span data-ttu-id="aac6c-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="aac6c-119">2\_x</span></span> | <span data-ttu-id="aac6c-120">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="aac6c-120">2\_sw</span></span> | <span data-ttu-id="aac6c-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="aac6c-121">3\_0</span></span> | <span data-ttu-id="aac6c-122">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="aac6c-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="aac6c-123">texm3x2tex</span><span class="sxs-lookup"><span data-stu-id="aac6c-123">texm3x2tex</span></span>            | <span data-ttu-id="aac6c-124">x</span><span class="sxs-lookup"><span data-stu-id="aac6c-124">x</span></span>    | <span data-ttu-id="aac6c-125">x</span><span class="sxs-lookup"><span data-stu-id="aac6c-125">x</span></span>    | <span data-ttu-id="aac6c-126">x</span><span class="sxs-lookup"><span data-stu-id="aac6c-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="aac6c-127">L’instruction est utilisée comme l’une des deux instructions représentant une opération de multiplication de matrice matrice.</span><span class="sxs-lookup"><span data-stu-id="aac6c-127">The instruction is used as one of two instructions representing a 3x2 matrix multiply operation.</span></span> <span data-ttu-id="aac6c-128">Cette instruction doit être utilisée avec l’instruction [texm3x2pad-PS](texm3x2pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="aac6c-128">This instruction must be used with the [texm3x2pad - ps](texm3x2pad---ps.md) instruction.</span></span>

<span data-ttu-id="aac6c-129">Lors de l’utilisation de ces deux instructions, les registres de texture doivent utiliser la séquence suivante.</span><span class="sxs-lookup"><span data-stu-id="aac6c-129">When using these two instructions, texture registers must use the following sequence.</span></span>


```
 
tex t(n)                      // Define tn as a standard 3-vector (tn must 
                              // be defined in some way before it is used)
texm3x2pad  t(m),   t(n)      // where m > n
                              // Perform first row of matrix multiply
texm3x2tex  t(m+1), t(n)      // Perform second row of matrix multiply 
                              // to get (u,v) to sample texture 
                              // associated with stage m+1
```



<span data-ttu-id="aac6c-130">Voici plus de détails sur la façon dont la multiplication matrice est accomplie.</span><span class="sxs-lookup"><span data-stu-id="aac6c-130">Here is more detail about how the 3x2 multiply is accomplished.</span></span>

<span data-ttu-id="aac6c-131">L’instruction texm3x2pad exécute la première ligne de la multiplication pour<sup>Rechercher u.</sup></span><span class="sxs-lookup"><span data-stu-id="aac6c-131">The texm3x2pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="aac6c-132">u<sup>'</sup> = t (n)<sub>RGB</sub> \* TextureCoordinates (étape m)<sub>UVW</sub></span><span class="sxs-lookup"><span data-stu-id="aac6c-132">u<sup>'</sup> = t(n)<sub>RGB</sub> \* TextureCoordinates(stage m)<sub>UVW</sub></span></span>

<span data-ttu-id="aac6c-133">L’instruction texm3x2tex effectue la deuxième ligne de la multiplication pour rechercher v<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="aac6c-133">The texm3x2tex instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="aac6c-134">v<sup>'</sup> = t (n)<sub>RGB</sub> \* TextureCoordinates (étape m + 1)<sub>UVW</sub></span><span class="sxs-lookup"><span data-stu-id="aac6c-134">v<sup>'</sup> = t(n)<sub>RGB</sub> \* TextureCoordinates(stage m+1)<sub>UVW</sub></span></span>

<span data-ttu-id="aac6c-135">L’instruction texm3x2tex échantillonne la texture à l’étape (m + 1) avec (u<sup>'</sup>, v<sup>'</sup>) et stocke le résultat dans t (m + 1).</span><span class="sxs-lookup"><span data-stu-id="aac6c-135">The texm3x2tex instruction samples the texture on stage (m+1) with (u<sup>'</sup>,v<sup>'</sup>) and stores the result in t(m+1).</span></span>

<span data-ttu-id="aac6c-136">t (m + 1)<sub>RGB</sub> = TextureSample (étape m + 1)<sub>RGB</sub> avec (u<sup>'</sup>, v<sup>'</sup> ) en tant que coordonnées</span><span class="sxs-lookup"><span data-stu-id="aac6c-136">t(m+1)<sub>RGB</sub> = TextureSample(stage m+1)<sub>RGB</sub> using (u<sup>'</sup>, v<sup>'</sup> ) as coordinates</span></span>

## <a name="examples"></a><span data-ttu-id="aac6c-137">Exemples</span><span class="sxs-lookup"><span data-stu-id="aac6c-137">Examples</span></span>

<span data-ttu-id="aac6c-138">Voici un exemple de nuanceur avec les cartes de texture et les étapes de texture identifiées.</span><span class="sxs-lookup"><span data-stu-id="aac6c-138">Here is an example shader with the texture maps and the texture stages identified.</span></span>


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x2pad  t1,  t0   // First row of matrix multiply
texm3x2tex  t2,  t0   // Second row of matrix multiply to get (u,v)
                      // with which to sample texture in stage 2
mov r0, t2            // Output result
```



<span data-ttu-id="aac6c-139">Cet exemple requiert les textures suivantes dans les étapes de texture suivantes.</span><span class="sxs-lookup"><span data-stu-id="aac6c-139">This example requires the following textures in the following texture stages.</span></span>

-   <span data-ttu-id="aac6c-140">L’étape 0 prend un mappage avec les données de perturbation (x, y, z).</span><span class="sxs-lookup"><span data-stu-id="aac6c-140">Stage 0 takes a map with (x,y,z) perturbation data.</span></span>
-   <span data-ttu-id="aac6c-141">L’étape 1 contient des coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="aac6c-141">Stage 1 holds texture coordinates.</span></span> <span data-ttu-id="aac6c-142">Aucune texture n’est nécessaire dans l’étape de texture.</span><span class="sxs-lookup"><span data-stu-id="aac6c-142">No texture is required in the texture stage.</span></span>
-   <span data-ttu-id="aac6c-143">L’étape 2 contient les coordonnées de texture ainsi qu’une texture 2D définie à cette étape de texture.</span><span class="sxs-lookup"><span data-stu-id="aac6c-143">Stage 2 holds both texture coordinates as well as a 2D texture set at that texture stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aac6c-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aac6c-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aac6c-145">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="aac6c-145">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





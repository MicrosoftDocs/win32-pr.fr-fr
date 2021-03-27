---
title: texm3x3-PS
description: Effectue une multiplication de matrice 3x3 quand elle est utilisée conjointement avec deux instructions texm3x3pad-PS.
ms.assetid: d0b14c87-3507-4237-9f2c-1eb94a6df71c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6238a4b148de67275af1b288d57686cc4d381ee9
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971550"
---
# <a name="texm3x3---ps"></a><span data-ttu-id="181be-103">texm3x3-PS</span><span class="sxs-lookup"><span data-stu-id="181be-103">texm3x3 - ps</span></span>

<span data-ttu-id="181be-104">Effectue une multiplication de matrice 3x3 quand elle est utilisée conjointement avec deux instructions [texm3x3pad-PS](texm3x3pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="181be-104">Performs a 3x3 matrix multiply when used in conjunction with two [texm3x3pad - ps](texm3x3pad---ps.md) instructions.</span></span>

## <a name="syntax"></a><span data-ttu-id="181be-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="181be-105">Syntax</span></span>



| <span data-ttu-id="181be-106">texm3x3 DST, SRC</span><span class="sxs-lookup"><span data-stu-id="181be-106">texm3x3 dst, src</span></span> |
|------------------|



 

<span data-ttu-id="181be-107">where</span><span class="sxs-lookup"><span data-stu-id="181be-107">where</span></span>

-   <span data-ttu-id="181be-108">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="181be-108">dst is the destination register.</span></span>
-   <span data-ttu-id="181be-109">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="181be-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="181be-110">Notes</span><span class="sxs-lookup"><span data-stu-id="181be-110">Remarks</span></span>



| <span data-ttu-id="181be-111">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="181be-111">Pixel shader versions</span></span> | <span data-ttu-id="181be-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="181be-112">1\_1</span></span> | <span data-ttu-id="181be-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="181be-113">1\_2</span></span> | <span data-ttu-id="181be-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="181be-114">1\_3</span></span> | <span data-ttu-id="181be-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="181be-115">1\_4</span></span> | <span data-ttu-id="181be-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="181be-116">2\_0</span></span> | <span data-ttu-id="181be-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="181be-117">2\_x</span></span> | <span data-ttu-id="181be-118">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="181be-118">2\_sw</span></span> | <span data-ttu-id="181be-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="181be-119">3\_0</span></span> | <span data-ttu-id="181be-120">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="181be-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="181be-121">texm3x3</span><span class="sxs-lookup"><span data-stu-id="181be-121">texm3x3</span></span>               |      | <span data-ttu-id="181be-122">x</span><span class="sxs-lookup"><span data-stu-id="181be-122">x</span></span>    | <span data-ttu-id="181be-123">x</span><span class="sxs-lookup"><span data-stu-id="181be-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="181be-124">Cette instruction est la même que l’instruction [texm3x3tex-PS](texm3x3tex---ps.md) , sans la recherche de texture.</span><span class="sxs-lookup"><span data-stu-id="181be-124">This instruction is the same as the [texm3x3tex - ps](texm3x3tex---ps.md) instruction, without the texture lookup.</span></span>

<span data-ttu-id="181be-125">Cette instruction est utilisée comme dernière des trois instructions représentant une opération de multiplication de matrice 3x3.</span><span class="sxs-lookup"><span data-stu-id="181be-125">This instruction is used as the final of three instructions representing a 3x3 matrix multiply operation.</span></span> <span data-ttu-id="181be-126">La matrice 3x3 est composée des coordonnées de texture de la troisième étape de texture et des deux étapes de texture précédentes.</span><span class="sxs-lookup"><span data-stu-id="181be-126">The 3x3 matrix is comprised of the texture coordinates of the third texture stage, and by the two preceding texture stages.</span></span> <span data-ttu-id="181be-127">Toute texture assignée à l’une des trois étapes de texture est ignorée.</span><span class="sxs-lookup"><span data-stu-id="181be-127">Any texture assigned to any of the three texture stages is ignored.</span></span>

<span data-ttu-id="181be-128">Cette instruction doit être utilisée avec deux instructions texm3x3pad.</span><span class="sxs-lookup"><span data-stu-id="181be-128">This instruction must be used with two texm3x3pad instructions.</span></span> <span data-ttu-id="181be-129">Les registres de texture doivent respecter la séquence suivante.</span><span class="sxs-lookup"><span data-stu-id="181be-129">Texture registers must follow the following sequence.</span></span>


```
 
tex t(n)                 // Define tn as a standard 3-vector (tn must
                         // be defined in some way before it is used)
texm3x3pad t(m),   t(n)  // where m > n
                         // Perform first row of matrix multiply
texm3x3pad t(m+1), t(n)  // Perform second row of matrix multiply
texm3x3    t(m+2), t(n)  // Perform third row of matrix multiply to get a
                         // 3-vector result
```



<span data-ttu-id="181be-130">Voici plus de détails sur la façon dont la multiplication 3x3 est accomplie.</span><span class="sxs-lookup"><span data-stu-id="181be-130">Here is more detail about how the 3x3 multiply is accomplished.</span></span>

<span data-ttu-id="181be-131">La première instruction texm3x3pad exécute la première ligne de la multiplication pour<sup>Rechercher u.</sup></span><span class="sxs-lookup"><span data-stu-id="181be-131">The first texm3x3pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="181be-132">u<sup>'</sup> = TextureCoordinates (stage m)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="181be-132">u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="181be-133">La deuxième instruction texm3x3pad exécute la deuxième ligne de la multiplication pour rechercher v<sup>»</sup>.</span><span class="sxs-lookup"><span data-stu-id="181be-133">The second texm3x3pad instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="181be-134">v<sup>'</sup> = TextureCoordinates (étape m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="181be-134">v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="181be-135">L’instruction texm3x3tex effectue la troisième ligne de la multiplication pour rechercher w<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="181be-135">The texm3x3tex instruction performs the third row of the multiply to find w<sup>'</sup>.</span></span>

<span data-ttu-id="181be-136">w<sup>'</sup> = TextureCoordinates (étape m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="181be-136">w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="181be-137">Placez le résultat de la multiplication de la matrice dans le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="181be-137">Place the result of the matrix multiply in the destination register.</span></span>

<span data-ttu-id="181be-138">t (m + 2)<sub>RVBA</sub> = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> , 1)</span><span class="sxs-lookup"><span data-stu-id="181be-138">t(m+2)<sub>RGBA</sub> = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> , 1)</span></span>

## <a name="related-topics"></a><span data-ttu-id="181be-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="181be-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="181be-140">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="181be-140">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





---
title: M3X2-PS
description: Multiplie un vecteur à 3 composants par une matrice matrice. | M3X2-PS
ms.assetid: a88e6228-a61a-408c-8d89-a5706dd146d5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 26532c78fa829b9c2a41f715b814ee8a0f44c879
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974386"
---
# <a name="m3x2---ps"></a><span data-ttu-id="0fd2f-104">M3X2-PS</span><span class="sxs-lookup"><span data-stu-id="0fd2f-104">m3x2 - ps</span></span>

<span data-ttu-id="0fd2f-105">Multiplie un vecteur à 3 composants par une matrice matrice.</span><span class="sxs-lookup"><span data-stu-id="0fd2f-105">Multiplies a 3-component vector by a 3x2 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fd2f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0fd2f-106">Syntax</span></span>



| <span data-ttu-id="0fd2f-107">M3X2 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="0fd2f-107">m3x2 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="0fd2f-108">where</span><span class="sxs-lookup"><span data-stu-id="0fd2f-108">where</span></span>

-   <span data-ttu-id="0fd2f-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="0fd2f-109">dst is the destination register.</span></span> <span data-ttu-id="0fd2f-110">Le résultat est un vecteur à 2 composants.</span><span class="sxs-lookup"><span data-stu-id="0fd2f-110">Result is a 2-component vector.</span></span>
-   <span data-ttu-id="0fd2f-111">src0 est un registre source qui représente un vecteur à 3 composants.</span><span class="sxs-lookup"><span data-stu-id="0fd2f-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="0fd2f-112">src1 est un registre source qui représente une matrice matrice, qui correspond au premier des 2 registres consécutifs.</span><span class="sxs-lookup"><span data-stu-id="0fd2f-112">src1 is a source register representing a 3x2 matrix, which corresponds to the first of 2 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fd2f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="0fd2f-113">Remarks</span></span>



| <span data-ttu-id="0fd2f-114">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="0fd2f-114">Pixel shader versions</span></span> | <span data-ttu-id="0fd2f-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="0fd2f-115">1\_1</span></span> | <span data-ttu-id="0fd2f-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="0fd2f-116">1\_2</span></span> | <span data-ttu-id="0fd2f-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="0fd2f-117">1\_3</span></span> | <span data-ttu-id="0fd2f-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="0fd2f-118">1\_4</span></span> | <span data-ttu-id="0fd2f-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0fd2f-119">2\_0</span></span> | <span data-ttu-id="0fd2f-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0fd2f-120">2\_x</span></span> | <span data-ttu-id="0fd2f-121">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="0fd2f-121">2\_sw</span></span> | <span data-ttu-id="0fd2f-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0fd2f-122">3\_0</span></span> | <span data-ttu-id="0fd2f-123">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="0fd2f-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="0fd2f-124">m3x2</span><span class="sxs-lookup"><span data-stu-id="0fd2f-124">m3x2</span></span>                  |      |      |      |      | <span data-ttu-id="0fd2f-125">x</span><span class="sxs-lookup"><span data-stu-id="0fd2f-125">x</span></span>    | <span data-ttu-id="0fd2f-126">x</span><span class="sxs-lookup"><span data-stu-id="0fd2f-126">x</span></span>    | <span data-ttu-id="0fd2f-127">x</span><span class="sxs-lookup"><span data-stu-id="0fd2f-127">x</span></span>     | <span data-ttu-id="0fd2f-128">x</span><span class="sxs-lookup"><span data-stu-id="0fd2f-128">x</span></span>    | <span data-ttu-id="0fd2f-129">x</span><span class="sxs-lookup"><span data-stu-id="0fd2f-129">x</span></span>     |



 

<span data-ttu-id="0fd2f-130">Le masque XY est requis pour le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="0fd2f-130">The xy mask is required for the destination register.</span></span> <span data-ttu-id="0fd2f-131">Les modificateurs de négation et Swizzle sont autorisés pour src0, mais pas pour src1.</span><span class="sxs-lookup"><span data-stu-id="0fd2f-131">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="0fd2f-132">Les équations suivantes illustrent le fonctionnement de l’instruction :</span><span class="sxs-lookup"><span data-stu-id="0fd2f-132">The following equations show how the instruction operates:</span></span>


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z);
```



<span data-ttu-id="0fd2f-133">Le vecteur d’entrée se trouve dans Register src0.</span><span class="sxs-lookup"><span data-stu-id="0fd2f-133">The input vector is in register src0.</span></span> <span data-ttu-id="0fd2f-134">La matrice d’entrée matrice se trouve dans Register src1 et le registre supérieur suivant dans le même fichier de Registre, comme illustré dans l’extension suivante.</span><span class="sxs-lookup"><span data-stu-id="0fd2f-134">The input 3x2 matrix is in register src1 and the next higher register in the same register file, as shown in the following expansion.</span></span> <span data-ttu-id="0fd2f-135">Un résultat 2D est généré, laissant les autres éléments du registre de destination (dest. z et dest. w) non affectés.</span><span class="sxs-lookup"><span data-stu-id="0fd2f-135">A 2D result is produced, leaving the other elements of the destination register (dest.z and dest.w) unaffected.</span></span>

<span data-ttu-id="0fd2f-136">Cette opération est couramment utilisée pour les transformations 2D.</span><span class="sxs-lookup"><span data-stu-id="0fd2f-136">This operation is commonly used for 2D transforms.</span></span> <span data-ttu-id="0fd2f-137">Cette instruction est implémentée en tant que paire de produits scalaires comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="0fd2f-137">This instruction is implemented as a pair of dot products as shown here.</span></span>


```
m3x2   r0.xy, r1, c0   which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
```



<span data-ttu-id="0fd2f-138">Les modificateurs Swizzle et négation ne sont pas valides pour le registre src1.</span><span class="sxs-lookup"><span data-stu-id="0fd2f-138">Swizzle and negate modifiers are invalid for the src1 register.</span></span> <span data-ttu-id="0fd2f-139">Les registres DST et src0, ou l’un des registres src1 + i, ne peuvent pas être identiques.</span><span class="sxs-lookup"><span data-stu-id="0fd2f-139">The dst and src0 register, or any of src1+i registers, cannot be the same.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0fd2f-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0fd2f-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fd2f-141">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="0fd2f-141">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





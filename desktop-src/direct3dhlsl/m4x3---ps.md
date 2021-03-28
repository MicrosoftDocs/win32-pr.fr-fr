---
title: m4x3-PS
description: Multiplie un vecteur à 4 composants par une matrice 4x3. | m4x3-PS
ms.assetid: cf9ae4c3-6cdf-4c6f-b34c-0ebd3c8a4123
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7787268906c2c9e92dc1e3fa1ec87c4af3079255
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974339"
---
# <a name="m4x3---ps"></a><span data-ttu-id="0af68-104">m4x3-PS</span><span class="sxs-lookup"><span data-stu-id="0af68-104">m4x3 - ps</span></span>

<span data-ttu-id="0af68-105">Multiplie un vecteur à 4 composants par une matrice 4x3.</span><span class="sxs-lookup"><span data-stu-id="0af68-105">Multiplies a 4-component vector by a 4x3 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="0af68-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0af68-106">Syntax</span></span>



| <span data-ttu-id="0af68-107">m4x3 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="0af68-107">m4x3 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="0af68-108">where</span><span class="sxs-lookup"><span data-stu-id="0af68-108">where</span></span>

-   <span data-ttu-id="0af68-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="0af68-109">dst is the destination register.</span></span> <span data-ttu-id="0af68-110">Le résultat est un vecteur à 3 composants.</span><span class="sxs-lookup"><span data-stu-id="0af68-110">Result is a 3-component vector.</span></span>
-   <span data-ttu-id="0af68-111">src0 est un registre source qui représente un vecteur à 4 composants.</span><span class="sxs-lookup"><span data-stu-id="0af68-111">src0 is a source register representing a 4-component vector.</span></span>
-   <span data-ttu-id="0af68-112">src1 est un registre source qui représente une matrice 4x3, qui correspond au premier des 3 registres consécutifs.</span><span class="sxs-lookup"><span data-stu-id="0af68-112">src1 is a source register representing a 4x3 matrix, which corresponds to the first of 3 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="0af68-113">Notes</span><span class="sxs-lookup"><span data-stu-id="0af68-113">Remarks</span></span>



| <span data-ttu-id="0af68-114">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="0af68-114">Pixel shader versions</span></span> | <span data-ttu-id="0af68-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="0af68-115">1\_1</span></span> | <span data-ttu-id="0af68-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="0af68-116">1\_2</span></span> | <span data-ttu-id="0af68-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="0af68-117">1\_3</span></span> | <span data-ttu-id="0af68-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="0af68-118">1\_4</span></span> | <span data-ttu-id="0af68-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0af68-119">2\_0</span></span> | <span data-ttu-id="0af68-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0af68-120">2\_x</span></span> | <span data-ttu-id="0af68-121">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="0af68-121">2\_sw</span></span> | <span data-ttu-id="0af68-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0af68-122">3\_0</span></span> | <span data-ttu-id="0af68-123">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="0af68-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="0af68-124">m4x3</span><span class="sxs-lookup"><span data-stu-id="0af68-124">m4x3</span></span>                  |      |      |      |      | <span data-ttu-id="0af68-125">x</span><span class="sxs-lookup"><span data-stu-id="0af68-125">x</span></span>    | <span data-ttu-id="0af68-126">x</span><span class="sxs-lookup"><span data-stu-id="0af68-126">x</span></span>    | <span data-ttu-id="0af68-127">x</span><span class="sxs-lookup"><span data-stu-id="0af68-127">x</span></span>     | <span data-ttu-id="0af68-128">x</span><span class="sxs-lookup"><span data-stu-id="0af68-128">x</span></span>    | <span data-ttu-id="0af68-129">x</span><span class="sxs-lookup"><span data-stu-id="0af68-129">x</span></span>     |



 

<span data-ttu-id="0af68-130">Le masque XYZ est requis pour le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="0af68-130">The xyz mask is required for the destination register.</span></span> <span data-ttu-id="0af68-131">Les modificateurs de négation et Swizzle sont autorisés pour src0, mais pas pour src1.</span><span class="sxs-lookup"><span data-stu-id="0af68-131">Negate and swizzle modifiers are allowed for src0, but not for src1.</span></span>

<span data-ttu-id="0af68-132">L’extrait de code suivant montre les opérations effectuées.</span><span class="sxs-lookup"><span data-stu-id="0af68-132">The following code snippet shows the operations performed.</span></span>


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z) + (src0.w*src1.w);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z) + (src0.w*src2.w);
dest.z = (src0.x*src3.x) + (src0.y*src3.y) + (src0.z*src3.z) + (src0.w*src3.w);
```



<span data-ttu-id="0af68-133">Le vecteur d’entrée se trouve dans Register src0.</span><span class="sxs-lookup"><span data-stu-id="0af68-133">The input vector is in register src0.</span></span> <span data-ttu-id="0af68-134">La matrice d’entrée 4x3 est dans Register src1, et les deux registres suivants supérieurs, comme illustré dans l’expansion ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="0af68-134">The input 4x3 matrix is in register src1, and the next two higher registers, as shown in the expansion below.</span></span> <span data-ttu-id="0af68-135">Un résultat 3D est généré, ce qui laisse l’autre élément du registre de destination (dest. w) non affecté.</span><span class="sxs-lookup"><span data-stu-id="0af68-135">A 3D result is produced, leaving the other element of the destination register (dest.w) unaffected.</span></span>

<span data-ttu-id="0af68-136">Cette opération est couramment utilisée pour transformer un vecteur de position en une matrice qui n’a pas d’effet de projet, comme c’est le cas dans les transformations d’espace de modèle.</span><span class="sxs-lookup"><span data-stu-id="0af68-136">This operation is commonly used for transforming a position vector by a matrix that has no projective effect, such as occurs in model-space transformations.</span></span> <span data-ttu-id="0af68-137">Cette instruction est implémentée sous la forme d’un ensemble de produits point, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="0af68-137">This instruction is implemented as a set of dot products as shown below.</span></span>


```
m4x3   r0.xyz, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
```



<span data-ttu-id="0af68-138">Les modificateurs Swizzle et négation ne sont pas valides pour le registre src1.</span><span class="sxs-lookup"><span data-stu-id="0af68-138">Swizzle and negate modifiers are invalid for the src1 register.</span></span> <span data-ttu-id="0af68-139">Les registres DST et src0 ne peuvent pas être identiques.</span><span class="sxs-lookup"><span data-stu-id="0af68-139">The dst and src0 register cannot be the same.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0af68-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0af68-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0af68-141">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="0af68-141">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





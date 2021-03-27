---
title: M4X4-vs
description: Multiplie un vecteur à 4 composants par une matrice 4x4. | M4X4-vs
ms.assetid: 016100ac-e316-41fd-a606-271be7394a1a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 846802f46cd829b3e610ec016a546c5302895bd9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211438"
---
# <a name="m4x4---vs"></a><span data-ttu-id="e8eda-104">M4X4-vs</span><span class="sxs-lookup"><span data-stu-id="e8eda-104">m4x4 - vs</span></span>

<span data-ttu-id="e8eda-105">Multiplie un vecteur à 4 composants par une matrice 4x4.</span><span class="sxs-lookup"><span data-stu-id="e8eda-105">Multiplies a 4-component vector by a 4x4 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8eda-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8eda-106">Syntax</span></span>



| <span data-ttu-id="e8eda-107">M4X4 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="e8eda-107">m4x4 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="e8eda-108">where</span><span class="sxs-lookup"><span data-stu-id="e8eda-108">where</span></span>

-   <span data-ttu-id="e8eda-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="e8eda-109">dst is the destination register.</span></span> <span data-ttu-id="e8eda-110">Le résultat est un vecteur à 4 composants.</span><span class="sxs-lookup"><span data-stu-id="e8eda-110">Result is a 4-component vector.</span></span>
-   <span data-ttu-id="e8eda-111">src0 est un registre source qui représente un vecteur à 4 composants.</span><span class="sxs-lookup"><span data-stu-id="e8eda-111">src0 is a source register representing a 4-component vector.</span></span>
-   <span data-ttu-id="e8eda-112">src1 est un registre source qui représente une matrice 4x4, qui correspond au premier des 4 registres consécutifs.</span><span class="sxs-lookup"><span data-stu-id="e8eda-112">src1 is a source register representing a 4x4 matrix, which corresponds to the first of 4 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8eda-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e8eda-113">Remarks</span></span>



| <span data-ttu-id="e8eda-114">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="e8eda-114">Vertex shader versions</span></span> | <span data-ttu-id="e8eda-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="e8eda-115">1\_1</span></span> | <span data-ttu-id="e8eda-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e8eda-116">2\_0</span></span> | <span data-ttu-id="e8eda-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e8eda-117">2\_x</span></span> | <span data-ttu-id="e8eda-118">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="e8eda-118">2\_sw</span></span> | <span data-ttu-id="e8eda-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e8eda-119">3\_0</span></span> | <span data-ttu-id="e8eda-120">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="e8eda-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="e8eda-121">m4x4</span><span class="sxs-lookup"><span data-stu-id="e8eda-121">m4x4</span></span>                   | <span data-ttu-id="e8eda-122">x</span><span class="sxs-lookup"><span data-stu-id="e8eda-122">x</span></span>    | <span data-ttu-id="e8eda-123">x</span><span class="sxs-lookup"><span data-stu-id="e8eda-123">x</span></span>    | <span data-ttu-id="e8eda-124">x</span><span class="sxs-lookup"><span data-stu-id="e8eda-124">x</span></span>    | <span data-ttu-id="e8eda-125">x</span><span class="sxs-lookup"><span data-stu-id="e8eda-125">x</span></span>     | <span data-ttu-id="e8eda-126">x</span><span class="sxs-lookup"><span data-stu-id="e8eda-126">x</span></span>    | <span data-ttu-id="e8eda-127">x</span><span class="sxs-lookup"><span data-stu-id="e8eda-127">x</span></span>     |



 

<span data-ttu-id="e8eda-128">Le masque XYZW (par défaut) est requis pour le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="e8eda-128">The xyzw (default) mask is required for the destination register.</span></span> <span data-ttu-id="e8eda-129">Les modificateurs de négation et Swizzle sont autorisés pour src0, mais pas pour src1.</span><span class="sxs-lookup"><span data-stu-id="e8eda-129">Negate and swizzle modifiers are allowed for src0, but not for src1.</span></span>

<span data-ttu-id="e8eda-130">Les modificateurs Swizzle et négation ne sont pas valides pour le registre src0.</span><span class="sxs-lookup"><span data-stu-id="e8eda-130">Swizzle and negate modifiers are invalid for the src0 register.</span></span> <span data-ttu-id="e8eda-131">Les registres dest et src0 ne peuvent pas être identiques.</span><span class="sxs-lookup"><span data-stu-id="e8eda-131">The dest and src0 registers cannot be the same.</span></span>

<span data-ttu-id="e8eda-132">Le fragment de code suivant montre les opérations effectuées.</span><span class="sxs-lookup"><span data-stu-id="e8eda-132">The following code fragment shows the operations performed.</span></span>


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z) + 
        (src0.w * src1.w);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z) + 
        (src0.w * src2.w);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z) + 
        (src0.w * src3.w);
dest.w = (src0.x * src4.x) + (src0.y * src4.y) + (src0.z * src4.z) + 
        (src0.w * src4.w);
```



<span data-ttu-id="e8eda-133">Le vecteur d’entrée se trouve dans Register src0.</span><span class="sxs-lookup"><span data-stu-id="e8eda-133">The input vector is in register src0.</span></span> <span data-ttu-id="e8eda-134">La matrice 4x4 d’entrée se trouve dans Register src1, et les trois registres supérieurs suivants, comme illustré dans l’expansion ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="e8eda-134">The input 4x4 matrix is in register src1, and the next three higher registers, as shown in the expansion below.</span></span>

<span data-ttu-id="e8eda-135">Cette opération est couramment utilisée pour transformer une position en une matrice de projection.</span><span class="sxs-lookup"><span data-stu-id="e8eda-135">This operation is commonly used for transforming a position by a projection matrix.</span></span> <span data-ttu-id="e8eda-136">Cette instruction est implémentée sous la forme d’une série de produits scalaires, comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="e8eda-136">This instruction is implemented as a series of dot products as shown here.</span></span>


```
m4x4   r0.xyzw, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
dp4   r0.w, r1, c3
```



## <a name="related-topics"></a><span data-ttu-id="e8eda-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e8eda-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8eda-138">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="e8eda-138">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





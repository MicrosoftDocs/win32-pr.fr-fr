---
title: M3x4-vs
description: Multiplie un vecteur à 3 composants par une matrice 3x4. | M3x4-vs
ms.assetid: 8bec1ac5-376b-4eae-ba82-b42a6c0e7c4e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a4018698dbe6ab986945a84c1fcf9ce0431bd0fc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974026"
---
# <a name="m3x4---vs"></a><span data-ttu-id="bc96f-104">M3x4-vs</span><span class="sxs-lookup"><span data-stu-id="bc96f-104">m3x4 - vs</span></span>

<span data-ttu-id="bc96f-105">Multiplie un vecteur à 3 composants par une matrice 3x4.</span><span class="sxs-lookup"><span data-stu-id="bc96f-105">Multiplies a 3-component vector by a 3x4 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc96f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc96f-106">Syntax</span></span>



| <span data-ttu-id="bc96f-107">M3x4 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="bc96f-107">m3x4 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="bc96f-108">where</span><span class="sxs-lookup"><span data-stu-id="bc96f-108">where</span></span>

-   <span data-ttu-id="bc96f-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="bc96f-109">dst is the destination register.</span></span> <span data-ttu-id="bc96f-110">Le résultat est un vecteur à 4 composants.</span><span class="sxs-lookup"><span data-stu-id="bc96f-110">Result is a 4-component vector.</span></span>
-   <span data-ttu-id="bc96f-111">src0 est un registre source qui représente un vecteur à 3 composants.</span><span class="sxs-lookup"><span data-stu-id="bc96f-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="bc96f-112">src1 est un registre source qui représente une matrice 3x4, qui correspond au premier des 4 registres consécutifs.</span><span class="sxs-lookup"><span data-stu-id="bc96f-112">src1 is a source register representing a 3x4 matrix, which corresponds to the first of 4 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc96f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="bc96f-113">Remarks</span></span>



| <span data-ttu-id="bc96f-114">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="bc96f-114">Vertex shader versions</span></span> | <span data-ttu-id="bc96f-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="bc96f-115">1\_1</span></span> | <span data-ttu-id="bc96f-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bc96f-116">2\_0</span></span> | <span data-ttu-id="bc96f-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="bc96f-117">2\_x</span></span> | <span data-ttu-id="bc96f-118">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="bc96f-118">2\_sw</span></span> | <span data-ttu-id="bc96f-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bc96f-119">3\_0</span></span> | <span data-ttu-id="bc96f-120">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="bc96f-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="bc96f-121">m3x4</span><span class="sxs-lookup"><span data-stu-id="bc96f-121">m3x4</span></span>                   | <span data-ttu-id="bc96f-122">x</span><span class="sxs-lookup"><span data-stu-id="bc96f-122">x</span></span>    | <span data-ttu-id="bc96f-123">x</span><span class="sxs-lookup"><span data-stu-id="bc96f-123">x</span></span>    | <span data-ttu-id="bc96f-124">x</span><span class="sxs-lookup"><span data-stu-id="bc96f-124">x</span></span>    | <span data-ttu-id="bc96f-125">x</span><span class="sxs-lookup"><span data-stu-id="bc96f-125">x</span></span>     | <span data-ttu-id="bc96f-126">x</span><span class="sxs-lookup"><span data-stu-id="bc96f-126">x</span></span>    | <span data-ttu-id="bc96f-127">x</span><span class="sxs-lookup"><span data-stu-id="bc96f-127">x</span></span>     |



 

<span data-ttu-id="bc96f-128">Le masque XYZW (par défaut) est requis pour le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="bc96f-128">The xyzw (default) mask is required for the destination register.</span></span> <span data-ttu-id="bc96f-129">Les modificateurs de négation et Swizzle sont autorisés pour src0, mais pas pour src1.</span><span class="sxs-lookup"><span data-stu-id="bc96f-129">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="bc96f-130">Le fragment de code suivant montre les opérations effectuées.</span><span class="sxs-lookup"><span data-stu-id="bc96f-130">The following code fragment shows the operations performed.</span></span>


```
 
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z);
dest.w = (src0.x * src4.x) + (src0.y * src4.y) + (src0.z * src4.z);
```



<span data-ttu-id="bc96f-131">Le vecteur d’entrée se trouve dans Register src0.</span><span class="sxs-lookup"><span data-stu-id="bc96f-131">The input vector is in register src0.</span></span> <span data-ttu-id="bc96f-132">La matrice d’entrée 3x4 est dans Register src1 et les trois registres supérieurs suivants, comme illustré dans l’expansion ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="bc96f-132">The input 3x4 matrix is in register src1 and the next three higher registers, as shown in the expansion below.</span></span>

<span data-ttu-id="bc96f-133">Cette opération est couramment utilisée pour transformer un vecteur de position en une matrice qui a un effet de projet, mais qui n’applique aucune traduction.</span><span class="sxs-lookup"><span data-stu-id="bc96f-133">This operation is commonly used for transforming a position vector by a matrix that has a projective effect but applies no translation.</span></span> <span data-ttu-id="bc96f-134">Cette instruction est implémentée en tant que paire de produits scalaires comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="bc96f-134">This instruction is implemented as a pair of dot products as shown here.</span></span>


```
m3x4   r0.xyzw, r1, c0   will be expanded to: 

dp3 r0.x, r1, c0
dp3 r0.y, r1, c1
dp3 r0.z, r1, c2
dp3 r0.w, r1, c3
```



## <a name="related-topics"></a><span data-ttu-id="bc96f-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bc96f-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc96f-136">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="bc96f-136">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





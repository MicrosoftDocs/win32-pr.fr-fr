---
title: M3X2-vs
description: Multiplie un vecteur à 3 composants par une matrice matrice. | M3X2-vs
ms.assetid: 4ef3bd47-3e38-4d9d-a8f5-6ee9c08de69c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 870a8d4918870930faa536ead01dab2947d5faea
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211441"
---
# <a name="m3x2---vs"></a><span data-ttu-id="05a3d-104">M3X2-vs</span><span class="sxs-lookup"><span data-stu-id="05a3d-104">m3x2 - vs</span></span>

<span data-ttu-id="05a3d-105">Multiplie un vecteur à 3 composants par une matrice matrice.</span><span class="sxs-lookup"><span data-stu-id="05a3d-105">Multiplies a 3-component vector by a 3x2 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="05a3d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05a3d-106">Syntax</span></span>



| <span data-ttu-id="05a3d-107">M3X2 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="05a3d-107">m3x2 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="05a3d-108">where</span><span class="sxs-lookup"><span data-stu-id="05a3d-108">where</span></span>

-   <span data-ttu-id="05a3d-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="05a3d-109">dst is the destination register.</span></span> <span data-ttu-id="05a3d-110">Le résultat est un vecteur à 2 composants.</span><span class="sxs-lookup"><span data-stu-id="05a3d-110">Result is a 2-component vector.</span></span>
-   <span data-ttu-id="05a3d-111">src0 est un registre source qui représente un vecteur à 3 composants.</span><span class="sxs-lookup"><span data-stu-id="05a3d-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="05a3d-112">src1 est un registre source qui représente une matrice matrice, qui correspond au premier des 2 registres consécutifs.</span><span class="sxs-lookup"><span data-stu-id="05a3d-112">src1 is a source register representing a 3x2 matrix, which corresponds to the first of 2 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="05a3d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="05a3d-113">Remarks</span></span>



| <span data-ttu-id="05a3d-114">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="05a3d-114">Vertex shader versions</span></span> | <span data-ttu-id="05a3d-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="05a3d-115">1\_1</span></span> | <span data-ttu-id="05a3d-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="05a3d-116">2\_0</span></span> | <span data-ttu-id="05a3d-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="05a3d-117">2\_x</span></span> | <span data-ttu-id="05a3d-118">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="05a3d-118">2\_sw</span></span> | <span data-ttu-id="05a3d-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="05a3d-119">3\_0</span></span> | <span data-ttu-id="05a3d-120">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="05a3d-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="05a3d-121">m3x2</span><span class="sxs-lookup"><span data-stu-id="05a3d-121">m3x2</span></span>                   | <span data-ttu-id="05a3d-122">x</span><span class="sxs-lookup"><span data-stu-id="05a3d-122">x</span></span>    | <span data-ttu-id="05a3d-123">x</span><span class="sxs-lookup"><span data-stu-id="05a3d-123">x</span></span>    | <span data-ttu-id="05a3d-124">x</span><span class="sxs-lookup"><span data-stu-id="05a3d-124">x</span></span>    | <span data-ttu-id="05a3d-125">x</span><span class="sxs-lookup"><span data-stu-id="05a3d-125">x</span></span>     | <span data-ttu-id="05a3d-126">x</span><span class="sxs-lookup"><span data-stu-id="05a3d-126">x</span></span>    | <span data-ttu-id="05a3d-127">x</span><span class="sxs-lookup"><span data-stu-id="05a3d-127">x</span></span>     |



 

<span data-ttu-id="05a3d-128">Le masque XY est requis pour le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="05a3d-128">The xy mask is required for the destination register.</span></span> <span data-ttu-id="05a3d-129">Les modificateurs de négation et Swizzle sont autorisés pour src0, mais pas pour src1.</span><span class="sxs-lookup"><span data-stu-id="05a3d-129">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="05a3d-130">Les équations suivantes illustrent le fonctionnement de l’instruction :</span><span class="sxs-lookup"><span data-stu-id="05a3d-130">The following equations show how the instruction operates:</span></span>


```
dest.x = (src0.x * src1.x) + (src0.x * src1.y) + (src0.x * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
```



<span data-ttu-id="05a3d-131">Le vecteur d’entrée se trouve dans Register src0.</span><span class="sxs-lookup"><span data-stu-id="05a3d-131">The input vector is in register src0.</span></span> <span data-ttu-id="05a3d-132">La matrice d’entrée matrice se trouve dans Register src1 et le registre supérieur suivant dans le même fichier de Registre, comme illustré dans l’extension suivante.</span><span class="sxs-lookup"><span data-stu-id="05a3d-132">The input 3x2 matrix is in register src1 and the next higher register in the same register file, as shown in the following expansion.</span></span> <span data-ttu-id="05a3d-133">Un résultat 2D est généré, laissant les autres éléments du registre de destination (dest. z et dest. w) non affectés.</span><span class="sxs-lookup"><span data-stu-id="05a3d-133">A 2D result is produced, leaving the other elements of the destination register (dest.z and dest.w) unaffected.</span></span>

<span data-ttu-id="05a3d-134">Cette opération est couramment utilisée pour les transformations 2D.</span><span class="sxs-lookup"><span data-stu-id="05a3d-134">This operation is commonly used for 2D transforms.</span></span> <span data-ttu-id="05a3d-135">Cette instruction est implémentée en tant que paire de produits scalaires comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="05a3d-135">This instruction is implemented as a pair of dot products as shown here.</span></span>


```
m3x2   r0.xy, r1, c0   which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
```



<span data-ttu-id="05a3d-136">Les modificateurs Swizzle et négation ne sont pas valides pour le registre src1.</span><span class="sxs-lookup"><span data-stu-id="05a3d-136">Swizzle and negate modifiers are invalid for the src1 register.</span></span> <span data-ttu-id="05a3d-137">Le registre dest et src0, ou l’un des registres src1 + i, ne peut pas être identique.</span><span class="sxs-lookup"><span data-stu-id="05a3d-137">The dest and src0 register, or any of src1+i registers, cannot be the same.</span></span>

## <a name="related-topics"></a><span data-ttu-id="05a3d-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="05a3d-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05a3d-139">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="05a3d-139">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





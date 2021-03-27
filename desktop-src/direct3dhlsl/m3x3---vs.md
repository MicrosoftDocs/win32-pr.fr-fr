---
title: M3x3-vs
description: Multiplie un vecteur à 3 composants par une matrice 3x3. | M3x3-vs
ms.assetid: 6a749ed0-097d-4354-bc70-fbcd879eafab
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e75cdb4b098b92ea358c32e40b3948c7ac73e0cf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104394000"
---
# <a name="m3x3---vs"></a><span data-ttu-id="5b49d-104">M3x3-vs</span><span class="sxs-lookup"><span data-stu-id="5b49d-104">m3x3 - vs</span></span>

<span data-ttu-id="5b49d-105">Multiplie un vecteur à 3 composants par une matrice 3x3.</span><span class="sxs-lookup"><span data-stu-id="5b49d-105">Multiplies a 3-component vector by a 3x3 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b49d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b49d-106">Syntax</span></span>



| <span data-ttu-id="5b49d-107">M3x3 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="5b49d-107">m3x3 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="5b49d-108">where</span><span class="sxs-lookup"><span data-stu-id="5b49d-108">where</span></span>

-   <span data-ttu-id="5b49d-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="5b49d-109">dst is the destination register.</span></span> <span data-ttu-id="5b49d-110">Le résultat est un vecteur à 3 composants.</span><span class="sxs-lookup"><span data-stu-id="5b49d-110">Result is a 3-component vector.</span></span>
-   <span data-ttu-id="5b49d-111">src0 est un registre source qui représente un vecteur à 3 composants.</span><span class="sxs-lookup"><span data-stu-id="5b49d-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="5b49d-112">src1 est un registre source qui représente une matrice 3x3, qui correspond au premier des 3 registres consécutifs.</span><span class="sxs-lookup"><span data-stu-id="5b49d-112">src1 is a source register representing a 3x3 matrix, which corresponds to the first of 3 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b49d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="5b49d-113">Remarks</span></span>



| <span data-ttu-id="5b49d-114">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="5b49d-114">Vertex shader versions</span></span> | <span data-ttu-id="5b49d-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="5b49d-115">1\_1</span></span> | <span data-ttu-id="5b49d-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5b49d-116">2\_0</span></span> | <span data-ttu-id="5b49d-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5b49d-117">2\_x</span></span> | <span data-ttu-id="5b49d-118">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="5b49d-118">2\_sw</span></span> | <span data-ttu-id="5b49d-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5b49d-119">3\_0</span></span> | <span data-ttu-id="5b49d-120">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="5b49d-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="5b49d-121">m3x3</span><span class="sxs-lookup"><span data-stu-id="5b49d-121">m3x3</span></span>                   | <span data-ttu-id="5b49d-122">x</span><span class="sxs-lookup"><span data-stu-id="5b49d-122">x</span></span>    | <span data-ttu-id="5b49d-123">x</span><span class="sxs-lookup"><span data-stu-id="5b49d-123">x</span></span>    | <span data-ttu-id="5b49d-124">x</span><span class="sxs-lookup"><span data-stu-id="5b49d-124">x</span></span>    | <span data-ttu-id="5b49d-125">x</span><span class="sxs-lookup"><span data-stu-id="5b49d-125">x</span></span>     | <span data-ttu-id="5b49d-126">x</span><span class="sxs-lookup"><span data-stu-id="5b49d-126">x</span></span>    | <span data-ttu-id="5b49d-127">x</span><span class="sxs-lookup"><span data-stu-id="5b49d-127">x</span></span>     |



 

<span data-ttu-id="5b49d-128">Le masque XYZ est requis pour le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="5b49d-128">The xyz mask is required for the destination register.</span></span> <span data-ttu-id="5b49d-129">Les modificateurs de négation et Swizzle sont autorisés pour src0, mais pas pour src1.</span><span class="sxs-lookup"><span data-stu-id="5b49d-129">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="5b49d-130">Le fragment de code suivant montre les opérations effectuées.</span><span class="sxs-lookup"><span data-stu-id="5b49d-130">The following code fragment shows the operations performed.</span></span>


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z);
```



<span data-ttu-id="5b49d-131">Le vecteur d’entrée se trouve dans Register src0.</span><span class="sxs-lookup"><span data-stu-id="5b49d-131">The input vector is in register src0.</span></span> <span data-ttu-id="5b49d-132">La matrice 3x3 entrée se trouve dans Register src1, et les deux registres supérieurs suivants, comme illustré dans l’expansion ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="5b49d-132">The input 3x3 matrix is in register src1, and the next two higher registers, as shown in the expansion below.</span></span> <span data-ttu-id="5b49d-133">Un résultat 3D est généré, ce qui laisse l’autre élément du registre de destination (dest. w) non affecté.</span><span class="sxs-lookup"><span data-stu-id="5b49d-133">A 3D result is produced, leaving the other element of the destination register (dest.w) unaffected.</span></span>

<span data-ttu-id="5b49d-134">Cette opération est couramment utilisée pour transformer les vecteurs normaux lors des calculs d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="5b49d-134">This operation is commonly used for transforming normal vectors during lighting computations.</span></span> <span data-ttu-id="5b49d-135">Cette instruction est implémentée en tant que paire de produits scalaires comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="5b49d-135">This instruction is implemented as a pair of dot products as shown below.</span></span>


```
m3x3 r0.xyz, r1, c0  which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
dp3   r0.z, r1, c2
```



## <a name="related-topics"></a><span data-ttu-id="5b49d-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5b49d-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b49d-137">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="5b49d-137">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





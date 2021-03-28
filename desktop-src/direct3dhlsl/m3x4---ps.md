---
title: M3x4-PS
description: Multiplie un vecteur à 3 composants par une matrice 3x4. | M3x4-PS
ms.assetid: b749d3cd-2acf-450c-94f2-fea5e1c8f4d2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4c245f4765853301a7c8319c8038b9ed342e3715
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974351"
---
# <a name="m3x4---ps"></a><span data-ttu-id="6211c-104">M3x4-PS</span><span class="sxs-lookup"><span data-stu-id="6211c-104">m3x4 - ps</span></span>

<span data-ttu-id="6211c-105">Multiplie un vecteur à 3 composants par une matrice 3x4.</span><span class="sxs-lookup"><span data-stu-id="6211c-105">Multiplies a 3-component vector by a 3x4 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="6211c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6211c-106">Syntax</span></span>



| <span data-ttu-id="6211c-107">M3x4 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="6211c-107">m3x4 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="6211c-108">where</span><span class="sxs-lookup"><span data-stu-id="6211c-108">where</span></span>

-   <span data-ttu-id="6211c-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="6211c-109">dst is the destination register.</span></span> <span data-ttu-id="6211c-110">Le résultat est un vecteur à 4 composants.</span><span class="sxs-lookup"><span data-stu-id="6211c-110">Result is a 4-component vector.</span></span>
-   <span data-ttu-id="6211c-111">src0 est un registre source qui représente un vecteur à 3 composants.</span><span class="sxs-lookup"><span data-stu-id="6211c-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="6211c-112">src1 est un registre source qui représente une matrice 3x4, qui correspond au premier des 4 registres consécutifs.</span><span class="sxs-lookup"><span data-stu-id="6211c-112">src1 is a source register representing a 3x4 matrix, which corresponds to the first of 4 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="6211c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="6211c-113">Remarks</span></span>



| <span data-ttu-id="6211c-114">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="6211c-114">Pixel shader versions</span></span> | <span data-ttu-id="6211c-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="6211c-115">1\_1</span></span> | <span data-ttu-id="6211c-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="6211c-116">1\_2</span></span> | <span data-ttu-id="6211c-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="6211c-117">1\_3</span></span> | <span data-ttu-id="6211c-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="6211c-118">1\_4</span></span> | <span data-ttu-id="6211c-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6211c-119">2\_0</span></span> | <span data-ttu-id="6211c-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6211c-120">2\_x</span></span> | <span data-ttu-id="6211c-121">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="6211c-121">2\_sw</span></span> | <span data-ttu-id="6211c-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6211c-122">3\_0</span></span> | <span data-ttu-id="6211c-123">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="6211c-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="6211c-124">m3x4</span><span class="sxs-lookup"><span data-stu-id="6211c-124">m3x4</span></span>                  |      |      |      |      | <span data-ttu-id="6211c-125">x</span><span class="sxs-lookup"><span data-stu-id="6211c-125">x</span></span>    | <span data-ttu-id="6211c-126">x</span><span class="sxs-lookup"><span data-stu-id="6211c-126">x</span></span>    | <span data-ttu-id="6211c-127">x</span><span class="sxs-lookup"><span data-stu-id="6211c-127">x</span></span>     | <span data-ttu-id="6211c-128">x</span><span class="sxs-lookup"><span data-stu-id="6211c-128">x</span></span>    | <span data-ttu-id="6211c-129">x</span><span class="sxs-lookup"><span data-stu-id="6211c-129">x</span></span>     |



 

<span data-ttu-id="6211c-130">Le masque XYZW (par défaut) est requis pour le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="6211c-130">The xyzw (default) mask is required for the destination register.</span></span> <span data-ttu-id="6211c-131">Les modificateurs de négation et Swizzle sont autorisés pour src0, mais pas pour src1.</span><span class="sxs-lookup"><span data-stu-id="6211c-131">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="6211c-132">L’extrait de code suivant montre les opérations effectuées.</span><span class="sxs-lookup"><span data-stu-id="6211c-132">The following code snippet shows the operations performed.</span></span>


```
 
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z);
dest.z = (src0.x*src3.x) + (src0.y*src3.y) + (src0.z*src3.z);
dest.w = (src0.x*src4.x) + (src0.y*src4.y) + (src0.z*src4.z);
```



<span data-ttu-id="6211c-133">Le vecteur d’entrée se trouve dans Register src0.</span><span class="sxs-lookup"><span data-stu-id="6211c-133">The input vector is in register src0.</span></span> <span data-ttu-id="6211c-134">La matrice d’entrée 3x4 est dans Register src1, et les deux registres suivants supérieurs, comme illustré dans l’expansion ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="6211c-134">The input 3x4 matrix is in register src1, and the next two higher registers, as shown in the expansion below.</span></span>

<span data-ttu-id="6211c-135">Cette opération est couramment utilisée pour transformer un vecteur de position en une matrice qui a un effet de projet, mais qui n’applique aucune traduction.</span><span class="sxs-lookup"><span data-stu-id="6211c-135">This operation is commonly used for transforming a position vector by a matrix that has a projective effect but applies no translation.</span></span> <span data-ttu-id="6211c-136">Cette instruction est implémentée en tant que paire de produits scalaires comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="6211c-136">This instruction is implemented as a pair of dot products as shown here.</span></span>


```
m3x4   r0.xyzw, r1, c0   will be expanded to: 

dp3 r0.x, r1, c0
dp3 r0.y, r1, c1
dp3 r0.z, r1, c2
dp3 r0.w, r1, c3
```



## <a name="related-topics"></a><span data-ttu-id="6211c-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6211c-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6211c-138">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="6211c-138">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





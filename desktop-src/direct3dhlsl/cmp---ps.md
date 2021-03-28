---
title: CMP-PS
description: Choisissez src1 si src0 0. Dans le cas contraire, choisissez src2. La comparaison est effectuée par canal.
ms.assetid: 8fabd548-3f5e-4b78-bf1e-16e4f1548ccd
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: da3da1062d02e995876a1f67e5c4e19518774760
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030577"
---
# <a name="cmp---ps"></a><span data-ttu-id="a75ff-105">CMP-PS</span><span class="sxs-lookup"><span data-stu-id="a75ff-105">cmp - ps</span></span>

<span data-ttu-id="a75ff-106">Choisissez src1 si src0 >= 0.</span><span class="sxs-lookup"><span data-stu-id="a75ff-106">Choose src1 if src0 >= 0.</span></span> <span data-ttu-id="a75ff-107">Dans le cas contraire, choisissez src2.</span><span class="sxs-lookup"><span data-stu-id="a75ff-107">Otherwise, choose src2.</span></span> <span data-ttu-id="a75ff-108">La comparaison est effectuée par canal.</span><span class="sxs-lookup"><span data-stu-id="a75ff-108">The comparison is done per channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="a75ff-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a75ff-109">Syntax</span></span>



| <span data-ttu-id="a75ff-110">CMP DST, src0, src1, src2</span><span class="sxs-lookup"><span data-stu-id="a75ff-110">cmp dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="a75ff-111">where</span><span class="sxs-lookup"><span data-stu-id="a75ff-111">where</span></span>

-   <span data-ttu-id="a75ff-112">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="a75ff-112">dst is the destination register.</span></span>
-   <span data-ttu-id="a75ff-113">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="a75ff-113">src0 is a source register.</span></span>
-   <span data-ttu-id="a75ff-114">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="a75ff-114">src1 is a source register.</span></span>
-   <span data-ttu-id="a75ff-115">src2 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="a75ff-115">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="a75ff-116">Notes</span><span class="sxs-lookup"><span data-stu-id="a75ff-116">Remarks</span></span>



| <span data-ttu-id="a75ff-117">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="a75ff-117">Pixel shader versions</span></span> | <span data-ttu-id="a75ff-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="a75ff-118">1\_1</span></span> | <span data-ttu-id="a75ff-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="a75ff-119">1\_2</span></span> | <span data-ttu-id="a75ff-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="a75ff-120">1\_3</span></span> | <span data-ttu-id="a75ff-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="a75ff-121">1\_4</span></span> | <span data-ttu-id="a75ff-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a75ff-122">2\_0</span></span> | <span data-ttu-id="a75ff-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a75ff-123">2\_x</span></span> | <span data-ttu-id="a75ff-124">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="a75ff-124">2\_sw</span></span> | <span data-ttu-id="a75ff-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a75ff-125">3\_0</span></span> | <span data-ttu-id="a75ff-126">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="a75ff-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="a75ff-127">CMP</span><span class="sxs-lookup"><span data-stu-id="a75ff-127">cmp</span></span>                   |      | <span data-ttu-id="a75ff-128">x</span><span class="sxs-lookup"><span data-stu-id="a75ff-128">x</span></span>    | <span data-ttu-id="a75ff-129">x</span><span class="sxs-lookup"><span data-stu-id="a75ff-129">x</span></span>    | <span data-ttu-id="a75ff-130">x</span><span class="sxs-lookup"><span data-stu-id="a75ff-130">x</span></span>    | <span data-ttu-id="a75ff-131">x</span><span class="sxs-lookup"><span data-stu-id="a75ff-131">x</span></span>    | <span data-ttu-id="a75ff-132">x</span><span class="sxs-lookup"><span data-stu-id="a75ff-132">x</span></span>    | <span data-ttu-id="a75ff-133">x</span><span class="sxs-lookup"><span data-stu-id="a75ff-133">x</span></span>     | <span data-ttu-id="a75ff-134">x</span><span class="sxs-lookup"><span data-stu-id="a75ff-134">x</span></span>    | <span data-ttu-id="a75ff-135">x</span><span class="sxs-lookup"><span data-stu-id="a75ff-135">x</span></span>     |



 

<span data-ttu-id="a75ff-136">Il existe quelques limitations supplémentaires pour les versions 1 \_ 2 et 1 \_ 3 :</span><span class="sxs-lookup"><span data-stu-id="a75ff-136">There are a few additional limitations for versions 1\_2 and 1\_3:</span></span>

-   <span data-ttu-id="a75ff-137">Chaque nuanceur peut utiliser jusqu’à un maximum de trois instructions CMP.</span><span class="sxs-lookup"><span data-stu-id="a75ff-137">Each shader can use up to a maximum of three cmp instructions.</span></span>
-   <span data-ttu-id="a75ff-138">Le registre de destination ne peut pas être le même que l’un des registres source.</span><span class="sxs-lookup"><span data-stu-id="a75ff-138">The destination register cannot be the same as any of the source registers.</span></span>

<span data-ttu-id="a75ff-139">Cet exemple effectue une comparaison de quatre canaux.</span><span class="sxs-lookup"><span data-stu-id="a75ff-139">This example does a four-channel comparison.</span></span>


```
ps_1_4
def c0, -0.6, 0.6, 0, 0.6
def c1  0,0,0,0
def c2  1,1,1,1

mov r1, c1
mov r2, c2

cmp r0, c0, r1, r2   // r0 is assigned 1,0,0,0 based on the following:

// r0.x = c2.x because c0.x < 0
// r0.y = c1.y because c0.y >= 0
// r0.z = c1.z because c0.z >= 0
// r0.w = c1.w because c0.w >= 0
```



## <a name="related-topics"></a><span data-ttu-id="a75ff-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a75ff-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a75ff-141">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="a75ff-141">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





---
title: DP4-PS
description: Calcule le produit scalaire à quatre composants des registres sources. | DP4-PS
ms.assetid: 83ef6097-cacf-4498-842b-3eb03e57bd6f
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2562259af164b8680d54e9a120abaa405fd781c5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104043020"
---
# <a name="dp4---ps"></a><span data-ttu-id="d9434-104">DP4-PS</span><span class="sxs-lookup"><span data-stu-id="d9434-104">dp4 - ps</span></span>

<span data-ttu-id="d9434-105">Calcule le produit scalaire à quatre composants des registres sources.</span><span class="sxs-lookup"><span data-stu-id="d9434-105">Computes the four-component dot product of the source registers.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9434-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d9434-106">Syntax</span></span>



| <span data-ttu-id="d9434-107">DP4 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="d9434-107">dp4 dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="d9434-108">where</span><span class="sxs-lookup"><span data-stu-id="d9434-108">where</span></span>

-   <span data-ttu-id="d9434-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="d9434-109">dst is the destination register.</span></span>
-   <span data-ttu-id="d9434-110">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="d9434-110">src0 is a source register.</span></span>
-   <span data-ttu-id="d9434-111">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="d9434-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9434-112">Notes</span><span class="sxs-lookup"><span data-stu-id="d9434-112">Remarks</span></span>



| <span data-ttu-id="d9434-113">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="d9434-113">Pixel shader versions</span></span> | <span data-ttu-id="d9434-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="d9434-114">1\_1</span></span> | <span data-ttu-id="d9434-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="d9434-115">1\_2</span></span> | <span data-ttu-id="d9434-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="d9434-116">1\_3</span></span> | <span data-ttu-id="d9434-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="d9434-117">1\_4</span></span> | <span data-ttu-id="d9434-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d9434-118">2\_0</span></span> | <span data-ttu-id="d9434-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d9434-119">2\_x</span></span> | <span data-ttu-id="d9434-120">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="d9434-120">2\_sw</span></span> | <span data-ttu-id="d9434-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d9434-121">3\_0</span></span> | <span data-ttu-id="d9434-122">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="d9434-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="d9434-123">dp4</span><span class="sxs-lookup"><span data-stu-id="d9434-123">dp4</span></span>                   |      | <span data-ttu-id="d9434-124">x</span><span class="sxs-lookup"><span data-stu-id="d9434-124">x</span></span>    | <span data-ttu-id="d9434-125">x</span><span class="sxs-lookup"><span data-stu-id="d9434-125">x</span></span>    | <span data-ttu-id="d9434-126">x</span><span class="sxs-lookup"><span data-stu-id="d9434-126">x</span></span>    | <span data-ttu-id="d9434-127">x</span><span class="sxs-lookup"><span data-stu-id="d9434-127">x</span></span>    | <span data-ttu-id="d9434-128">x</span><span class="sxs-lookup"><span data-stu-id="d9434-128">x</span></span>    | <span data-ttu-id="d9434-129">x</span><span class="sxs-lookup"><span data-stu-id="d9434-129">x</span></span>     | <span data-ttu-id="d9434-130">x</span><span class="sxs-lookup"><span data-stu-id="d9434-130">x</span></span>    | <span data-ttu-id="d9434-131">x</span><span class="sxs-lookup"><span data-stu-id="d9434-131">x</span></span>     |



 

<span data-ttu-id="d9434-132">L’extrait de code suivant montre les opérations effectuées :</span><span class="sxs-lookup"><span data-stu-id="d9434-132">The following code snippet shows the operations performed:</span></span>


```
dest.x = dest.y = dest.z = dest.w = 
    (src0.x * src1.x) + (src0.y * src1.y) + 
    (src0.z * src1.z) + (src0.w * src1.w);
```



<span data-ttu-id="d9434-133">Limitations pour PS \_ 1 \_ 2 et PS \_ 1 \_ 3 :</span><span class="sxs-lookup"><span data-stu-id="d9434-133">Limitations for ps\_1\_2 and ps\_1\_3:</span></span>

-   <span data-ttu-id="d9434-134">Chaque nuanceur peut utiliser jusqu’à un maximum de quatre instructions DP4.</span><span class="sxs-lookup"><span data-stu-id="d9434-134">Each shader can use up to a maximum of four dp4 instructions.</span></span>
-   <span data-ttu-id="d9434-135">Chaque instruction DP4 compte comme deux instructions arithmétiques.</span><span class="sxs-lookup"><span data-stu-id="d9434-135">Each dp4 instruction counts as two arithmetic instructions.</span></span>

<span data-ttu-id="d9434-136">Limitations pour les \_ versions 1 X :</span><span class="sxs-lookup"><span data-stu-id="d9434-136">Limitations for 1\_X versions:</span></span>

-   <span data-ttu-id="d9434-137">Cette instruction ne peut pas être co-émise, car DP4 s’exécute à la fois dans le pipeline Vector et alpha.</span><span class="sxs-lookup"><span data-stu-id="d9434-137">This instruction cannot be co-issued because dp4 runs in both the vector and alpha pipeline.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9434-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d9434-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9434-139">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="d9434-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





---
title: Add-PS
description: Ajoute deux vecteurs. | Add-PS
ms.assetid: f7d29a66-879b-4160-82fd-0a1b2076559a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54092caf19a486b68b92ef63d992f11289a51c93
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113130088"
---
# <a name="add---ps"></a><span data-ttu-id="add0f-104">Add-PS</span><span class="sxs-lookup"><span data-stu-id="add0f-104">add - ps</span></span>

<span data-ttu-id="add0f-105">Ajoute deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="add0f-105">Adds two vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="add0f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="add0f-106">Syntax</span></span>



| <span data-ttu-id="add0f-107">Ajouter DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="add0f-107">add dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="add0f-108">where</span><span class="sxs-lookup"><span data-stu-id="add0f-108">where</span></span>

-   <span data-ttu-id="add0f-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="add0f-109">dst is the destination register.</span></span>
-   <span data-ttu-id="add0f-110">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="add0f-110">src0 is a source register.</span></span>
-   <span data-ttu-id="add0f-111">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="add0f-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="add0f-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="add0f-112">Remarks</span></span>



| <span data-ttu-id="add0f-113">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="add0f-113">Pixel shader versions</span></span> | <span data-ttu-id="add0f-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="add0f-114">1\_1</span></span> | <span data-ttu-id="add0f-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="add0f-115">1\_2</span></span> | <span data-ttu-id="add0f-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="add0f-116">1\_3</span></span> | <span data-ttu-id="add0f-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="add0f-117">1\_4</span></span> | <span data-ttu-id="add0f-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="add0f-118">2\_0</span></span> | <span data-ttu-id="add0f-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="add0f-119">2\_x</span></span> | <span data-ttu-id="add0f-120">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="add0f-120">2\_sw</span></span> | <span data-ttu-id="add0f-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="add0f-121">3\_0</span></span> | <span data-ttu-id="add0f-122">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="add0f-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="add0f-123">add</span><span class="sxs-lookup"><span data-stu-id="add0f-123">add</span></span>                   | <span data-ttu-id="add0f-124">x</span><span class="sxs-lookup"><span data-stu-id="add0f-124">x</span></span>    | <span data-ttu-id="add0f-125">x</span><span class="sxs-lookup"><span data-stu-id="add0f-125">x</span></span>    | <span data-ttu-id="add0f-126">x</span><span class="sxs-lookup"><span data-stu-id="add0f-126">x</span></span>    | <span data-ttu-id="add0f-127">x</span><span class="sxs-lookup"><span data-stu-id="add0f-127">x</span></span>    | <span data-ttu-id="add0f-128">x</span><span class="sxs-lookup"><span data-stu-id="add0f-128">x</span></span>    | <span data-ttu-id="add0f-129">x</span><span class="sxs-lookup"><span data-stu-id="add0f-129">x</span></span>    | <span data-ttu-id="add0f-130">x</span><span class="sxs-lookup"><span data-stu-id="add0f-130">x</span></span>     | <span data-ttu-id="add0f-131">x</span><span class="sxs-lookup"><span data-stu-id="add0f-131">x</span></span>    | <span data-ttu-id="add0f-132">x</span><span class="sxs-lookup"><span data-stu-id="add0f-132">x</span></span>     |



 

<span data-ttu-id="add0f-133">L’extrait de code suivant montre les opérations effectuées.</span><span class="sxs-lookup"><span data-stu-id="add0f-133">The following code snippet shows the operations performed.</span></span>


```
dest.x = src0.x + src1.x;
dest.y = src0.y + src1.y;
dest.z = src0.z + src1.z;
dest.w = src0.w + src1.w;
```



## <a name="instruction-information"></a><span data-ttu-id="add0f-134">Informations sur les instructions</span><span class="sxs-lookup"><span data-stu-id="add0f-134">Instruction Information</span></span>



|   <span data-ttu-id="add0f-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="add0f-135">Requirement</span></span>                       | <span data-ttu-id="add0f-136">Value</span><span class="sxs-lookup"><span data-stu-id="add0f-136">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="add0f-137">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="add0f-137">Minimum operating system</span></span> | <span data-ttu-id="add0f-138">Windows 98</span><span class="sxs-lookup"><span data-stu-id="add0f-138">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="add0f-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="add0f-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="add0f-140">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="add0f-140">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





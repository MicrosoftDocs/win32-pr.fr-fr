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
ms.openlocfilehash: f8c6ef7c14ac54610301f283d076751b0c4d4a5e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973934"
---
# <a name="add---ps"></a><span data-ttu-id="d83d9-104">Add-PS</span><span class="sxs-lookup"><span data-stu-id="d83d9-104">add - ps</span></span>

<span data-ttu-id="d83d9-105">Ajoute deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="d83d9-105">Adds two vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="d83d9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d83d9-106">Syntax</span></span>



| <span data-ttu-id="d83d9-107">Ajouter DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="d83d9-107">add dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="d83d9-108">where</span><span class="sxs-lookup"><span data-stu-id="d83d9-108">where</span></span>

-   <span data-ttu-id="d83d9-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="d83d9-109">dst is the destination register.</span></span>
-   <span data-ttu-id="d83d9-110">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="d83d9-110">src0 is a source register.</span></span>
-   <span data-ttu-id="d83d9-111">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="d83d9-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="d83d9-112">Notes</span><span class="sxs-lookup"><span data-stu-id="d83d9-112">Remarks</span></span>



| <span data-ttu-id="d83d9-113">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="d83d9-113">Pixel shader versions</span></span> | <span data-ttu-id="d83d9-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="d83d9-114">1\_1</span></span> | <span data-ttu-id="d83d9-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="d83d9-115">1\_2</span></span> | <span data-ttu-id="d83d9-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="d83d9-116">1\_3</span></span> | <span data-ttu-id="d83d9-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="d83d9-117">1\_4</span></span> | <span data-ttu-id="d83d9-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d83d9-118">2\_0</span></span> | <span data-ttu-id="d83d9-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d83d9-119">2\_x</span></span> | <span data-ttu-id="d83d9-120">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="d83d9-120">2\_sw</span></span> | <span data-ttu-id="d83d9-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d83d9-121">3\_0</span></span> | <span data-ttu-id="d83d9-122">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="d83d9-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="d83d9-123">add</span><span class="sxs-lookup"><span data-stu-id="d83d9-123">add</span></span>                   | <span data-ttu-id="d83d9-124">x</span><span class="sxs-lookup"><span data-stu-id="d83d9-124">x</span></span>    | <span data-ttu-id="d83d9-125">x</span><span class="sxs-lookup"><span data-stu-id="d83d9-125">x</span></span>    | <span data-ttu-id="d83d9-126">x</span><span class="sxs-lookup"><span data-stu-id="d83d9-126">x</span></span>    | <span data-ttu-id="d83d9-127">x</span><span class="sxs-lookup"><span data-stu-id="d83d9-127">x</span></span>    | <span data-ttu-id="d83d9-128">x</span><span class="sxs-lookup"><span data-stu-id="d83d9-128">x</span></span>    | <span data-ttu-id="d83d9-129">x</span><span class="sxs-lookup"><span data-stu-id="d83d9-129">x</span></span>    | <span data-ttu-id="d83d9-130">x</span><span class="sxs-lookup"><span data-stu-id="d83d9-130">x</span></span>     | <span data-ttu-id="d83d9-131">x</span><span class="sxs-lookup"><span data-stu-id="d83d9-131">x</span></span>    | <span data-ttu-id="d83d9-132">x</span><span class="sxs-lookup"><span data-stu-id="d83d9-132">x</span></span>     |



 

<span data-ttu-id="d83d9-133">L’extrait de code suivant montre les opérations effectuées.</span><span class="sxs-lookup"><span data-stu-id="d83d9-133">The following code snippet shows the operations performed.</span></span>


```
dest.x = src0.x + src1.x;
dest.y = src0.y + src1.y;
dest.z = src0.z + src1.z;
dest.w = src0.w + src1.w;
```



## <a name="instruction-information"></a><span data-ttu-id="d83d9-134">Informations sur les instructions</span><span class="sxs-lookup"><span data-stu-id="d83d9-134">Instruction Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="d83d9-135">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="d83d9-135">Minimum operating system</span></span> | <span data-ttu-id="d83d9-136">Windows 98</span><span class="sxs-lookup"><span data-stu-id="d83d9-136">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d83d9-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d83d9-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d83d9-138">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="d83d9-138">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





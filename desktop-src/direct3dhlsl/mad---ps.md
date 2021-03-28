---
title: Mad-PS
description: Multiplier et ajouter une instruction. Définit le registre de destination sur (src0 \ src1) + src2.
ms.assetid: 0bcf5dcc-3657-4ee0-9aeb-bd2d8feea7a6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b3570f5826f91b35b07478e1ea34940a27d706cf
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381189"
---
# <a name="mad---ps"></a><span data-ttu-id="53942-104">Mad-PS</span><span class="sxs-lookup"><span data-stu-id="53942-104">mad - ps</span></span>

<span data-ttu-id="53942-105">Multiplier et ajouter une instruction.</span><span class="sxs-lookup"><span data-stu-id="53942-105">Multiply and add instruction.</span></span> <span data-ttu-id="53942-106">Définit le registre de destination sur (src0 \* src1) + src2.</span><span class="sxs-lookup"><span data-stu-id="53942-106">Sets the destination register to (src0 \* src1) + src2.</span></span>

## <a name="syntax"></a><span data-ttu-id="53942-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53942-107">Syntax</span></span>



| <span data-ttu-id="53942-108">Mad DST, src0, src1, src2</span><span class="sxs-lookup"><span data-stu-id="53942-108">mad dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="53942-109">where</span><span class="sxs-lookup"><span data-stu-id="53942-109">where</span></span>

-   <span data-ttu-id="53942-110">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="53942-110">dst is the destination register.</span></span>
-   <span data-ttu-id="53942-111">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="53942-111">src0 is a source register.</span></span>
-   <span data-ttu-id="53942-112">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="53942-112">src1 is a source register.</span></span>
-   <span data-ttu-id="53942-113">src2 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="53942-113">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="53942-114">Notes</span><span class="sxs-lookup"><span data-stu-id="53942-114">Remarks</span></span>



| <span data-ttu-id="53942-115">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="53942-115">Pixel shader versions</span></span> | <span data-ttu-id="53942-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="53942-116">1\_1</span></span> | <span data-ttu-id="53942-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="53942-117">1\_2</span></span> | <span data-ttu-id="53942-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="53942-118">1\_3</span></span> | <span data-ttu-id="53942-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="53942-119">1\_4</span></span> | <span data-ttu-id="53942-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="53942-120">2\_0</span></span> | <span data-ttu-id="53942-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="53942-121">2\_x</span></span> | <span data-ttu-id="53942-122">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="53942-122">2\_sw</span></span> | <span data-ttu-id="53942-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="53942-123">3\_0</span></span> | <span data-ttu-id="53942-124">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="53942-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="53942-125">Mad</span><span class="sxs-lookup"><span data-stu-id="53942-125">mad</span></span>                   | <span data-ttu-id="53942-126">x</span><span class="sxs-lookup"><span data-stu-id="53942-126">x</span></span>    | <span data-ttu-id="53942-127">x</span><span class="sxs-lookup"><span data-stu-id="53942-127">x</span></span>    | <span data-ttu-id="53942-128">x</span><span class="sxs-lookup"><span data-stu-id="53942-128">x</span></span>    | <span data-ttu-id="53942-129">x</span><span class="sxs-lookup"><span data-stu-id="53942-129">x</span></span>    | <span data-ttu-id="53942-130">x</span><span class="sxs-lookup"><span data-stu-id="53942-130">x</span></span>    | <span data-ttu-id="53942-131">x</span><span class="sxs-lookup"><span data-stu-id="53942-131">x</span></span>    | <span data-ttu-id="53942-132">x</span><span class="sxs-lookup"><span data-stu-id="53942-132">x</span></span>     | <span data-ttu-id="53942-133">x</span><span class="sxs-lookup"><span data-stu-id="53942-133">x</span></span>    | <span data-ttu-id="53942-134">x</span><span class="sxs-lookup"><span data-stu-id="53942-134">x</span></span>     |



 

<span data-ttu-id="53942-135">L’extrait de code suivant montre les opérations effectuées.</span><span class="sxs-lookup"><span data-stu-id="53942-135">The following code snippet shows the operations performed.</span></span>


```
dest.x = src0.x * src1.x + src2.x;
dest.y = src0.y * src1.y + src2.y;
dest.z = src0.z * src1.z + src2.z;
dest.w = src0.w * src1.w + src2.w;
```



## <a name="related-topics"></a><span data-ttu-id="53942-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="53942-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53942-137">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="53942-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





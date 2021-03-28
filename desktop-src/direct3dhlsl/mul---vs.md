---
title: Mul-vs
description: Multiplie les sources dans la destination. | Mul-vs
ms.assetid: 0b048cc2-b165-418f-893e-6dee28ca5ad3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e33ac35831b19f771f4f5b64d94bcc47c6657db5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991965"
---
# <a name="mul---vs"></a><span data-ttu-id="9ed4c-104">Mul-vs</span><span class="sxs-lookup"><span data-stu-id="9ed4c-104">mul - vs</span></span>

<span data-ttu-id="9ed4c-105">Multiplie les sources dans la destination.</span><span class="sxs-lookup"><span data-stu-id="9ed4c-105">Multiplies sources into the destination.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ed4c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ed4c-106">Syntax</span></span>



| <span data-ttu-id="9ed4c-107">Mul DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="9ed4c-107">mul dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="9ed4c-108">where</span><span class="sxs-lookup"><span data-stu-id="9ed4c-108">where</span></span>

-   <span data-ttu-id="9ed4c-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="9ed4c-109">dst is the destination register.</span></span>
-   <span data-ttu-id="9ed4c-110">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="9ed4c-110">src0 is a source register.</span></span>
-   <span data-ttu-id="9ed4c-111">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="9ed4c-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ed4c-112">Notes</span><span class="sxs-lookup"><span data-stu-id="9ed4c-112">Remarks</span></span>



| <span data-ttu-id="9ed4c-113">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="9ed4c-113">Vertex shader versions</span></span> | <span data-ttu-id="9ed4c-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="9ed4c-114">1\_1</span></span> | <span data-ttu-id="9ed4c-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9ed4c-115">2\_0</span></span> | <span data-ttu-id="9ed4c-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9ed4c-116">2\_x</span></span> | <span data-ttu-id="9ed4c-117">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="9ed4c-117">2\_sw</span></span> | <span data-ttu-id="9ed4c-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9ed4c-118">3\_0</span></span> | <span data-ttu-id="9ed4c-119">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="9ed4c-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="9ed4c-120">mul</span><span class="sxs-lookup"><span data-stu-id="9ed4c-120">mul</span></span>                    | <span data-ttu-id="9ed4c-121">x</span><span class="sxs-lookup"><span data-stu-id="9ed4c-121">x</span></span>    | <span data-ttu-id="9ed4c-122">x</span><span class="sxs-lookup"><span data-stu-id="9ed4c-122">x</span></span>    | <span data-ttu-id="9ed4c-123">x</span><span class="sxs-lookup"><span data-stu-id="9ed4c-123">x</span></span>    | <span data-ttu-id="9ed4c-124">x</span><span class="sxs-lookup"><span data-stu-id="9ed4c-124">x</span></span>     | <span data-ttu-id="9ed4c-125">x</span><span class="sxs-lookup"><span data-stu-id="9ed4c-125">x</span></span>    | <span data-ttu-id="9ed4c-126">x</span><span class="sxs-lookup"><span data-stu-id="9ed4c-126">x</span></span>     |



 

<span data-ttu-id="9ed4c-127">Le fragment de code suivant montre les opérations effectuées.</span><span class="sxs-lookup"><span data-stu-id="9ed4c-127">The following code fragment shows the operations performed.</span></span>


```
dest.x = src0.x * src1.x;
dest.y = src0.y * src1.y;
dest.z = src0.z * src1.z;
dest.w = src0.w * src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="9ed4c-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9ed4c-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ed4c-129">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="9ed4c-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





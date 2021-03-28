---
title: Max-vs
description: Calcule le nombre maximal de sources. | Max-vs
ms.assetid: 93fb8fb2-c722-43e5-bfe4-a2e9d3cd2049
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 923da795210fe2be62a6dd84a53f0127fef21077
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974246"
---
# <a name="max---vs"></a><span data-ttu-id="00682-104">Max-vs</span><span class="sxs-lookup"><span data-stu-id="00682-104">max - vs</span></span>

<span data-ttu-id="00682-105">Calcule le nombre maximal de sources.</span><span class="sxs-lookup"><span data-stu-id="00682-105">Calculates the maximum of the sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="00682-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00682-106">Syntax</span></span>



| <span data-ttu-id="00682-107">DST Max, src0, src1</span><span class="sxs-lookup"><span data-stu-id="00682-107">max dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="00682-108">where</span><span class="sxs-lookup"><span data-stu-id="00682-108">where</span></span>

-   <span data-ttu-id="00682-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="00682-109">dst is the destination register.</span></span>
-   <span data-ttu-id="00682-110">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="00682-110">src0 is a source register.</span></span>
-   <span data-ttu-id="00682-111">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="00682-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="00682-112">Notes</span><span class="sxs-lookup"><span data-stu-id="00682-112">Remarks</span></span>



| <span data-ttu-id="00682-113">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="00682-113">Vertex shader versions</span></span> | <span data-ttu-id="00682-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="00682-114">1\_1</span></span> | <span data-ttu-id="00682-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="00682-115">2\_0</span></span> | <span data-ttu-id="00682-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="00682-116">2\_x</span></span> | <span data-ttu-id="00682-117">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="00682-117">2\_sw</span></span> | <span data-ttu-id="00682-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="00682-118">3\_0</span></span> | <span data-ttu-id="00682-119">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="00682-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="00682-120">max</span><span class="sxs-lookup"><span data-stu-id="00682-120">max</span></span>                    | <span data-ttu-id="00682-121">x</span><span class="sxs-lookup"><span data-stu-id="00682-121">x</span></span>    | <span data-ttu-id="00682-122">x</span><span class="sxs-lookup"><span data-stu-id="00682-122">x</span></span>    | <span data-ttu-id="00682-123">x</span><span class="sxs-lookup"><span data-stu-id="00682-123">x</span></span>    | <span data-ttu-id="00682-124">x</span><span class="sxs-lookup"><span data-stu-id="00682-124">x</span></span>     | <span data-ttu-id="00682-125">x</span><span class="sxs-lookup"><span data-stu-id="00682-125">x</span></span>    | <span data-ttu-id="00682-126">x</span><span class="sxs-lookup"><span data-stu-id="00682-126">x</span></span>     |



 

<span data-ttu-id="00682-127">Le fragment de code suivant montre les opérations effectuées.</span><span class="sxs-lookup"><span data-stu-id="00682-127">The following code fragment shows the operations performed.</span></span>


```
dest.x=(src0.x >= src1.x) ? src0.x : src1.x;
dest.y=(src0.y >= src1.y) ? src0.y : src1.y;
dest.z=(src0.z >= src1.z) ? src0.z : src1.z;
dest.w=(src0.w >= src1.w) ? src0.w : src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="00682-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="00682-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00682-129">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="00682-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





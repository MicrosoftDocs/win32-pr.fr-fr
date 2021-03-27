---
title: Ajouter-vs
description: Ajoute deux vecteurs. | Ajouter-vs
ms.assetid: f66d3264-68be-4a4f-84fc-cc0f6c4245c9
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 678e7f815a819be2abf1d985516fe081d3c09c94
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869697"
---
# <a name="add---vs"></a><span data-ttu-id="fc40b-104">Ajouter-vs</span><span class="sxs-lookup"><span data-stu-id="fc40b-104">add - vs</span></span>

<span data-ttu-id="fc40b-105">Ajoute deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="fc40b-105">Adds two vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc40b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc40b-106">Syntax</span></span>



| <span data-ttu-id="fc40b-107">Ajouter DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="fc40b-107">add dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="fc40b-108">where</span><span class="sxs-lookup"><span data-stu-id="fc40b-108">where</span></span>

-   <span data-ttu-id="fc40b-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="fc40b-109">dst is the destination register.</span></span>
-   <span data-ttu-id="fc40b-110">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="fc40b-110">src0 is a source register.</span></span>
-   <span data-ttu-id="fc40b-111">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="fc40b-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc40b-112">Notes</span><span class="sxs-lookup"><span data-stu-id="fc40b-112">Remarks</span></span>



| <span data-ttu-id="fc40b-113">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="fc40b-113">Vertex shader versions</span></span> | <span data-ttu-id="fc40b-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="fc40b-114">1\_1</span></span> | <span data-ttu-id="fc40b-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fc40b-115">2\_0</span></span> | <span data-ttu-id="fc40b-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="fc40b-116">2\_x</span></span> | <span data-ttu-id="fc40b-117">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="fc40b-117">2\_sw</span></span> | <span data-ttu-id="fc40b-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fc40b-118">3\_0</span></span> | <span data-ttu-id="fc40b-119">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="fc40b-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="fc40b-120">add</span><span class="sxs-lookup"><span data-stu-id="fc40b-120">add</span></span>                    | <span data-ttu-id="fc40b-121">x</span><span class="sxs-lookup"><span data-stu-id="fc40b-121">x</span></span>    | <span data-ttu-id="fc40b-122">x</span><span class="sxs-lookup"><span data-stu-id="fc40b-122">x</span></span>    | <span data-ttu-id="fc40b-123">x</span><span class="sxs-lookup"><span data-stu-id="fc40b-123">x</span></span>    | <span data-ttu-id="fc40b-124">x</span><span class="sxs-lookup"><span data-stu-id="fc40b-124">x</span></span>     | <span data-ttu-id="fc40b-125">x</span><span class="sxs-lookup"><span data-stu-id="fc40b-125">x</span></span>    | <span data-ttu-id="fc40b-126">x</span><span class="sxs-lookup"><span data-stu-id="fc40b-126">x</span></span>     |



 

<span data-ttu-id="fc40b-127">Le fragment de code suivant montre les opérations effectuées.</span><span class="sxs-lookup"><span data-stu-id="fc40b-127">The following code fragment shows the operations performed.</span></span>


```
dest.x = src0.x + src1.x;
dest.y = src0.y + src1.y;
dest.z = src0.z + src1.z;
dest.w = src0.w + src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="fc40b-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fc40b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc40b-129">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="fc40b-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





---
title: min-PS
description: Calcule la valeur minimale des sources. | min-PS
ms.assetid: 2ee6208d-a353-4747-8037-c21dd1a05016
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3a735b38769a30e9dccf544785d931641469f5dc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974155"
---
# <a name="min---ps"></a><span data-ttu-id="bd35f-104">min-PS</span><span class="sxs-lookup"><span data-stu-id="bd35f-104">min - ps</span></span>

<span data-ttu-id="bd35f-105">Calcule la valeur minimale des sources.</span><span class="sxs-lookup"><span data-stu-id="bd35f-105">Calculates the minimum of the sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd35f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bd35f-106">Syntax</span></span>



| <span data-ttu-id="bd35f-107">heure d’été min, src0, src1</span><span class="sxs-lookup"><span data-stu-id="bd35f-107">min dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="bd35f-108">where</span><span class="sxs-lookup"><span data-stu-id="bd35f-108">where</span></span>

-   <span data-ttu-id="bd35f-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="bd35f-109">dst is the destination register.</span></span>
-   <span data-ttu-id="bd35f-110">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="bd35f-110">src0 is a source register.</span></span>
-   <span data-ttu-id="bd35f-111">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="bd35f-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd35f-112">Notes</span><span class="sxs-lookup"><span data-stu-id="bd35f-112">Remarks</span></span>



| <span data-ttu-id="bd35f-113">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="bd35f-113">Pixel shader versions</span></span> | <span data-ttu-id="bd35f-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="bd35f-114">1\_1</span></span> | <span data-ttu-id="bd35f-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="bd35f-115">1\_2</span></span> | <span data-ttu-id="bd35f-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="bd35f-116">1\_3</span></span> | <span data-ttu-id="bd35f-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="bd35f-117">1\_4</span></span> | <span data-ttu-id="bd35f-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bd35f-118">2\_0</span></span> | <span data-ttu-id="bd35f-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="bd35f-119">2\_x</span></span> | <span data-ttu-id="bd35f-120">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="bd35f-120">2\_sw</span></span> | <span data-ttu-id="bd35f-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bd35f-121">3\_0</span></span> | <span data-ttu-id="bd35f-122">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="bd35f-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="bd35f-123">minute(s)</span><span class="sxs-lookup"><span data-stu-id="bd35f-123">min</span></span>                   |      |      |      |      | <span data-ttu-id="bd35f-124">x</span><span class="sxs-lookup"><span data-stu-id="bd35f-124">x</span></span>    | <span data-ttu-id="bd35f-125">x</span><span class="sxs-lookup"><span data-stu-id="bd35f-125">x</span></span>    | <span data-ttu-id="bd35f-126">x</span><span class="sxs-lookup"><span data-stu-id="bd35f-126">x</span></span>     | <span data-ttu-id="bd35f-127">x</span><span class="sxs-lookup"><span data-stu-id="bd35f-127">x</span></span>    | <span data-ttu-id="bd35f-128">x</span><span class="sxs-lookup"><span data-stu-id="bd35f-128">x</span></span>     |



 

<span data-ttu-id="bd35f-129">L’extrait de code suivant montre les opérations effectuées.</span><span class="sxs-lookup"><span data-stu-id="bd35f-129">The following code snippet shows the operations performed.</span></span>


```
dest.x=(src0.x < src1.x) ? src0.x : src1.x;
dest.y=(src0.y < src1.y) ? src0.y : src1.y;
dest.z=(src0.z < src1.z) ? src0.z : src1.z;
dest.w=(src0.w < src1.w) ? src0.w : src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="bd35f-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bd35f-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd35f-131">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="bd35f-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





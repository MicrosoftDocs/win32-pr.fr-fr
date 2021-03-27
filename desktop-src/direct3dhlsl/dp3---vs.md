---
title: DP3-vs
description: Calcule le produit scalaire à trois composants des registres sources. | DP3-vs
ms.assetid: a5263a18-ed53-41eb-85ca-2cff872e03d8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 81580401f25ddcf7ce1c1d53475d0c3beba74a89
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211375"
---
# <a name="dp3---vs"></a><span data-ttu-id="5ab25-104">DP3-vs</span><span class="sxs-lookup"><span data-stu-id="5ab25-104">dp3 - vs</span></span>

<span data-ttu-id="5ab25-105">Calcule le produit scalaire à trois composants des registres sources.</span><span class="sxs-lookup"><span data-stu-id="5ab25-105">Computes the three-component dot product of the source registers.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ab25-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ab25-106">Syntax</span></span>



| <span data-ttu-id="5ab25-107">DP3 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="5ab25-107">dp3 dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="5ab25-108">where</span><span class="sxs-lookup"><span data-stu-id="5ab25-108">where</span></span>

-   <span data-ttu-id="5ab25-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="5ab25-109">dst is the destination register.</span></span>
-   <span data-ttu-id="5ab25-110">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="5ab25-110">src0 is a source register.</span></span>
-   <span data-ttu-id="5ab25-111">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="5ab25-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ab25-112">Notes</span><span class="sxs-lookup"><span data-stu-id="5ab25-112">Remarks</span></span>



| <span data-ttu-id="5ab25-113">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="5ab25-113">Vertex shader versions</span></span> | <span data-ttu-id="5ab25-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="5ab25-114">1\_1</span></span> | <span data-ttu-id="5ab25-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5ab25-115">2\_0</span></span> | <span data-ttu-id="5ab25-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5ab25-116">2\_x</span></span> | <span data-ttu-id="5ab25-117">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="5ab25-117">2\_sw</span></span> | <span data-ttu-id="5ab25-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5ab25-118">3\_0</span></span> | <span data-ttu-id="5ab25-119">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="5ab25-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="5ab25-120">dp3</span><span class="sxs-lookup"><span data-stu-id="5ab25-120">dp3</span></span>                    | <span data-ttu-id="5ab25-121">x</span><span class="sxs-lookup"><span data-stu-id="5ab25-121">x</span></span>    | <span data-ttu-id="5ab25-122">x</span><span class="sxs-lookup"><span data-stu-id="5ab25-122">x</span></span>    | <span data-ttu-id="5ab25-123">x</span><span class="sxs-lookup"><span data-stu-id="5ab25-123">x</span></span>    | <span data-ttu-id="5ab25-124">x</span><span class="sxs-lookup"><span data-stu-id="5ab25-124">x</span></span>     | <span data-ttu-id="5ab25-125">x</span><span class="sxs-lookup"><span data-stu-id="5ab25-125">x</span></span>    | <span data-ttu-id="5ab25-126">x</span><span class="sxs-lookup"><span data-stu-id="5ab25-126">x</span></span>     |



 

<span data-ttu-id="5ab25-127">Le fragment de code suivant montre les opérations effectuées :</span><span class="sxs-lookup"><span data-stu-id="5ab25-127">The following code fragment shows the operations performed:</span></span>


```
dest.w = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.x = dest.y = dest.z = dest.w;
```



## <a name="related-topics"></a><span data-ttu-id="5ab25-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5ab25-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ab25-129">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="5ab25-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





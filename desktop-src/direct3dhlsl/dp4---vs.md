---
title: DP4-vs
description: Calcule le produit scalaire à quatre composants des registres sources. | DP4-vs
ms.assetid: ee3d3c8d-6031-4264-80ba-2b200a721310
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 747695436094dd5d2e9787e3eeca525b292f14c4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974074"
---
# <a name="dp4---vs"></a><span data-ttu-id="a6120-104">DP4-vs</span><span class="sxs-lookup"><span data-stu-id="a6120-104">dp4 - vs</span></span>

<span data-ttu-id="a6120-105">Calcule le produit scalaire à quatre composants des registres sources.</span><span class="sxs-lookup"><span data-stu-id="a6120-105">Computes the four-component dot product of the source registers.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6120-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a6120-106">Syntax</span></span>



| <span data-ttu-id="a6120-107">DP4 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="a6120-107">dp4 dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="a6120-108">where</span><span class="sxs-lookup"><span data-stu-id="a6120-108">where</span></span>

-   <span data-ttu-id="a6120-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="a6120-109">dst is the destination register.</span></span>
-   <span data-ttu-id="a6120-110">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="a6120-110">src0 is a source register.</span></span>
-   <span data-ttu-id="a6120-111">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="a6120-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6120-112">Notes</span><span class="sxs-lookup"><span data-stu-id="a6120-112">Remarks</span></span>



| <span data-ttu-id="a6120-113">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="a6120-113">Vertex shader versions</span></span> | <span data-ttu-id="a6120-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="a6120-114">1\_1</span></span> | <span data-ttu-id="a6120-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a6120-115">2\_0</span></span> | <span data-ttu-id="a6120-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a6120-116">2\_x</span></span> | <span data-ttu-id="a6120-117">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="a6120-117">2\_sw</span></span> | <span data-ttu-id="a6120-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a6120-118">3\_0</span></span> | <span data-ttu-id="a6120-119">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="a6120-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="a6120-120">dp4</span><span class="sxs-lookup"><span data-stu-id="a6120-120">dp4</span></span>                    | <span data-ttu-id="a6120-121">x</span><span class="sxs-lookup"><span data-stu-id="a6120-121">x</span></span>    | <span data-ttu-id="a6120-122">x</span><span class="sxs-lookup"><span data-stu-id="a6120-122">x</span></span>    | <span data-ttu-id="a6120-123">x</span><span class="sxs-lookup"><span data-stu-id="a6120-123">x</span></span>    | <span data-ttu-id="a6120-124">x</span><span class="sxs-lookup"><span data-stu-id="a6120-124">x</span></span>     | <span data-ttu-id="a6120-125">x</span><span class="sxs-lookup"><span data-stu-id="a6120-125">x</span></span>    | <span data-ttu-id="a6120-126">x</span><span class="sxs-lookup"><span data-stu-id="a6120-126">x</span></span>     |



 

<span data-ttu-id="a6120-127">Le fragment de code suivant montre les opérations effectuées :</span><span class="sxs-lookup"><span data-stu-id="a6120-127">The following code fragment shows the operations performed:</span></span>


```
dest.w = (src0.x * src1.x) + (src0.y * src1.y) + 
         (src0.z * src1.z) + (src0.w * src1.w);
dest.x = dest.y = dest.z = dest.w;
```



## <a name="related-topics"></a><span data-ttu-id="a6120-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a6120-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6120-129">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="a6120-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





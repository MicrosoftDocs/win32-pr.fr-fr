---
title: SGE-vs
description: Calcule le signe si la première source est supérieure ou égale à la deuxième source.
ms.assetid: 88e8eb68-8189-40c3-b20e-f395576f5f6a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7bad8816b87a32c5f10c73df27beb3cc2aef7716
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381179"
---
# <a name="sge---vs"></a><span data-ttu-id="75f45-103">SGE-vs</span><span class="sxs-lookup"><span data-stu-id="75f45-103">sge - vs</span></span>

<span data-ttu-id="75f45-104">Calcule le signe si la première source est supérieure ou égale à la deuxième source.</span><span class="sxs-lookup"><span data-stu-id="75f45-104">Computes the sign if the first source is greater than or equal to the second source.</span></span>

## <a name="syntax"></a><span data-ttu-id="75f45-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75f45-105">Syntax</span></span>



| <span data-ttu-id="75f45-106">SGE DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="75f45-106">sge dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="75f45-107">where</span><span class="sxs-lookup"><span data-stu-id="75f45-107">where</span></span>

-   <span data-ttu-id="75f45-108">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="75f45-108">dst is the destination register.</span></span>
-   <span data-ttu-id="75f45-109">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="75f45-109">src0 is a source register.</span></span>
-   <span data-ttu-id="75f45-110">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="75f45-110">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="75f45-111">Notes</span><span class="sxs-lookup"><span data-stu-id="75f45-111">Remarks</span></span>



| <span data-ttu-id="75f45-112">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="75f45-112">Vertex shader versions</span></span> | <span data-ttu-id="75f45-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="75f45-113">1\_1</span></span> | <span data-ttu-id="75f45-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="75f45-114">2\_0</span></span> | <span data-ttu-id="75f45-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="75f45-115">2\_x</span></span> | <span data-ttu-id="75f45-116">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="75f45-116">2\_sw</span></span> | <span data-ttu-id="75f45-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="75f45-117">3\_0</span></span> | <span data-ttu-id="75f45-118">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="75f45-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="75f45-119">sge</span><span class="sxs-lookup"><span data-stu-id="75f45-119">sge</span></span>                    | <span data-ttu-id="75f45-120">x</span><span class="sxs-lookup"><span data-stu-id="75f45-120">x</span></span>    | <span data-ttu-id="75f45-121">x</span><span class="sxs-lookup"><span data-stu-id="75f45-121">x</span></span>    | <span data-ttu-id="75f45-122">x</span><span class="sxs-lookup"><span data-stu-id="75f45-122">x</span></span>    | <span data-ttu-id="75f45-123">x</span><span class="sxs-lookup"><span data-stu-id="75f45-123">x</span></span>     | <span data-ttu-id="75f45-124">x</span><span class="sxs-lookup"><span data-stu-id="75f45-124">x</span></span>    | <span data-ttu-id="75f45-125">x</span><span class="sxs-lookup"><span data-stu-id="75f45-125">x</span></span>     |



 

<span data-ttu-id="75f45-126">Le fragment de code suivant montre les opérations effectuées.</span><span class="sxs-lookup"><span data-stu-id="75f45-126">The following code fragment shows the operations performed.</span></span>


```
 
dest.x = (src0.x >= src1.x) ? 1.0f : 0.0f;
dest.y = (src0.y >= src1.y) ? 1.0f : 0.0f;
dest.z = (src0.z >= src1.z) ? 1.0f : 0.0f;
dest.w = (src0.w >= src1.w) ? 1.0f : 0.0f;
```



## <a name="related-topics"></a><span data-ttu-id="75f45-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="75f45-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75f45-128">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="75f45-128">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





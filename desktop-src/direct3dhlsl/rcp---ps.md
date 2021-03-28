---
title: RCP-PS
description: Calcule la réciproque du scalaire source. | RCP-PS
ms.assetid: d8dfc2b3-4404-47ec-aeaf-1adb7e7a342e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2df8ad2d673d96dced84630b1a641c7e4f27ceb2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974238"
---
# <a name="rcp---ps"></a><span data-ttu-id="f9fdb-104">RCP-PS</span><span class="sxs-lookup"><span data-stu-id="f9fdb-104">rcp - ps</span></span>

<span data-ttu-id="f9fdb-105">Calcule la réciproque du scalaire source.</span><span class="sxs-lookup"><span data-stu-id="f9fdb-105">Computes the reciprocal of the source scalar.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9fdb-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9fdb-106">Syntax</span></span>



| <span data-ttu-id="f9fdb-107">RCP DST, SRC</span><span class="sxs-lookup"><span data-stu-id="f9fdb-107">rcp dst, src</span></span> |
|--------------|



 

<span data-ttu-id="f9fdb-108">where</span><span class="sxs-lookup"><span data-stu-id="f9fdb-108">where</span></span>

-   <span data-ttu-id="f9fdb-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="f9fdb-109">dst is the destination register.</span></span>
-   <span data-ttu-id="f9fdb-110">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="f9fdb-110">src is a source register.</span></span> <span data-ttu-id="f9fdb-111">Le registre source nécessite l’utilisation explicite de Swizzle répliqués, c’est-à-dire qu’exactement l’un des composants. x,. y,. z,. w Swizzle (ou. r,. g,. b,. a équivalents) doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="f9fdb-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9fdb-112">Notes</span><span class="sxs-lookup"><span data-stu-id="f9fdb-112">Remarks</span></span>



| <span data-ttu-id="f9fdb-113">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="f9fdb-113">Pixel shader versions</span></span> | <span data-ttu-id="f9fdb-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="f9fdb-114">1\_1</span></span> | <span data-ttu-id="f9fdb-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="f9fdb-115">1\_2</span></span> | <span data-ttu-id="f9fdb-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="f9fdb-116">1\_3</span></span> | <span data-ttu-id="f9fdb-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="f9fdb-117">1\_4</span></span> | <span data-ttu-id="f9fdb-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f9fdb-118">2\_0</span></span> | <span data-ttu-id="f9fdb-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f9fdb-119">2\_x</span></span> | <span data-ttu-id="f9fdb-120">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="f9fdb-120">2\_sw</span></span> | <span data-ttu-id="f9fdb-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f9fdb-121">3\_0</span></span> | <span data-ttu-id="f9fdb-122">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="f9fdb-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="f9fdb-123">rcp</span><span class="sxs-lookup"><span data-stu-id="f9fdb-123">rcp</span></span>                   |      |      |      |      | <span data-ttu-id="f9fdb-124">x</span><span class="sxs-lookup"><span data-stu-id="f9fdb-124">x</span></span>    | <span data-ttu-id="f9fdb-125">x</span><span class="sxs-lookup"><span data-stu-id="f9fdb-125">x</span></span>    | <span data-ttu-id="f9fdb-126">x</span><span class="sxs-lookup"><span data-stu-id="f9fdb-126">x</span></span>     | <span data-ttu-id="f9fdb-127">x</span><span class="sxs-lookup"><span data-stu-id="f9fdb-127">x</span></span>    | <span data-ttu-id="f9fdb-128">x</span><span class="sxs-lookup"><span data-stu-id="f9fdb-128">x</span></span>     |



 

<span data-ttu-id="f9fdb-129">La sortie doit être exactement 1,0 si l’entrée est exactement 1,0.</span><span class="sxs-lookup"><span data-stu-id="f9fdb-129">The output must be exactly 1.0 if the input is exactly 1.0.</span></span> <span data-ttu-id="f9fdb-130">Une source de 0,0 donne l’infini.</span><span class="sxs-lookup"><span data-stu-id="f9fdb-130">A source of 0.0 yields infinity.</span></span>

<span data-ttu-id="f9fdb-131">Le résultat scalaire est répliqué sur tous les canaux dans le masque d’écriture de destination.</span><span class="sxs-lookup"><span data-stu-id="f9fdb-131">The scalar result is replicated to all channels in the destination write mask.</span></span>

<span data-ttu-id="f9fdb-132">La précision doit être d’au moins 1,0/(2 ² ²) erreur absolue sur la plage (1,0, 2,0), car les implémentations courantes séparent la mantisse et l’exposant.</span><span class="sxs-lookup"><span data-stu-id="f9fdb-132">Precision should be at least 1.0/(2²²) absolute error over the range (1.0, 2.0) because common implementations will separate mantissa and exponent.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9fdb-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f9fdb-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9fdb-134">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="f9fdb-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





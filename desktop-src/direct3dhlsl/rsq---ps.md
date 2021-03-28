---
title: rsq-PS
description: Calcule la racine carrée réciproque (positive uniquement) du scalaire source. | rsq-PS
ms.assetid: deb1bd12-6347-4b1e-b21b-f3ef48da4c13
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13777810c67ba38b2c8f47f0c0db0cf9b70771ad
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974147"
---
# <a name="rsq---ps"></a><span data-ttu-id="ff792-104">rsq-PS</span><span class="sxs-lookup"><span data-stu-id="ff792-104">rsq - ps</span></span>

<span data-ttu-id="ff792-105">Calcule la racine carrée réciproque (positive uniquement) du scalaire source.</span><span class="sxs-lookup"><span data-stu-id="ff792-105">Computes the reciprocal square root (positive only) of the source scalar.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff792-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ff792-106">Syntax</span></span>



| <span data-ttu-id="ff792-107">rsq DST, SRC</span><span class="sxs-lookup"><span data-stu-id="ff792-107">rsq dst, src</span></span> |
|--------------|



 

<span data-ttu-id="ff792-108">where</span><span class="sxs-lookup"><span data-stu-id="ff792-108">where</span></span>

-   <span data-ttu-id="ff792-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="ff792-109">dst is the destination register.</span></span>
-   <span data-ttu-id="ff792-110">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="ff792-110">src is a source register.</span></span> <span data-ttu-id="ff792-111">Le registre source nécessite l’utilisation explicite de Swizzle répliqués, c’est-à-dire qu’exactement l’un des composants. x,. y,. z,. w Swizzle (ou. r,. g,. b,. a équivalents) doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="ff792-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff792-112">Notes</span><span class="sxs-lookup"><span data-stu-id="ff792-112">Remarks</span></span>



| <span data-ttu-id="ff792-113">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="ff792-113">Pixel shader versions</span></span> | <span data-ttu-id="ff792-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="ff792-114">1\_1</span></span> | <span data-ttu-id="ff792-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="ff792-115">1\_2</span></span> | <span data-ttu-id="ff792-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="ff792-116">1\_3</span></span> | <span data-ttu-id="ff792-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="ff792-117">1\_4</span></span> | <span data-ttu-id="ff792-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ff792-118">2\_0</span></span> | <span data-ttu-id="ff792-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ff792-119">2\_x</span></span> | <span data-ttu-id="ff792-120">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="ff792-120">2\_sw</span></span> | <span data-ttu-id="ff792-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ff792-121">3\_0</span></span> | <span data-ttu-id="ff792-122">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="ff792-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="ff792-123">rsq</span><span class="sxs-lookup"><span data-stu-id="ff792-123">rsq</span></span>                   |      |      |      |      | <span data-ttu-id="ff792-124">x</span><span class="sxs-lookup"><span data-stu-id="ff792-124">x</span></span>    | <span data-ttu-id="ff792-125">x</span><span class="sxs-lookup"><span data-stu-id="ff792-125">x</span></span>    | <span data-ttu-id="ff792-126">x</span><span class="sxs-lookup"><span data-stu-id="ff792-126">x</span></span>     | <span data-ttu-id="ff792-127">x</span><span class="sxs-lookup"><span data-stu-id="ff792-127">x</span></span>    | <span data-ttu-id="ff792-128">x</span><span class="sxs-lookup"><span data-stu-id="ff792-128">x</span></span>     |



 

<span data-ttu-id="ff792-129">La valeur absolue est prise avant le traitement.</span><span class="sxs-lookup"><span data-stu-id="ff792-129">The absolute value is taken before processing.</span></span>

<span data-ttu-id="ff792-130">La précision doit être d’au moins 1,0/(2 ² ²) erreur absolue sur la plage (1,0, 4,0), car les implémentations courantes séparent la mantisse et l’exposant.</span><span class="sxs-lookup"><span data-stu-id="ff792-130">Precision should be at least 1.0/(2²²) absolute error over the range (1.0, 4.0) because common implementations will separate mantissa and exponent.</span></span>

<span data-ttu-id="ff792-131">La sortie doit être exactement 1,0 si l’entrée est exactement 1,0.</span><span class="sxs-lookup"><span data-stu-id="ff792-131">The output must be exactly 1.0 if the input is exactly 1.0.</span></span> <span data-ttu-id="ff792-132">Une source de 0,0 donne l’infini.</span><span class="sxs-lookup"><span data-stu-id="ff792-132">A source of 0.0 yields infinity.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff792-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ff792-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff792-134">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="ff792-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





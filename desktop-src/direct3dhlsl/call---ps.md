---
title: appeler-PS
description: Effectue un appel de fonction à l’instruction marquée avec l’étiquette fournie. | appeler-PS
ms.assetid: d5f5e5a1-f205-477d-a11b-ff9eeeec6c95
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27be29c478afdf92c29fefd16a82319e0899d2ec
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991969"
---
# <a name="call---ps"></a><span data-ttu-id="260b3-104">appeler-PS</span><span class="sxs-lookup"><span data-stu-id="260b3-104">call - ps</span></span>

<span data-ttu-id="260b3-105">Effectue un appel de fonction à l’instruction marquée avec l’étiquette fournie.</span><span class="sxs-lookup"><span data-stu-id="260b3-105">Performs a function call to the instruction marked with the provided label.</span></span>

## <a name="syntax"></a><span data-ttu-id="260b3-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="260b3-106">Syntax</span></span>



| <span data-ttu-id="260b3-107">appeler l\#</span><span class="sxs-lookup"><span data-stu-id="260b3-107">call l\#</span></span> |
|----------|



 

<span data-ttu-id="260b3-108">Où :</span><span class="sxs-lookup"><span data-stu-id="260b3-108">Where:</span></span>

-   <span data-ttu-id="260b3-109">l \# est une [étiquette-PS](label---ps.md) qui marque le début de la sous-routine à appeler.</span><span class="sxs-lookup"><span data-stu-id="260b3-109">l\# is a [label - ps](label---ps.md) marking the beginning of the subroutine to be called.</span></span>

## <a name="remarks"></a><span data-ttu-id="260b3-110">Notes</span><span class="sxs-lookup"><span data-stu-id="260b3-110">Remarks</span></span>



| <span data-ttu-id="260b3-111">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="260b3-111">Pixel shader versions</span></span> | <span data-ttu-id="260b3-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="260b3-112">1\_1</span></span> | <span data-ttu-id="260b3-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="260b3-113">1\_2</span></span> | <span data-ttu-id="260b3-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="260b3-114">1\_3</span></span> | <span data-ttu-id="260b3-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="260b3-115">1\_4</span></span> | <span data-ttu-id="260b3-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="260b3-116">2\_0</span></span> | <span data-ttu-id="260b3-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="260b3-117">2\_x</span></span> | <span data-ttu-id="260b3-118">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="260b3-118">2\_sw</span></span> | <span data-ttu-id="260b3-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="260b3-119">3\_0</span></span> | <span data-ttu-id="260b3-120">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="260b3-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="260b3-121">appel</span><span class="sxs-lookup"><span data-stu-id="260b3-121">call</span></span>                  |      |      |      |      |      | <span data-ttu-id="260b3-122">x</span><span class="sxs-lookup"><span data-stu-id="260b3-122">x</span></span>    | <span data-ttu-id="260b3-123">x</span><span class="sxs-lookup"><span data-stu-id="260b3-123">x</span></span>     | <span data-ttu-id="260b3-124">x</span><span class="sxs-lookup"><span data-stu-id="260b3-124">x</span></span>    | <span data-ttu-id="260b3-125">x</span><span class="sxs-lookup"><span data-stu-id="260b3-125">x</span></span>     |



 

<span data-ttu-id="260b3-126">Cette instruction effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="260b3-126">This instruction does the following:</span></span>

1.  <span data-ttu-id="260b3-127">Adresse push de la prochaine instruction à la pile d’adresses de retour.</span><span class="sxs-lookup"><span data-stu-id="260b3-127">Push address of the next instruction to the return address stack.</span></span>
2.  <span data-ttu-id="260b3-128">Poursuivez l’exécution à partir de l’instruction marquée par l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="260b3-128">Continue execution from the instruction marked by the label.</span></span>

## <a name="related-topics"></a><span data-ttu-id="260b3-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="260b3-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="260b3-130">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="260b3-130">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





---
title: étiquette-PS
description: Marquer l’instruction suivante comme ayant un index d’étiquette. | étiquette-PS
ms.assetid: 21afa062-c536-4891-ba69-ca5284b0539c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3fb266b649642c82293e8310b6302c6763ddc27
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992012"
---
# <a name="label---ps"></a><span data-ttu-id="96e22-104">étiquette-PS</span><span class="sxs-lookup"><span data-stu-id="96e22-104">label - ps</span></span>

<span data-ttu-id="96e22-105">Marquer l’instruction suivante comme ayant un index d’étiquette.</span><span class="sxs-lookup"><span data-stu-id="96e22-105">Mark the next instruction as having a label index.</span></span>

## <a name="syntax"></a><span data-ttu-id="96e22-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96e22-106">Syntax</span></span>



| <span data-ttu-id="96e22-107">étiquette l\#</span><span class="sxs-lookup"><span data-stu-id="96e22-107">label l\#</span></span> |
|-----------|



 

<span data-ttu-id="96e22-108">où \# identifie le numéro de l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="96e22-108">where \# identifies the label number.</span></span>

<span data-ttu-id="96e22-109">Pour PS \_ 2 \_ x, le numéro d’étiquette doit être compris entre 0 et 15.</span><span class="sxs-lookup"><span data-stu-id="96e22-109">For ps\_2\_x, the label number must be between between 0 and 15.</span></span>

<span data-ttu-id="96e22-110">Pour les logiciels PS \_ 2 \_ , PS \_ 3 \_ 0 et PS \_ 3 \_ , le numéro d’étiquette doit être compris entre 0 et 2047.</span><span class="sxs-lookup"><span data-stu-id="96e22-110">For ps\_2\_sw, ps\_3\_0, and ps\_3\_sw, the label number must be between between 0 and 2047.</span></span>

## <a name="remarks"></a><span data-ttu-id="96e22-111">Notes</span><span class="sxs-lookup"><span data-stu-id="96e22-111">Remarks</span></span>



| <span data-ttu-id="96e22-112">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="96e22-112">Pixel shader versions</span></span> | <span data-ttu-id="96e22-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="96e22-113">1\_1</span></span> | <span data-ttu-id="96e22-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="96e22-114">1\_2</span></span> | <span data-ttu-id="96e22-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="96e22-115">1\_3</span></span> | <span data-ttu-id="96e22-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="96e22-116">1\_4</span></span> | <span data-ttu-id="96e22-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="96e22-117">2\_0</span></span> | <span data-ttu-id="96e22-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="96e22-118">2\_x</span></span> | <span data-ttu-id="96e22-119">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="96e22-119">2\_sw</span></span> | <span data-ttu-id="96e22-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="96e22-120">3\_0</span></span> | <span data-ttu-id="96e22-121">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="96e22-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="96e22-122">label</span><span class="sxs-lookup"><span data-stu-id="96e22-122">label</span></span>                 |      |      |      |      |      | <span data-ttu-id="96e22-123">x</span><span class="sxs-lookup"><span data-stu-id="96e22-123">x</span></span>    | <span data-ttu-id="96e22-124">x</span><span class="sxs-lookup"><span data-stu-id="96e22-124">x</span></span>     | <span data-ttu-id="96e22-125">x</span><span class="sxs-lookup"><span data-stu-id="96e22-125">x</span></span>    | <span data-ttu-id="96e22-126">x</span><span class="sxs-lookup"><span data-stu-id="96e22-126">x</span></span>     |



 

<span data-ttu-id="96e22-127">Cette instruction définit une étiquette située à l’instruction de nuanceur suivante.</span><span class="sxs-lookup"><span data-stu-id="96e22-127">This instruction defines a label located at the next shader instruction.</span></span> <span data-ttu-id="96e22-128">L’instruction label ne peut être présente directement qu’après une instruction [RET](ret---ps.md) (qui définit la fin de la sous-routine ou du programme principal précédent).</span><span class="sxs-lookup"><span data-stu-id="96e22-128">The label instruction can only be present directly after a [ret](ret---ps.md) instruction (which defines the end of the previous subroutine or main program).</span></span>

## <a name="related-topics"></a><span data-ttu-id="96e22-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="96e22-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96e22-130">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="96e22-130">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





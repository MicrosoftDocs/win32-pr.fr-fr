---
title: étiquette-vs
description: Marquer l’instruction suivante comme ayant un index d’étiquette. | étiquette-vs
ms.assetid: e1aee8bc-4655-4bd5-8012-bd7a2d46e712
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6e2b72fe21301aa66d8428dc3696ceb3f12e6214
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992088"
---
# <a name="label---vs"></a><span data-ttu-id="c605e-104">étiquette-vs</span><span class="sxs-lookup"><span data-stu-id="c605e-104">label - vs</span></span>

<span data-ttu-id="c605e-105">Marquer l’instruction suivante comme ayant un index d’étiquette.</span><span class="sxs-lookup"><span data-stu-id="c605e-105">Mark the next instruction as having a label index.</span></span>

## <a name="syntax"></a><span data-ttu-id="c605e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c605e-106">Syntax</span></span>



| <span data-ttu-id="c605e-107">étiquette l\#</span><span class="sxs-lookup"><span data-stu-id="c605e-107">label l\#</span></span> |
|-----------|



 

<span data-ttu-id="c605e-108">où \# identifie le numéro de l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="c605e-108">where \# identifies the label number.</span></span>

<span data-ttu-id="c605e-109">Pour vs \_ 2 \_ 0 et vs \_ 2 \_ x, le numéro d’étiquette doit être compris entre 0 et 15.</span><span class="sxs-lookup"><span data-stu-id="c605e-109">For vs\_2\_0, and vs\_2\_x, the label number must be between between 0 and 15.</span></span>

<span data-ttu-id="c605e-110">Pour vs \_ 2 \_ SW, vs \_ 3 \_ 0 et vs \_ 3 \_ SW, le numéro d’étiquette doit être compris entre 0 et 2047.</span><span class="sxs-lookup"><span data-stu-id="c605e-110">For vs\_2\_sw, vs\_3\_0 and vs\_3\_sw, the label number must be between between 0 and 2047.</span></span>

## <a name="remarks"></a><span data-ttu-id="c605e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="c605e-111">Remarks</span></span>



| <span data-ttu-id="c605e-112">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="c605e-112">Vertex shader versions</span></span> | <span data-ttu-id="c605e-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="c605e-113">1\_1</span></span> | <span data-ttu-id="c605e-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c605e-114">2\_0</span></span> | <span data-ttu-id="c605e-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c605e-115">2\_x</span></span> | <span data-ttu-id="c605e-116">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="c605e-116">2\_sw</span></span> | <span data-ttu-id="c605e-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c605e-117">3\_0</span></span> | <span data-ttu-id="c605e-118">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="c605e-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="c605e-119">label</span><span class="sxs-lookup"><span data-stu-id="c605e-119">label</span></span>                  |      | <span data-ttu-id="c605e-120">x</span><span class="sxs-lookup"><span data-stu-id="c605e-120">x</span></span>    | <span data-ttu-id="c605e-121">x</span><span class="sxs-lookup"><span data-stu-id="c605e-121">x</span></span>    | <span data-ttu-id="c605e-122">x</span><span class="sxs-lookup"><span data-stu-id="c605e-122">x</span></span>     | <span data-ttu-id="c605e-123">x</span><span class="sxs-lookup"><span data-stu-id="c605e-123">x</span></span>    | <span data-ttu-id="c605e-124">x</span><span class="sxs-lookup"><span data-stu-id="c605e-124">x</span></span>     |



 

<span data-ttu-id="c605e-125">Cette instruction définit une étiquette située à l’instruction de nuanceur suivante.</span><span class="sxs-lookup"><span data-stu-id="c605e-125">This instruction defines a label located at the next shader instruction.</span></span> <span data-ttu-id="c605e-126">L’instruction label ne peut être présente directement qu’après une instruction [RET](ret---vs.md) (qui définit la fin de la sous-routine ou du programme principal précédent).</span><span class="sxs-lookup"><span data-stu-id="c605e-126">The label instruction can only be present directly after a [ret](ret---vs.md) instruction (which defines the end of the previous subroutine or main program).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c605e-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c605e-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c605e-128">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="c605e-128">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





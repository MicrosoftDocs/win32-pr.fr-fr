---
title: appel-vs
description: Effectue un appel de fonction à l’instruction marquée avec l’étiquette fournie. | appel-vs
ms.assetid: 3c1ec529-1ee4-40d9-8ce5-f8e7a61fde9c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c797e7ef6745f5710752fe059d2a2ff1f94a8aa3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953776"
---
# <a name="call---vs"></a><span data-ttu-id="5b0d6-104">appel-vs</span><span class="sxs-lookup"><span data-stu-id="5b0d6-104">call - vs</span></span>

<span data-ttu-id="5b0d6-105">Effectue un appel de fonction à l’instruction marquée avec l’étiquette fournie.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-105">Performs a function call to the instruction marked with the provided label.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b0d6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b0d6-106">Syntax</span></span>



| <span data-ttu-id="5b0d6-107">appeler l\#</span><span class="sxs-lookup"><span data-stu-id="5b0d6-107">call l\#</span></span> |
|----------|



 

<span data-ttu-id="5b0d6-108">où l \# est une [étiquette, et](label---vs.md) qui marque le début de la sous-routine à appeler.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-108">where l\# is a [label - vs](label---vs.md) marking the beginning of the subroutine to be called.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b0d6-109">Notes</span><span class="sxs-lookup"><span data-stu-id="5b0d6-109">Remarks</span></span>



| <span data-ttu-id="5b0d6-110">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="5b0d6-110">Vertex shader versions</span></span> | <span data-ttu-id="5b0d6-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="5b0d6-111">1\_1</span></span> | <span data-ttu-id="5b0d6-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5b0d6-112">2\_0</span></span> | <span data-ttu-id="5b0d6-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5b0d6-113">2\_x</span></span> | <span data-ttu-id="5b0d6-114">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="5b0d6-114">2\_sw</span></span> | <span data-ttu-id="5b0d6-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5b0d6-115">3\_0</span></span> | <span data-ttu-id="5b0d6-116">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="5b0d6-116">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="5b0d6-117">appel</span><span class="sxs-lookup"><span data-stu-id="5b0d6-117">call</span></span>                   |      | <span data-ttu-id="5b0d6-118">x</span><span class="sxs-lookup"><span data-stu-id="5b0d6-118">x</span></span>    | <span data-ttu-id="5b0d6-119">x</span><span class="sxs-lookup"><span data-stu-id="5b0d6-119">x</span></span>    | <span data-ttu-id="5b0d6-120">x</span><span class="sxs-lookup"><span data-stu-id="5b0d6-120">x</span></span>     | <span data-ttu-id="5b0d6-121">x</span><span class="sxs-lookup"><span data-stu-id="5b0d6-121">x</span></span>    | <span data-ttu-id="5b0d6-122">x</span><span class="sxs-lookup"><span data-stu-id="5b0d6-122">x</span></span>     |



 

<span data-ttu-id="5b0d6-123">Cette instruction effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="5b0d6-123">This instruction does the following:</span></span>

1.  <span data-ttu-id="5b0d6-124">Adresse push de la prochaine instruction à la pile d’adresses de retour.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-124">Push address of the next instruction to the return address stack.</span></span>
2.  <span data-ttu-id="5b0d6-125">Poursuivez l’exécution à partir de l’instruction marquée par l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-125">Continue execution from the instruction marked by the label.</span></span>

<span data-ttu-id="5b0d6-126">Dans le nuanceur de sommets 2 \_ 0, les appels d’imbrication ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-126">In vertex shader 2\_0, nesting calls are not allowed.</span></span>

<span data-ttu-id="5b0d6-127">Dans le nuanceur de vertex 2 \_ x, la profondeur d’imbrication est limitée par l’élément StaticFlowControlDepth de la structure [**D3DVSHADERCAPS2 \_ 0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dvshadercaps2_0) .</span><span class="sxs-lookup"><span data-stu-id="5b0d6-127">In vertex shader 2\_x, the nesting depth is limited by the StaticFlowControlDepth element of the [**D3DVSHADERCAPS2\_0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dvshadercaps2_0) structure.</span></span> <span data-ttu-id="5b0d6-128">Pour plus d’informations, consultez [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps).</span><span class="sxs-lookup"><span data-stu-id="5b0d6-128">For more information, see [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps).</span></span>

<span data-ttu-id="5b0d6-129">Dans le nuanceur de sommets 3 \_ 0, quatre niveaux d’imbrication des appels sont autorisés.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-129">In vertex shader 3\_0, four levels of call nesting are allowed.</span></span>

<span data-ttu-id="5b0d6-130">Seuls les appels de transfert sont autorisés.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-130">Only forward calls are allowed.</span></span> <span data-ttu-id="5b0d6-131">Cela signifie que l’emplacement de l’étiquette dans le nuanceur de sommets doit se trouver après l’instruction call qui la référence.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-131">This means that the location of the label inside the vertex shader should be after the call instruction referencing it.</span></span>

<span data-ttu-id="5b0d6-132">Si une instruction d’appel est appelée à l’intérieur d’une [boucle](loop---vs.md)... bloc [ENDLOOP](endloop---vs.md) , la valeur du [Registre de compteur de boucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al) est accessible à l’intérieur de la sous-routine.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-132">If a call instruction is invoked inside [loop](loop---vs.md)...[endloop](endloop---vs.md) block, the value of the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) is accessible inside the subroutine.</span></span>

<span data-ttu-id="5b0d6-133">Si une sous-routine référence le [Registre de compteur de boucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al) situé en dehors de la sous-routine, chaque instance de l’appel à cette sous-routine doit être entourée d’une [boucle](loop---vs.md)... bloc [ENDLOOP](endloop---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="5b0d6-133">If a subroutine is referencing the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) located outside of the subroutine, every instance of the call to this subroutine should be surrounded by a [loop](loop---vs.md)...[endloop](endloop---vs.md) block.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b0d6-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5b0d6-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b0d6-135">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="5b0d6-135">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 

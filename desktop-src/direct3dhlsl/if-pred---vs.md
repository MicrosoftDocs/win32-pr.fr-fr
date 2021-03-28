---
title: Si prédit-vs
description: Début d’un if prédit-vs... else-vs... endif-bloc vs, avec la condition extraite du contenu du registre de prédicat.
ms.assetid: 03f60ca3-cda0-4653-8582-74d1a75e0aee
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a1a36bb0c6c68f5132757719bbc7e37fbc71501
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313636"
---
# <a name="if-pred---vs"></a><span data-ttu-id="e8e98-103">Si prédit-vs</span><span class="sxs-lookup"><span data-stu-id="e8e98-103">if pred - vs</span></span>

<span data-ttu-id="e8e98-104">Début d’un if prédit-vs... [else-vs](else---vs.md)... [endif-bloc vs](endif---vs.md) , avec la condition extraite du contenu du registre de prédicat.</span><span class="sxs-lookup"><span data-stu-id="e8e98-104">Start of an if pred - vs...[else - vs](else---vs.md)...[endif - vs](endif---vs.md) block, with the condition taken from the content of the predicate register.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8e98-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8e98-105">Syntax</span></span>



| <span data-ttu-id="e8e98-106">Si \[ ! \] prédit. replicateSwizzle</span><span class="sxs-lookup"><span data-stu-id="e8e98-106">if \[!\]pred.replicateSwizzle</span></span> |
|-------------------------------|



 

<span data-ttu-id="e8e98-107">Où :</span><span class="sxs-lookup"><span data-stu-id="e8e98-107">Where:</span></span>

-   <span data-ttu-id="e8e98-108">\[!\] modificateur NOT facultatif.</span><span class="sxs-lookup"><span data-stu-id="e8e98-108">\[!\] an optional NOT modifier.</span></span> <span data-ttu-id="e8e98-109">Cela modifie la valeur dans le registre de prédicat.</span><span class="sxs-lookup"><span data-stu-id="e8e98-109">This modifies the value in the predicate register.</span></span>
-   <span data-ttu-id="e8e98-110">prédit est le registre de prédicat, P0.</span><span class="sxs-lookup"><span data-stu-id="e8e98-110">pred is the predicate register, p0.</span></span> <span data-ttu-id="e8e98-111">Consultez [Registre de prédicat](dx9-graphics-reference-asm-vs-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="e8e98-111">See [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).</span></span>
-   <span data-ttu-id="e8e98-112">replicateSwizzle est un composant unique qui est copié (ou répliqué) sur les quatre composants (swizzled).</span><span class="sxs-lookup"><span data-stu-id="e8e98-112">replicateSwizzle is a single component that is copied (or replicated) to all four components (swizzled).</span></span> <span data-ttu-id="e8e98-113">Les composants valides sont les suivants : x, y, z, w ou r, g, b, a.</span><span class="sxs-lookup"><span data-stu-id="e8e98-113">Valid components are: x, y, z, w or r, g, b, a.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8e98-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e8e98-114">Remarks</span></span>



| <span data-ttu-id="e8e98-115">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="e8e98-115">Vertex shader versions</span></span> | <span data-ttu-id="e8e98-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="e8e98-116">1\_1</span></span> | <span data-ttu-id="e8e98-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e8e98-117">2\_0</span></span> | <span data-ttu-id="e8e98-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e8e98-118">2\_x</span></span> | <span data-ttu-id="e8e98-119">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="e8e98-119">2\_sw</span></span> | <span data-ttu-id="e8e98-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e8e98-120">3\_0</span></span> | <span data-ttu-id="e8e98-121">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="e8e98-121">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="e8e98-122">Si prédite</span><span class="sxs-lookup"><span data-stu-id="e8e98-122">if pred</span></span>                |      |      | <span data-ttu-id="e8e98-123">x</span><span class="sxs-lookup"><span data-stu-id="e8e98-123">x</span></span>    | <span data-ttu-id="e8e98-124">x</span><span class="sxs-lookup"><span data-stu-id="e8e98-124">x</span></span>     | <span data-ttu-id="e8e98-125">x</span><span class="sxs-lookup"><span data-stu-id="e8e98-125">x</span></span>    | <span data-ttu-id="e8e98-126">x</span><span class="sxs-lookup"><span data-stu-id="e8e98-126">x</span></span>     |



 

<span data-ttu-id="e8e98-127">Cette instruction est utilisée pour ignorer un bloc de code, en fonction d’un canal du registre de prédicat.</span><span class="sxs-lookup"><span data-stu-id="e8e98-127">This instruction is used to skip a block of code, based on a channel of the predicate register.</span></span> <span data-ttu-id="e8e98-128">Chaque \_ bloc si prédit doit se terminer par une instruction Else ou endif.</span><span class="sxs-lookup"><span data-stu-id="e8e98-128">Each if\_pred block must end with an else or endif instruction.</span></span>

<span data-ttu-id="e8e98-129">Les restrictions sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e8e98-129">Restrictions include:</span></span>

<span data-ttu-id="e8e98-130">Si les \_ blocs prédits peuvent être imbriqués.</span><span class="sxs-lookup"><span data-stu-id="e8e98-130">if\_pred blocks can be nested.</span></span> <span data-ttu-id="e8e98-131">Cela compte la profondeur d’imbrication dynamique totale, ainsi que [si les blocs \_ COMP sont](if-comp---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="e8e98-131">This counts to the total dynamic nesting depth along with [if\_comp](if-comp---vs.md) blocks.</span></span>

<span data-ttu-id="e8e98-132">Un \_ bloc si prédit ne peut pas chevaucher un bloc de boucle, il doit l’être entièrement à l’intérieur ou l’entourer.</span><span class="sxs-lookup"><span data-stu-id="e8e98-132">An if\_pred block cannot straddle a loop block, it should be either completely inside it or surround it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8e98-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e8e98-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8e98-134">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="e8e98-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





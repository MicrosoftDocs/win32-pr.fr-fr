---
title: Si prédit-PS
description: Début d’une si bool-PS... else-PS... endif-bloc PS, avec la condition extraite du contenu du registre de prédicat.
ms.assetid: 7b43bf71-a2e9-468f-805f-620de065db08
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ead7c5936550715d48ee1ef6a3938b6219558823
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679117"
---
# <a name="if-pred---ps"></a><span data-ttu-id="781ea-103">Si prédit-PS</span><span class="sxs-lookup"><span data-stu-id="781ea-103">if pred - ps</span></span>

<span data-ttu-id="781ea-104">Début d’une [si bool-PS](if-bool---ps.md)... [else-PS](else---ps.md)... [endif-bloc PS](endif---ps.md) , avec la condition extraite du contenu du registre de prédicat.</span><span class="sxs-lookup"><span data-stu-id="781ea-104">Start of an [if bool - ps](if-bool---ps.md)...[else - ps](else---ps.md)...[endif - ps](endif---ps.md) block, with the condition taken from the content of the predicate register.</span></span>

## <a name="syntax"></a><span data-ttu-id="781ea-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="781ea-105">Syntax</span></span>



| <span data-ttu-id="781ea-106">Si \[ ! \] prédit. replicateSwizzle</span><span class="sxs-lookup"><span data-stu-id="781ea-106">if \[!\]pred.replicateSwizzle</span></span> |
|-------------------------------|



 

<span data-ttu-id="781ea-107">Où :</span><span class="sxs-lookup"><span data-stu-id="781ea-107">Where:</span></span>

-   <span data-ttu-id="781ea-108">\[!\] est un modificateur NOT facultatif.</span><span class="sxs-lookup"><span data-stu-id="781ea-108">\[!\] is an optional NOT modifier.</span></span> <span data-ttu-id="781ea-109">Cela modifie la valeur dans le registre de prédicat.</span><span class="sxs-lookup"><span data-stu-id="781ea-109">This modifies the value in the predicate register.</span></span>
-   <span data-ttu-id="781ea-110">prédit est l' [enregistrement de prédicat](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="781ea-110">pred is the [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>
-   <span data-ttu-id="781ea-111">replicateSwizzle est un composant unique qui est copié (ou répliqué) sur les quatre composants (swizzled).</span><span class="sxs-lookup"><span data-stu-id="781ea-111">replicateSwizzle is a single component that is copied (or replicated) to all four components (swizzled).</span></span> <span data-ttu-id="781ea-112">Les composants valides sont les suivants : \[ x, y, z, w \] ou \[ r, g, b, a \] .</span><span class="sxs-lookup"><span data-stu-id="781ea-112">Valid components are: \[x, y, z, w\] or \[r, g, b, a\].</span></span>

## <a name="remarks"></a><span data-ttu-id="781ea-113">Notes</span><span class="sxs-lookup"><span data-stu-id="781ea-113">Remarks</span></span>



| <span data-ttu-id="781ea-114">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="781ea-114">Pixel shader versions</span></span> | <span data-ttu-id="781ea-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="781ea-115">1\_1</span></span> | <span data-ttu-id="781ea-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="781ea-116">1\_2</span></span> | <span data-ttu-id="781ea-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="781ea-117">1\_3</span></span> | <span data-ttu-id="781ea-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="781ea-118">1\_4</span></span> | <span data-ttu-id="781ea-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="781ea-119">2\_0</span></span> | <span data-ttu-id="781ea-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="781ea-120">2\_x</span></span> | <span data-ttu-id="781ea-121">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="781ea-121">2\_sw</span></span> | <span data-ttu-id="781ea-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="781ea-122">3\_0</span></span> | <span data-ttu-id="781ea-123">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="781ea-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="781ea-124">Si \_ prédite</span><span class="sxs-lookup"><span data-stu-id="781ea-124">if\_pred</span></span>              |      |      |      |      |      | <span data-ttu-id="781ea-125">x</span><span class="sxs-lookup"><span data-stu-id="781ea-125">x</span></span>    | <span data-ttu-id="781ea-126">x</span><span class="sxs-lookup"><span data-stu-id="781ea-126">x</span></span>     | <span data-ttu-id="781ea-127">x</span><span class="sxs-lookup"><span data-stu-id="781ea-127">x</span></span>    | <span data-ttu-id="781ea-128">x</span><span class="sxs-lookup"><span data-stu-id="781ea-128">x</span></span>     |



 

<span data-ttu-id="781ea-129">Cette instruction est utilisée pour ignorer un bloc de code, en fonction d’un canal du registre de prédicat.</span><span class="sxs-lookup"><span data-stu-id="781ea-129">This instruction is used to skip a block of code, based on a channel of the predicate register.</span></span> <span data-ttu-id="781ea-130">Chaque \_ bloc si prédit doit se terminer par une instruction [else-PS](else---ps.md) ou [endif-PS](endif---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="781ea-130">Each if\_pred block must end with an [else - ps](else---ps.md) or [endif - ps](endif---ps.md) instruction.</span></span>

<span data-ttu-id="781ea-131">Les restrictions sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="781ea-131">Restrictions include:</span></span>

<span data-ttu-id="781ea-132">Si les \_ blocs prédits peuvent être imbriqués.</span><span class="sxs-lookup"><span data-stu-id="781ea-132">if\_pred blocks can be nested.</span></span> <span data-ttu-id="781ea-133">Cela compte la profondeur d’imbrication dynamique totale, ainsi que [si les blocs \_ COMP sont](if-comp---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="781ea-133">This counts to the total dynamic nesting depth along with [if\_comp](if-comp---ps.md) blocks.</span></span>

<span data-ttu-id="781ea-134">Un \_ bloc si prédit ne peut pas chevaucher un bloc de boucle ; il doit l’être entièrement à l’intérieur ou l’entourer.</span><span class="sxs-lookup"><span data-stu-id="781ea-134">An if\_pred block cannot straddle a loop block; it should either be completely inside it or surround it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="781ea-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="781ea-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="781ea-136">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="781ea-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





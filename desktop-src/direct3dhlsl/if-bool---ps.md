---
title: Si bool-PS
description: Début d’un bloc If.
ms.assetid: cff53072-1c73-4cf8-9ecd-11032a9c4bbb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 92c3158a09aeb871ef367133c07278b0f3b87390
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679102"
---
# <a name="if-bool---ps"></a><span data-ttu-id="5e85a-103">Si bool-PS</span><span class="sxs-lookup"><span data-stu-id="5e85a-103">if bool - ps</span></span>

<span data-ttu-id="5e85a-104">Début d’un bloc If.</span><span class="sxs-lookup"><span data-stu-id="5e85a-104">Start of an if block.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e85a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e85a-105">Syntax</span></span>



| <span data-ttu-id="5e85a-106">Si bool</span><span class="sxs-lookup"><span data-stu-id="5e85a-106">if bool</span></span> |
|---------|



 

<span data-ttu-id="5e85a-107">Où :</span><span class="sxs-lookup"><span data-stu-id="5e85a-107">Where:</span></span>

-   <span data-ttu-id="5e85a-108">bool est un numéro de Registre bool (booléen).</span><span class="sxs-lookup"><span data-stu-id="5e85a-108">bool is a bool (Boolean) register number.</span></span> <span data-ttu-id="5e85a-109">Consultez [Registre booléen constant](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).</span><span class="sxs-lookup"><span data-stu-id="5e85a-109">See [Constant Boolean Register](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5e85a-110">Notes</span><span class="sxs-lookup"><span data-stu-id="5e85a-110">Remarks</span></span>



| <span data-ttu-id="5e85a-111">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="5e85a-111">Pixel shader versions</span></span> | <span data-ttu-id="5e85a-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="5e85a-112">1\_1</span></span> | <span data-ttu-id="5e85a-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="5e85a-113">1\_2</span></span> | <span data-ttu-id="5e85a-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="5e85a-114">1\_3</span></span> | <span data-ttu-id="5e85a-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="5e85a-115">1\_4</span></span> | <span data-ttu-id="5e85a-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5e85a-116">2\_0</span></span> | <span data-ttu-id="5e85a-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5e85a-117">2\_x</span></span> | <span data-ttu-id="5e85a-118">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="5e85a-118">2\_sw</span></span> | <span data-ttu-id="5e85a-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5e85a-119">3\_0</span></span> | <span data-ttu-id="5e85a-120">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="5e85a-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="5e85a-121">Si bool</span><span class="sxs-lookup"><span data-stu-id="5e85a-121">if bool</span></span>               |      |      |      |      |      | <span data-ttu-id="5e85a-122">x</span><span class="sxs-lookup"><span data-stu-id="5e85a-122">x</span></span>    | <span data-ttu-id="5e85a-123">x</span><span class="sxs-lookup"><span data-stu-id="5e85a-123">x</span></span>     | <span data-ttu-id="5e85a-124">x</span><span class="sxs-lookup"><span data-stu-id="5e85a-124">x</span></span>    | <span data-ttu-id="5e85a-125">x</span><span class="sxs-lookup"><span data-stu-id="5e85a-125">x</span></span>     |



 

<span data-ttu-id="5e85a-126">Si le registre booléen source dans l’instruction if a la valeur true, le code inclus dans l’instruction if et la correspondance [endif-PS](endif---ps.md) ou [else-PS](else---ps.md) est exécuté.</span><span class="sxs-lookup"><span data-stu-id="5e85a-126">If the source Boolean register in the if statement is true, the code enclosed by the if statement and the matching [endif - ps](endif---ps.md) or [else - ps](else---ps.md) is executed.</span></span> <span data-ttu-id="5e85a-127">Sinon, le code délimité par else-PS... les instructions endif-PS sont exécutées.</span><span class="sxs-lookup"><span data-stu-id="5e85a-127">Otherwise, the code enclosed by the else - ps...endif - ps statements is executed.</span></span> <span data-ttu-id="5e85a-128">Cette instruction consomme un emplacement d’instruction.</span><span class="sxs-lookup"><span data-stu-id="5e85a-128">This instruction consumes one instruction slot.</span></span>

<span data-ttu-id="5e85a-129">Un bloc If peut être imbriqué.</span><span class="sxs-lookup"><span data-stu-id="5e85a-129">An if block can be nested.</span></span>

<span data-ttu-id="5e85a-130">Un bloc If ne peut pas chevaucher un bloc de boucle.</span><span class="sxs-lookup"><span data-stu-id="5e85a-130">An if block cannot straddle a loop block.</span></span>

<span data-ttu-id="5e85a-131">Un bloc If peut être suivi d’un bloc d’instructions et/ou d’une instruction [else-PS](else---ps.md) , et/ou d’une instruction [endif-PS](endif---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="5e85a-131">An if block can be followed by a statement block, and/or an [else - ps](else---ps.md) instruction, and/or an [endif - ps](endif---ps.md) instruction.</span></span>

## <a name="example"></a><span data-ttu-id="5e85a-132">Exemple</span><span class="sxs-lookup"><span data-stu-id="5e85a-132">Example</span></span>

<span data-ttu-id="5e85a-133">Cette instruction fournit un contrôle de workflow statique conditionnel.</span><span class="sxs-lookup"><span data-stu-id="5e85a-133">This instruction provides conditional static flow control.</span></span>


```
defb b3, true

if b3
// Instructions to run if b3 is nonzero
else
// Instructions to run otherwise
endif
```



## <a name="related-topics"></a><span data-ttu-id="5e85a-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5e85a-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e85a-135">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="5e85a-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[<span data-ttu-id="5e85a-136">else-PS</span><span class="sxs-lookup"><span data-stu-id="5e85a-136">else - ps</span></span>](else---ps.md)
</dt> <dt>

[<span data-ttu-id="5e85a-137">endif-PS</span><span class="sxs-lookup"><span data-stu-id="5e85a-137">endif - ps</span></span>](endif---ps.md)
</dt> </dl>

 

 





---
title: Si bool-vs
description: Démarre une si... sinon... endif-bloc vs.
ms.assetid: d77e2f81-400c-4997-9c34-426b6e6f47be
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 261ff572cbaf519cc0099f3ab68d1a0becca706f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030554"
---
# <a name="if-bool---vs"></a><span data-ttu-id="2d63f-103">Si bool-vs</span><span class="sxs-lookup"><span data-stu-id="2d63f-103">if bool - vs</span></span>

<span data-ttu-id="2d63f-104">Démarre une si... [sinon](else---vs.md)... [endif-bloc vs](endif---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="2d63f-104">Starts an if...[else](else---vs.md)...[endif - vs](endif---vs.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d63f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d63f-105">Syntax</span></span>



| <span data-ttu-id="2d63f-106">Si bool</span><span class="sxs-lookup"><span data-stu-id="2d63f-106">if bool</span></span> |
|---------|



 

<span data-ttu-id="2d63f-107">où bool est un numéro de Registre bool.</span><span class="sxs-lookup"><span data-stu-id="2d63f-107">where bool is a bool register number.</span></span> <span data-ttu-id="2d63f-108">Consultez [Registre booléen constant](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).</span><span class="sxs-lookup"><span data-stu-id="2d63f-108">See [Constant Boolean Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2d63f-109">Notes</span><span class="sxs-lookup"><span data-stu-id="2d63f-109">Remarks</span></span>



| <span data-ttu-id="2d63f-110">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="2d63f-110">Vertex shader versions</span></span> | <span data-ttu-id="2d63f-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="2d63f-111">1\_1</span></span> | <span data-ttu-id="2d63f-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2d63f-112">2\_0</span></span> | <span data-ttu-id="2d63f-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2d63f-113">2\_x</span></span> | <span data-ttu-id="2d63f-114">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="2d63f-114">2\_sw</span></span> | <span data-ttu-id="2d63f-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2d63f-115">3\_0</span></span> | <span data-ttu-id="2d63f-116">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="2d63f-116">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="2d63f-117">Si bool</span><span class="sxs-lookup"><span data-stu-id="2d63f-117">if bool</span></span>                |      | <span data-ttu-id="2d63f-118">x</span><span class="sxs-lookup"><span data-stu-id="2d63f-118">x</span></span>    | <span data-ttu-id="2d63f-119">x</span><span class="sxs-lookup"><span data-stu-id="2d63f-119">x</span></span>    | <span data-ttu-id="2d63f-120">x</span><span class="sxs-lookup"><span data-stu-id="2d63f-120">x</span></span>     | <span data-ttu-id="2d63f-121">x</span><span class="sxs-lookup"><span data-stu-id="2d63f-121">x</span></span>    | <span data-ttu-id="2d63f-122">x</span><span class="sxs-lookup"><span data-stu-id="2d63f-122">x</span></span>     |



 

<span data-ttu-id="2d63f-123">Si le registre booléen source dans l’instruction if a la valeur true, le code inclus dans l’instruction if et le signe else correspondant est exécuté.</span><span class="sxs-lookup"><span data-stu-id="2d63f-123">If the source Boolean register in the if statement is true, the code enclosed by the if statement and the matching else is run.</span></span> <span data-ttu-id="2d63f-124">Sinon, le code délimité par [else](else---vs.md)... [endif-les instructions vs](endif---vs.md) sont exécutées.</span><span class="sxs-lookup"><span data-stu-id="2d63f-124">Otherwise, the code enclosed by the [else](else---vs.md)...[endif - vs](endif---vs.md) statements is run.</span></span> <span data-ttu-id="2d63f-125">Cette instruction consomme un emplacement d’instruction.</span><span class="sxs-lookup"><span data-stu-id="2d63f-125">This instruction consumes one instruction slot.</span></span>

<span data-ttu-id="2d63f-126">Si les blocs peuvent être imbriqués.</span><span class="sxs-lookup"><span data-stu-id="2d63f-126">if blocks can be nested.</span></span>

<span data-ttu-id="2d63f-127">Un bloc If ne peut pas chevaucher un bloc de boucle.</span><span class="sxs-lookup"><span data-stu-id="2d63f-127">An if block cannot straddle a loop block.</span></span>

## <a name="example"></a><span data-ttu-id="2d63f-128">Exemple</span><span class="sxs-lookup"><span data-stu-id="2d63f-128">Example</span></span>

<span data-ttu-id="2d63f-129">Cette instruction fournit un contrôle de workflow statique conditionnel.</span><span class="sxs-lookup"><span data-stu-id="2d63f-129">This instruction provides conditional static flow control.</span></span>


```
defb b2, TRUE

...

if b2
// Instructions to run if b2 is nonzero

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a><span data-ttu-id="2d63f-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2d63f-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d63f-131">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="2d63f-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[<span data-ttu-id="2d63f-132">else-vs</span><span class="sxs-lookup"><span data-stu-id="2d63f-132">else - vs</span></span>](else---vs.md)
</dt> <dt>

[<span data-ttu-id="2d63f-133">endif-vs</span><span class="sxs-lookup"><span data-stu-id="2d63f-133">endif - vs</span></span>](endif---vs.md)
</dt> </dl>

 

 





---
title: Précis
description: Désactivation par instruction de la refactorisation arithmétique.
ms.assetid: A26E569A-32EA-4AED-83C2-4F937AD3829E
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03f288fb5dafee0e29c8c11cab72156f7ad3d569
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104507707"
---
# <a name="precise"></a><span data-ttu-id="0c523-103">Précis</span><span class="sxs-lookup"><span data-stu-id="0c523-103">Precise</span></span>

<span data-ttu-id="0c523-104">Désactivation par instruction de la refactorisation arithmétique.</span><span class="sxs-lookup"><span data-stu-id="0c523-104">Per-instruction disabling of arithmetic refactoring.</span></span>



| <span data-ttu-id="0c523-105">précis (masque de composant)</span><span class="sxs-lookup"><span data-stu-id="0c523-105">precise (component mask)</span></span> |
|--------------------------|



 

<span data-ttu-id="0c523-106">Ce modificateur requiert l’indicateur de nuanceur global « refactorisation \_ autorisée ».</span><span class="sxs-lookup"><span data-stu-id="0c523-106">This modifier requires the global shader flag "REFACTORING\_ALLOWED".</span></span> <span data-ttu-id="0c523-107">Lorsque la refactorisation \_ autorisée est présente, les résultats individuels des instructions individuelles peuvent être forcés à rester précis ou non à refactoriser par les compilateurs ou les pilotes.</span><span class="sxs-lookup"><span data-stu-id="0c523-107">When REFACTORING\_ALLOWED is present, individual component results of individual instructions can be forced to remain precise or not-refactorable by compilers or drivers.</span></span> <span data-ttu-id="0c523-108">Si les composants d’une instruction [**Mad**](mad--sm4---asm-.md) sont marqués comme **précis**, le matériel doit exécuter une instruction **Mad** ou l’équivalent exact, et il ne peut pas le fractionner en une multiplication suivie d’un ajout.</span><span class="sxs-lookup"><span data-stu-id="0c523-108">If components of a [**mad**](mad--sm4---asm-.md) instruction are tagged as **precise**, the hardware must execute a **mad** instruction or the exact equivalent, and it cannot split it into a multiply followed by an add.</span></span> <span data-ttu-id="0c523-109">À l’inverse, une multiplication suivie d’un ajout, où les deux ou les deux sont marqués comme **précis**, ne peut pas être fusionnée dans un **Mad** fusionné.</span><span class="sxs-lookup"><span data-stu-id="0c523-109">Conversely, a multiply followed by an add, where either or both are flagged as **precise**, cannot be merged into a fused **mad**.</span></span>

<span data-ttu-id="0c523-110">Si la refactorisation \_ autorisée n’a pas été spécifiée, le modificateur **precise** n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="0c523-110">If REFACTORING\_ALLOWED has not been specified, the **precise** modifier is not allowed.</span></span> <span data-ttu-id="0c523-111">Cela n’est pas nécessaire, car tout est précis.</span><span class="sxs-lookup"><span data-stu-id="0c523-111">It is not needed because everything is precise.</span></span> <span data-ttu-id="0c523-112">Le modificateur **precise** affecte toute opération, pas seulement l’arithmétique.</span><span class="sxs-lookup"><span data-stu-id="0c523-112">The **precise** modifier affects any operation, not just arithmetic.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="0c523-113">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="0c523-113">Minimum Shader Model</span></span>

<span data-ttu-id="0c523-114">Ce modificateur est pris en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="0c523-114">This modifier is supported in the following shader models.</span></span>



| <span data-ttu-id="0c523-115">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="0c523-115">Shader Model</span></span>                                              | <span data-ttu-id="0c523-116">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="0c523-116">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0c523-117">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="0c523-117">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0c523-118">Oui</span><span class="sxs-lookup"><span data-stu-id="0c523-118">yes</span></span>       |
| [<span data-ttu-id="0c523-119">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="0c523-119">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0c523-120">non</span><span class="sxs-lookup"><span data-stu-id="0c523-120">no</span></span>        |
| [<span data-ttu-id="0c523-121">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="0c523-121">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0c523-122">Oui</span><span class="sxs-lookup"><span data-stu-id="0c523-122">yes</span></span>       |
| [<span data-ttu-id="0c523-123">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0c523-123">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0c523-124">non</span><span class="sxs-lookup"><span data-stu-id="0c523-124">no</span></span>        |
| [<span data-ttu-id="0c523-125">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0c523-125">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0c523-126">non</span><span class="sxs-lookup"><span data-stu-id="0c523-126">no</span></span>        |
| [<span data-ttu-id="0c523-127">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0c523-127">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0c523-128">non</span><span class="sxs-lookup"><span data-stu-id="0c523-128">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0c523-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0c523-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c523-130">Modificateurs d’instruction du Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="0c523-130">Shader Model 5 Instruction Modifiers</span></span>](shader-model-5-instruction-modifiers.md)
</dt> </dl>

 

 





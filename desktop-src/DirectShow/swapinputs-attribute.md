---
description: L’attribut swapinputs spécifie s’il faut échanger les entrées de transition. Si la valeur est TRUE, les entrées sont échangées. La valeur par défaut est FALSE.
ms.assetid: 2b8d95ec-2c6c-4bd8-83e9-7f72770449b5
title: Attribut swapinputs
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27e2f02c642283e90b994bcd1bfa9e05076a7bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320602"
---
# <a name="swapinputs-attribute"></a><span data-ttu-id="d9cc7-105">Attribut swapinputs</span><span class="sxs-lookup"><span data-stu-id="d9cc7-105">swapinputs Attribute</span></span>

> [!Note]  
> <span data-ttu-id="d9cc7-106">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="d9cc7-106">\[Deprecated.</span></span> <span data-ttu-id="d9cc7-107">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d9cc7-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d9cc7-108">L' `swapinputs` attribut spécifie s’il faut échanger les entrées de transition.</span><span class="sxs-lookup"><span data-stu-id="d9cc7-108">The `swapinputs` attribute specifies whether to swap transition inputs.</span></span> <span data-ttu-id="d9cc7-109">Si la valeur est **true**, les entrées sont échangées.</span><span class="sxs-lookup"><span data-stu-id="d9cc7-109">If the value is **TRUE**, the inputs are swapped.</span></span> <span data-ttu-id="d9cc7-110">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="d9cc7-110">The default value is **FALSE**.</span></span>

## <a name="possible-values"></a><span data-ttu-id="d9cc7-111">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="d9cc7-111">Possible Values</span></span>

<span data-ttu-id="d9cc7-112">Les valeurs suivantes sont définies sur TRUE : y, Y, t, T, 1.</span><span class="sxs-lookup"><span data-stu-id="d9cc7-112">The following values are defined as TRUE: y, Y, t, T, 1.</span></span> <span data-ttu-id="d9cc7-113">Les valeurs suivantes sont définies avec la valeur FALSe : n, N, f, F, 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="d9cc7-113">The following values are defined as FALSE: n, N, f, F, 0 (zero).</span></span>

## <a name="applies-to"></a><span data-ttu-id="d9cc7-114">S'applique à</span><span class="sxs-lookup"><span data-stu-id="d9cc7-114">Applies To</span></span>

[<span data-ttu-id="d9cc7-115">**passe**</span><span class="sxs-lookup"><span data-stu-id="d9cc7-115">**transition**</span></span>](transition-element.md)

## <a name="remarks"></a><span data-ttu-id="d9cc7-116">Notes</span><span class="sxs-lookup"><span data-stu-id="d9cc7-116">Remarks</span></span>

<span data-ttu-id="d9cc7-117">Par défaut, une transition se poursuit à partir du composite de toutes les couches de faible priorité vers la couche sur laquelle la transition réside.</span><span class="sxs-lookup"><span data-stu-id="d9cc7-117">By default, a transition proceeds from the composite of all lower-priority layers to the layer on which the transition resides.</span></span> <span data-ttu-id="d9cc7-118">Si l' `swapinputs` attribut est 1, cette direction est inversée.</span><span class="sxs-lookup"><span data-stu-id="d9cc7-118">If the `swapinputs` attribute is 1, this direction is reversed.</span></span> <span data-ttu-id="d9cc7-119">Pour plus d’informations sur le modèle de structuration en couches utilisé par DES, consultez [le modèle de chronologie](the-timeline-model.md).</span><span class="sxs-lookup"><span data-stu-id="d9cc7-119">For more information about the layering model used by DES, see [The Timeline Model](the-timeline-model.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d9cc7-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9cc7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9cc7-121">Attributs XTL</span><span class="sxs-lookup"><span data-stu-id="d9cc7-121">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="d9cc7-122">**IAMTimelineTrans::SetSwapInputs**</span><span class="sxs-lookup"><span data-stu-id="d9cc7-122">**IAMTimelineTrans::SetSwapInputs**</span></span>](iamtimelinetrans-setswapinputs.md)
</dt> </dl>

 

 




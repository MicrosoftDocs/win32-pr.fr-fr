---
description: L’attribut cutpoint spécifie quand une transition passe d’une source à la suivante, si la transition est rendue sous la forme d’une coupe. La valeur est relative au début de la transition.
ms.assetid: bdb0b8cd-025f-4b56-9cd4-f71c58ee809a
title: Attribut cutpoint
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd516bd67577906a0a06d8da692ffbd7563ce32f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109231"
---
# <a name="cutpoint-attribute"></a><span data-ttu-id="a746f-104">Attribut cutpoint</span><span class="sxs-lookup"><span data-stu-id="a746f-104">cutpoint Attribute</span></span>

> [!Note]  
> <span data-ttu-id="a746f-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="a746f-105">\[Deprecated.</span></span> <span data-ttu-id="a746f-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a746f-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a746f-107">L' `cutpoint` attribut spécifie quand une transition passe d’une source à la suivante, si la transition est rendue sous la forme d’une coupe.</span><span class="sxs-lookup"><span data-stu-id="a746f-107">The `cutpoint` attribute specifies when a transition cuts from one source to the next, if the transition is rendered as a cut.</span></span> <span data-ttu-id="a746f-108">La valeur est relative au début de la transition.</span><span class="sxs-lookup"><span data-stu-id="a746f-108">The value is relative to the start of the transition.</span></span>

## <a name="possible-values"></a><span data-ttu-id="a746f-109">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="a746f-109">Possible Values</span></span>

<span data-ttu-id="a746f-110">Doit être une chaîne au format *hh : mm : SS. FF* , où *hh* = heures, *mm* = minutes, *SS* = secondes et *FF* = fractions de secondes.</span><span class="sxs-lookup"><span data-stu-id="a746f-110">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="a746f-111">Exemple : 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="a746f-111">Example: 1:04:30.512.</span></span> <span data-ttu-id="a746f-112">Les unités de début peuvent être omises.</span><span class="sxs-lookup"><span data-stu-id="a746f-112">Leading units can be omitted.</span></span> <span data-ttu-id="a746f-113">Par exemple, 3:00 (trois minutes) et 45 (45 secondes) sont valides.</span><span class="sxs-lookup"><span data-stu-id="a746f-113">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="applies-to"></a><span data-ttu-id="a746f-114">S'applique à</span><span class="sxs-lookup"><span data-stu-id="a746f-114">Applies To</span></span>

[<span data-ttu-id="a746f-115">**passe**</span><span class="sxs-lookup"><span data-stu-id="a746f-115">**transition**</span></span>](transition-element.md)

## <a name="see-also"></a><span data-ttu-id="a746f-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a746f-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a746f-117">Attributs XTL</span><span class="sxs-lookup"><span data-stu-id="a746f-117">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="a746f-118">**IAMTimelineTrans::SetCutPoint**</span><span class="sxs-lookup"><span data-stu-id="a746f-118">**IAMTimelineTrans::SetCutPoint**</span></span>](iamtimelinetrans-setcutpoint.md)
</dt> </dl>

 

 




---
description: L’attribut Start spécifie l’heure de début d’un objet, par rapport à l’objet parent.
ms.assetid: 971de88e-c1ee-4e07-bf8e-3153e4fd11f3
title: Start (attribut)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b377d0d83c86b981400a784904cf0423f0cca20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536558"
---
# <a name="start-attribute"></a><span data-ttu-id="68c3f-103">Start (attribut)</span><span class="sxs-lookup"><span data-stu-id="68c3f-103">start Attribute</span></span>

> [!Note]  
> <span data-ttu-id="68c3f-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="68c3f-104">\[Deprecated.</span></span> <span data-ttu-id="68c3f-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="68c3f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="68c3f-106">L' `start` attribut spécifie l’heure de début d’un objet, par rapport à l’objet parent.</span><span class="sxs-lookup"><span data-stu-id="68c3f-106">The `start` attribute specifies the start time of an object, relative to the parent object.</span></span>

## <a name="possible-values"></a><span data-ttu-id="68c3f-107">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="68c3f-107">Possible Values</span></span>

<span data-ttu-id="68c3f-108">Doit être une chaîne au format *hh : mm : SS. FF* , où *hh* = heures, *mm* = minutes, *SS* = secondes et *FF* = fractions de secondes.</span><span class="sxs-lookup"><span data-stu-id="68c3f-108">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="68c3f-109">Exemple : 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="68c3f-109">Example: 1:04:30.512.</span></span> <span data-ttu-id="68c3f-110">Les unités de début peuvent être omises.</span><span class="sxs-lookup"><span data-stu-id="68c3f-110">Leading units can be omitted.</span></span> <span data-ttu-id="68c3f-111">Par exemple, 3:00 (trois minutes) et 45 (45 secondes) sont valides.</span><span class="sxs-lookup"><span data-stu-id="68c3f-111">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="applies-to"></a><span data-ttu-id="68c3f-112">S'applique à</span><span class="sxs-lookup"><span data-stu-id="68c3f-112">Applies To</span></span>

<span data-ttu-id="68c3f-113">[**clip**](clip-element.md), [**effet**](effect-element.md), [**transition**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="68c3f-113">[**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="68c3f-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68c3f-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68c3f-115">Attributs XTL</span><span class="sxs-lookup"><span data-stu-id="68c3f-115">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="68c3f-116">**IAMTimelineObj::SetStartStop**</span><span class="sxs-lookup"><span data-stu-id="68c3f-116">**IAMTimelineObj::SetStartStop**</span></span>](iamtimelineobj-setstartstop.md)
</dt> </dl>

 

 




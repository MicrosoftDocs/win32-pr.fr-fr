---
description: L’attribut Stop spécifie l’heure d’arrêt d’un objet, par rapport à l’objet parent.
ms.assetid: 1bda3472-abda-4672-9b82-311163e56fe0
title: arrêter l’attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6deb3f2a422cb8100da32c0427caf6436e72fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545026"
---
# <a name="stop-attribute"></a><span data-ttu-id="5ee07-103">arrêter l’attribut</span><span class="sxs-lookup"><span data-stu-id="5ee07-103">stop Attribute</span></span>

> [!Note]  
> <span data-ttu-id="5ee07-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="5ee07-104">\[Deprecated.</span></span> <span data-ttu-id="5ee07-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5ee07-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5ee07-106">L' `stop` attribut spécifie l’heure d’arrêt d’un objet, par rapport à l’objet parent.</span><span class="sxs-lookup"><span data-stu-id="5ee07-106">The `stop` attribute specifies the stop time of an object, relative to the parent object.</span></span>

## <a name="possible-values"></a><span data-ttu-id="5ee07-107">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="5ee07-107">Possible Values</span></span>

<span data-ttu-id="5ee07-108">Doit être une chaîne au format *hh : mm : SS. FF* , où *hh* = heures, *mm* = minutes, *SS* = secondes et *FF* = fractions de secondes.</span><span class="sxs-lookup"><span data-stu-id="5ee07-108">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="5ee07-109">Exemple : 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="5ee07-109">Example: 1:04:30.512.</span></span> <span data-ttu-id="5ee07-110">Les unités de début peuvent être omises.</span><span class="sxs-lookup"><span data-stu-id="5ee07-110">Leading units can be omitted.</span></span> <span data-ttu-id="5ee07-111">Par exemple, 3:00 (trois minutes) et 45 (45 secondes) sont valides.</span><span class="sxs-lookup"><span data-stu-id="5ee07-111">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="applies-to"></a><span data-ttu-id="5ee07-112">S'applique à</span><span class="sxs-lookup"><span data-stu-id="5ee07-112">Applies To</span></span>

<span data-ttu-id="5ee07-113">[**clip**](clip-element.md), [**effet**](effect-element.md), [**transition**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="5ee07-113">[**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="5ee07-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ee07-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ee07-115">Attributs XTL</span><span class="sxs-lookup"><span data-stu-id="5ee07-115">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="5ee07-116">**IAMTimelineObj::SetStartStop**</span><span class="sxs-lookup"><span data-stu-id="5ee07-116">**IAMTimelineObj::SetStartStop**</span></span>](iamtimelineobj-setstartstop.md)
</dt> </dl>

 

 




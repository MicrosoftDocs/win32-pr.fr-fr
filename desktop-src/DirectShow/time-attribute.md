---
description: L’attribut Time spécifie l’heure à laquelle un paramètre assume une nouvelle valeur, par rapport au début de la transition ou de l’effet.
ms.assetid: bb478215-cbd5-4fea-9d88-a1f2b002f3da
title: Attribut heure
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15a84d40c5e38ed81f8c17cd2d931e3f85e389a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210949"
---
# <a name="time-attribute"></a><span data-ttu-id="8edf7-103">Attribut heure</span><span class="sxs-lookup"><span data-stu-id="8edf7-103">time Attribute</span></span>

> [!Note]  
> <span data-ttu-id="8edf7-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="8edf7-104">\[Deprecated.</span></span> <span data-ttu-id="8edf7-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8edf7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8edf7-106">L' `time` attribut spécifie l’heure à laquelle un paramètre assume une nouvelle valeur, par rapport au début de la transition ou de l’effet.</span><span class="sxs-lookup"><span data-stu-id="8edf7-106">The `time` attribute specifies the time at which a parameter assumes a new value, relative to the start of the transition or effect.</span></span>

## <a name="possible-values"></a><span data-ttu-id="8edf7-107">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="8edf7-107">Possible Values</span></span>

<span data-ttu-id="8edf7-108">Doit être une chaîne au format *hh : mm : SS. FF* , où *hh* = heures, *mm* = minutes, *SS* = secondes et *FF* = fractions de secondes.</span><span class="sxs-lookup"><span data-stu-id="8edf7-108">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="8edf7-109">Exemple : 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="8edf7-109">Example: 1:04:30.512.</span></span> <span data-ttu-id="8edf7-110">Les unités de début peuvent être omises.</span><span class="sxs-lookup"><span data-stu-id="8edf7-110">Leading units can be omitted.</span></span> <span data-ttu-id="8edf7-111">Par exemple, 3:00 (trois minutes) et 45 (45 secondes) sont valides.</span><span class="sxs-lookup"><span data-stu-id="8edf7-111">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="applies-to"></a><span data-ttu-id="8edf7-112">S'applique à</span><span class="sxs-lookup"><span data-stu-id="8edf7-112">Applies To</span></span>

<span data-ttu-id="8edf7-113">[**at**](at-element.md), [ **linéaire**](linear-element.md)</span><span class="sxs-lookup"><span data-stu-id="8edf7-113">[**at**](at-element.md), [**linear**](linear-element.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="8edf7-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8edf7-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8edf7-115">Attributs XTL</span><span class="sxs-lookup"><span data-stu-id="8edf7-115">XTL Attributes</span></span>](xtl-attributes.md)
</dt> </dl>

 

 




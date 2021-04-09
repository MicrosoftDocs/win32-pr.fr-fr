---
description: La propriété TotalTitleTime récupère le temps de lecture total pour le titre actuel.
ms.assetid: b05bb76b-d4ba-42e6-92ea-8e48f4c8f409
title: Propriété TotalTitleTime
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a300a2da8de2698a74e0d72362818bd8a2a5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865789"
---
# <a name="totaltitletime-property"></a><span data-ttu-id="16d60-103">Propriété TotalTitleTime</span><span class="sxs-lookup"><span data-stu-id="16d60-103">TotalTitleTime Property</span></span>

> [!Note]  
> <span data-ttu-id="16d60-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="16d60-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="16d60-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="16d60-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="16d60-106">La `TotalTitleTime` propriété récupère le temps de lecture total pour le titre actuel.</span><span class="sxs-lookup"><span data-stu-id="16d60-106">The `TotalTitleTime` property retrieves the total playback time for the current title.</span></span>

``` syntax
[ sTotalTime = ] MSWebDVD.TotalTitleTime
```

## <a name="return-value"></a><span data-ttu-id="16d60-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="16d60-107">Return Value</span></span>

<span data-ttu-id="16d60-108">Retourne la durée d’exécution totale du titre actuel sous la forme d’une chaîne au format « hh : mm : SS : FF ».</span><span class="sxs-lookup"><span data-stu-id="16d60-108">Returns the total playing time of the current title as a String in the format "hh:mm:ss:ff".</span></span>

## <a name="remarks"></a><span data-ttu-id="16d60-109">Notes</span><span class="sxs-lookup"><span data-stu-id="16d60-109">Remarks</span></span>

<span data-ttu-id="16d60-110">Cette propriété est en lecture seule sans valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="16d60-110">This property is read-only with no default value.</span></span> <span data-ttu-id="16d60-111">La chaîne retournée aura une longueur de 11 caractères au format « hh : mm : SS : FF » (heures, minutes, secondes, frames).</span><span class="sxs-lookup"><span data-stu-id="16d60-111">The returned string will be 11 characters long in the format "hh:mm:ss:ff" (hours, minutes, seconds, frames).</span></span>

## <a name="see-also"></a><span data-ttu-id="16d60-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16d60-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16d60-113">**PlayAtTime**</span><span class="sxs-lookup"><span data-stu-id="16d60-113">**PlayAtTime**</span></span>](playattime-method.md)
</dt> <dt>

[<span data-ttu-id="16d60-114">**PlayAtTimeInTitle**</span><span class="sxs-lookup"><span data-stu-id="16d60-114">**PlayAtTimeInTitle**</span></span>](playattimeintitle-method.md)
</dt> </dl>

 

 




---
description: La méthode PlayPeriodInTitleAutoStop démarre la lecture à l’heure spécifiée dans le titre spécifié jusqu’à l’heure d’arrêt spécifiée.
ms.assetid: 0c4df76d-3991-4a6c-a8e5-5fd713eeffc2
title: Méthode PlayPeriodInTitleAutoStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d05899b66b7f1a11f8f5b177d311b9634a52595b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846145"
---
# <a name="playperiodintitleautostop-method"></a><span data-ttu-id="fec2d-103">Méthode PlayPeriodInTitleAutoStop</span><span class="sxs-lookup"><span data-stu-id="fec2d-103">PlayPeriodInTitleAutoStop Method</span></span>

> [!Note]  
> <span data-ttu-id="fec2d-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="fec2d-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="fec2d-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="fec2d-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="fec2d-106">La `PlayPeriodInTitleAutoStop` méthode démarre la lecture à l’heure spécifiée dans le titre spécifié jusqu’à l’heure d’arrêt spécifiée.</span><span class="sxs-lookup"><span data-stu-id="fec2d-106">The `PlayPeriodInTitleAutoStop` method starts playback at the specified time in the specified title until the specified stop time.</span></span>

``` syntax
MSWebDVD.PlayPeriodInTitleAutoStop(iTitle, sStartTime, sEndTime)
```

## <a name="parameters"></a><span data-ttu-id="fec2d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fec2d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fec2d-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span><span class="sxs-lookup"><span data-stu-id="fec2d-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="fec2d-109">Spécifie le titre sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="fec2d-109">Specifies the title as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="fec2d-110"><span id="sStartTime"></span><span id="sstarttime"></span><span id="SSTARTTIME"></span>*sStartTime*</span><span class="sxs-lookup"><span data-stu-id="fec2d-110"><span id="sStartTime"></span><span id="sstarttime"></span><span id="SSTARTTIME"></span>*sStartTime*</span></span>
</dt> <dd>

<span data-ttu-id="fec2d-111">Spécifie l’heure de début sous la forme d’une chaîne au format « hh : mm : SS : FF » (en spécifiant les heures, les minutes, les secondes, les frames).</span><span class="sxs-lookup"><span data-stu-id="fec2d-111">Specifies the start time as a string in "hh:mm:ss:ff" format (specifying hours, minutes, seconds, frames).</span></span>

</dd> <dt>

<span data-ttu-id="fec2d-112"><span id="sEndTime"></span><span id="sendtime"></span><span id="SENDTIME"></span>*sEndTime*</span><span class="sxs-lookup"><span data-stu-id="fec2d-112"><span id="sEndTime"></span><span id="sendtime"></span><span id="SENDTIME"></span>*sEndTime*</span></span>
</dt> <dd>

<span data-ttu-id="fec2d-113">Spécifie l’heure de fin sous la forme d’une chaîne au format « hh : mm : SS : FF ».</span><span class="sxs-lookup"><span data-stu-id="fec2d-113">Specifies the end time as a String in "hh:mm:ss:ff" format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fec2d-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fec2d-114">Return Value</span></span>

<span data-ttu-id="fec2d-115">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="fec2d-115">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="fec2d-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fec2d-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fec2d-117">**PlayChaptersAutoStop**</span><span class="sxs-lookup"><span data-stu-id="fec2d-117">**PlayChaptersAutoStop**</span></span>](playchaptersautostop-method.md)
</dt> </dl>

 

 




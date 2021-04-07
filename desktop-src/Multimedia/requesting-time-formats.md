---
title: Demande de formats d’heure
description: Demande de formats d’heure
ms.assetid: 3492dfe3-ed54-405a-aa4f-b17abbd1e07f
keywords:
- MIDI (Musical Instrument Digital Interface), formats d’heure
- MIDI (Musical Instrument Digital Interface), formats d’heure
- Services MIDI, formats d’heure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf191c857c45896c916ace4656d33bd3dd558f04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724805"
---
# <a name="requesting-time-formats"></a><span data-ttu-id="d27a2-106">Demande de formats d’heure</span><span class="sxs-lookup"><span data-stu-id="d27a2-106">Requesting Time Formats</span></span>

<span data-ttu-id="d27a2-107">Windows utilise la structure [**MMTIME**](/previous-versions//dd757347(v=vs.85)) pour représenter le temps dans un ou plusieurs formats différents, y compris les millisecondes, les échantillons, les formats de pointeurs de chansons SMPTE et midi.</span><span class="sxs-lookup"><span data-stu-id="d27a2-107">Windows uses the [**MMTIME**](/previous-versions//dd757347(v=vs.85)) structure to represent time in one or more different formats, including milliseconds, samples, SMPTE, and MIDI song pointer formats.</span></span> <span data-ttu-id="d27a2-108">Le membre **wType** spécifie le format d’heure.</span><span class="sxs-lookup"><span data-stu-id="d27a2-108">The **wType** member specifies the time format.</span></span>

<span data-ttu-id="d27a2-109">La fonction [**midiStreamPosition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) utilise la structure **MMTIME** .</span><span class="sxs-lookup"><span data-stu-id="d27a2-109">The [**midiStreamPosition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) function uses the **MMTIME** structure.</span></span> <span data-ttu-id="d27a2-110">Avant d’appeler cette fonction, vous devez définir le membre **wType** pour indiquer le format d’heure demandé.</span><span class="sxs-lookup"><span data-stu-id="d27a2-110">Before calling this function, you must set the **wType** member to indicate your requested time format.</span></span> <span data-ttu-id="d27a2-111">Pour voir si le format d’heure demandé est pris en charge, vérifiez **wType** après l’appel.</span><span class="sxs-lookup"><span data-stu-id="d27a2-111">To see if the requested time format is supported, check **wType** after the call.</span></span> <span data-ttu-id="d27a2-112">Si le format d’heure demandé n’est pas pris en charge, l’heure est spécifiée dans un autre format d’heure sélectionné par le pilote de périphérique et le membre **wType** est modifié pour indiquer le format d’heure sélectionné.</span><span class="sxs-lookup"><span data-stu-id="d27a2-112">If the requested time format is not supported, the time is specified in an alternate time format selected by the device driver and the **wType** member is changed to indicate the selected time format.</span></span>

<span data-ttu-id="d27a2-113">Pour plus d’informations sur la structure **MMTIME** , consultez [minuteries multimédias](multimedia-timers.md).</span><span class="sxs-lookup"><span data-stu-id="d27a2-113">For more information about the **MMTIME** structure, see [Multimedia Timers](multimedia-timers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d27a2-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d27a2-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d27a2-115">Services MIDI</span><span class="sxs-lookup"><span data-stu-id="d27a2-115">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 
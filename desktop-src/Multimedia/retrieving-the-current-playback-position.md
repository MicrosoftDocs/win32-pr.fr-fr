---
title: Récupération de la position de lecture actuelle
description: Récupération de la position de lecture actuelle
ms.assetid: a08fe5da-8945-486f-9413-877c7d13d5de
keywords:
- audio de forme d’onde, position de lecture actuelle
- Waveform-interface audio, position de lecture actuelle
- lecture des fichiers Waveform-Audio, position de lecture actuelle
- waveOutGetPosition fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28737cfc292dc8779b21756f38813642b82e452
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314675"
---
# <a name="retrieving-the-current-playback-position"></a><span data-ttu-id="56d8b-107">Récupération de la position de lecture actuelle</span><span class="sxs-lookup"><span data-stu-id="56d8b-107">Retrieving the Current Playback Position</span></span>

<span data-ttu-id="56d8b-108">Vous pouvez surveiller la position de lecture actuelle dans le fichier lors de la lecture de l’audio Wave à l’aide de la fonction [**waveOutGetPosition**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition) .</span><span class="sxs-lookup"><span data-stu-id="56d8b-108">You can monitor the current playback position within the file while waveform audio is playing by using the [**waveOutGetPosition**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition) function.</span></span>

<span data-ttu-id="56d8b-109">Pour les périphériques audio Waveform, les exemples sont le format d’heure par défaut dans lequel représenter la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="56d8b-109">For waveform-audio devices, samples are the preferred time format in which to represent the current position.</span></span> <span data-ttu-id="56d8b-110">Ainsi, la position actuelle d’un périphérique audio Waveform est spécifiée comme le nombre d’échantillons pour un canal à partir du début du fichier Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="56d8b-110">Thus, the current position of a waveform-audio device is specified as the number of samples for one channel from the beginning of the waveform-audio file.</span></span> <span data-ttu-id="56d8b-111">Pour interroger la position actuelle d’un périphérique audio Waveform, définissez le membre **wType** de la structure [**MMTIME**](/previous-versions//dd757347(v=vs.85)) sur des échantillons de temps \_ et transmettez cette structure à **waveOutGetPosition**.</span><span class="sxs-lookup"><span data-stu-id="56d8b-111">To query the current position of a waveform-audio device, set the **wType** member of the [**MMTIME**](/previous-versions//dd757347(v=vs.85)) structure to TIME\_SAMPLES and pass this structure to **waveOutGetPosition**.</span></span>

<span data-ttu-id="56d8b-112">La structure **MMTIME** peut représenter le temps dans un ou plusieurs formats différents, y compris les millisecondes, les échantillons, les ingénieurs de la société de motion et les formats de pointeur de chanson midi.</span><span class="sxs-lookup"><span data-stu-id="56d8b-112">The **MMTIME** structure can represent time in one or more different formats, including milliseconds, samples, SMPTE (Society of Motion Picture and Television Engineers), and MIDI song pointer formats.</span></span> <span data-ttu-id="56d8b-113">Le membre **wType** spécifie le format utilisé pour représenter l’heure.</span><span class="sxs-lookup"><span data-stu-id="56d8b-113">The **wType** member specifies the format used to represent time.</span></span> <span data-ttu-id="56d8b-114">Avant d’appeler une fonction qui utilise la structure **MMTIME** , vous devez définir **wType** pour indiquer le format d’heure demandé.</span><span class="sxs-lookup"><span data-stu-id="56d8b-114">Before calling a function that uses the **MMTIME** structure, you must set **wType** to indicate your requested time format.</span></span> <span data-ttu-id="56d8b-115">Veillez à vérifier **wType** après l’appel pour voir si le format d’heure demandé est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="56d8b-115">Be sure to check **wType** after the call to see whether the requested time format is supported.</span></span> <span data-ttu-id="56d8b-116">Si le format d’heure demandé n’est pas pris en charge, le pilote de périphérique spécifie l’heure dans un autre format d’heure et remplace le membre **wType** par le format d’heure sélectionné.</span><span class="sxs-lookup"><span data-stu-id="56d8b-116">If the requested time format is not supported, the device driver specifies the time in an alternate time format and changes the **wType** member to the selected time format.</span></span>

<span data-ttu-id="56d8b-117">Pour plus d’informations sur la structure **MMTIME** , consultez [minuteries multimédias](multimedia-timers.md).</span><span class="sxs-lookup"><span data-stu-id="56d8b-117">For more information about the **MMTIME** structure, see [Multimedia Timers](multimedia-timers.md).</span></span>

 

 
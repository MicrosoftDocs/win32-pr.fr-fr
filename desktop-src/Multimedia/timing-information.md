---
title: Informations de minutage
description: Informations de minutage
ms.assetid: ff9d6fb2-1387-49ce-a4de-1b2f67353628
keywords:
- MIDI (Musical Instrument Digital Interface), informations de minutage
- MIDI (Musical Instrument Digital Interface), informations de minutage
- mémoires tampons de flux, informations de minutage
- MIDIEVENT, structure
- mémoires tampons de flux, format SMPTE
- mémoires tampons de flux, heure de la note du trimestre
- mémoires tampons de flux, cycles
- Format SMPTE
- heure de la note du trimestre
- ticks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2daf5b1847456e8fb518665521e484118fead79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101489"
---
# <a name="timing-information"></a><span data-ttu-id="00fae-113">Informations de minutage</span><span class="sxs-lookup"><span data-stu-id="00fae-113">Timing Information</span></span>

<span data-ttu-id="00fae-114">Les informations de minutage pour un événement MIDI sont stockées dans le membre **dwDeltaTime** de la structure [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) .</span><span class="sxs-lookup"><span data-stu-id="00fae-114">Timing information for a MIDI event is stored in the **dwDeltaTime** member of the [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structure.</span></span> <span data-ttu-id="00fae-115">L’heure est indiquée en graduations, comme défini dans la spécification *1,0 des fichiers MIDI standard* .</span><span class="sxs-lookup"><span data-stu-id="00fae-115">Time is given in ticks, as defined in the *Standard MIDI Files 1.0* specification.</span></span> <span data-ttu-id="00fae-116">La longueur d’un battement est définie par le format d’heure et éventuellement par le tempo associé au flux.</span><span class="sxs-lookup"><span data-stu-id="00fae-116">The length of a tick is defined by the time format and possibly the tempo associated with the stream.</span></span> <span data-ttu-id="00fae-117">Pour plus d’informations sur les flux, consultez [flux midi](midi-streams.md).</span><span class="sxs-lookup"><span data-stu-id="00fae-117">For more information about streams, see [MIDI Streams](midi-streams.md).</span></span>

<span data-ttu-id="00fae-118">Une graduation est exprimée en microsecondes par trimestre ou en tant que battements de temps de l’information SMPTE (société de motion et ingénieurs de la télévision).</span><span class="sxs-lookup"><span data-stu-id="00fae-118">A tick is expressed either as microseconds per quarter note or as ticks of SMPTE (Society of Motion Picture and Television Engineers) time.</span></span> <span data-ttu-id="00fae-119">Les applications qui envoient des messages MIDI individuellement ou utilisent des messages MIDI non traités utilisent l’heure de la note trimestrielle et les informations sur le tempo pour déterminer la durée d’un cycle.</span><span class="sxs-lookup"><span data-stu-id="00fae-119">Applications that send MIDI messages individually or use unprocessed MIDI messages use quarter note time and tempo information to determine the duration of a tick.</span></span> <span data-ttu-id="00fae-120">Les applications qui prétraitent les messages MIDI peuvent stocker le temps écoulé en tant que nombre d’unités SMPTE utilisées.</span><span class="sxs-lookup"><span data-stu-id="00fae-120">Applications that preprocess MIDI messages can store the elapsed time as a count of the SMPTE units being used.</span></span>

<span data-ttu-id="00fae-121">L’heure de la note du trimestre est indiquée par un zéro dans le bit de mot haute (bit 15) du mot de la Division horaire.</span><span class="sxs-lookup"><span data-stu-id="00fae-121">Quarter note time is indicated with a zero in the high-word bit (bit 15) of the time-division word.</span></span> <span data-ttu-id="00fae-122">Le reste du mot contient la note des graduations par trimestre.</span><span class="sxs-lookup"><span data-stu-id="00fae-122">The remainder of the word contains the ticks per quarter note.</span></span> <span data-ttu-id="00fae-123">Un tempo associé à un flux de données MIDI est conservé en unités (microsecondes par trimestre) conformément à la spécification des *fichiers midi Standard 1,0* .</span><span class="sxs-lookup"><span data-stu-id="00fae-123">A tempo associated with a stream of MIDI data is kept in units (microseconds per quarter note) consistent with the *Standard MIDI Files 1.0* specification.</span></span> <span data-ttu-id="00fae-124">Par exemple, une note d’un quart de l’heure 4/4 qui utilise une note tempo de 500 000 microsecondes par trimestre est lue au taux de 120 temps par minute.</span><span class="sxs-lookup"><span data-stu-id="00fae-124">For example, a quarter note in 4/4 time that uses a tempo of 500,000 microseconds per quarter note plays at the rate of 120 beats per minute.</span></span>

<span data-ttu-id="00fae-125">Les formats de la Division de temps SMPTE spécifient entièrement la longueur d’un battement sans avoir besoin d’informations sur le tempo.</span><span class="sxs-lookup"><span data-stu-id="00fae-125">SMPTE time division formats completely specify the length of a tick without the need for tempo information.</span></span> <span data-ttu-id="00fae-126">Dans à l’aide des formats d’heure SMPTE, les séquences MIDI peuvent être synchronisées avec d’autres événements SMPTE, tels que des vidéos ou des données audio entrelacées.</span><span class="sxs-lookup"><span data-stu-id="00fae-126">In using SMPTE time formats, MIDI sequences can be synchronized with other SMPTE events, such as video or striped audio.</span></span> <span data-ttu-id="00fae-127">L’heure SMPTE est indiquée par un 1 dans le bit de poids fort (bit 15) du mot de la Division temporelle.</span><span class="sxs-lookup"><span data-stu-id="00fae-127">SMPTE time is indicated with a 1 in the high-order bit (bit 15) of the time-division word.</span></span> <span data-ttu-id="00fae-128">Le reste de l’octet le plus significatif spécifie le format SMPTE utilisé comme valeurs négatives.</span><span class="sxs-lookup"><span data-stu-id="00fae-128">The rest of the most-significant byte specifies the SMPTE format in use as negative values.</span></span> <span data-ttu-id="00fae-129">Les formats SMPTE pris en charge et leurs valeurs correspondantes (entre parenthèses) sont 24 (-24), 25 (-25), 30 (-30) et 30 Drop (-29).</span><span class="sxs-lookup"><span data-stu-id="00fae-129">The supported SMPTE formats and their corresponding values (in parentheses) are 24 (-24), 25 (-25), 30 (-30), and 30 drop (-29).</span></span> <span data-ttu-id="00fae-130">L’octet de poids faible du mot de la Division horaire spécifie le nombre de graduations par cadre SMPTE.</span><span class="sxs-lookup"><span data-stu-id="00fae-130">The low byte of the time-division word specifies the number of ticks per SMPTE frame.</span></span>

 

 
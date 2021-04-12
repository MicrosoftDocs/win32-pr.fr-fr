---
title: Informations de référence MIDI
description: Informations de référence MIDI
ms.assetid: 6229a4a7-be42-4e2a-af9d-695c4759a4ef
keywords:
- Multimédia Windows, MIDI (Musical Instrument Digital Interface)
- multimédia, MIDI (Musical Instrument Digital Interface)
- audio multimédia, MIDI (Musical Instrument Digital Interface)
- audio, MIDI (Musical Instrument Digital Interface)
- Windows Multimedia, référence MIDI
- multimédia, référence MIDI
- audio multimédia, référence MIDI
- audio, référence MIDI
- Informations de référence sur l’interface MIDI (Musical Instrument Digital Interface)
- MIDI (Musical Instrument Digital Interface), référence
- référence pour MIDI, à propos de
- Référence MIDI, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c21542867faf1e09d68dc4fc81a50d25f56b5c5e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381902"
---
# <a name="midi-reference"></a><span data-ttu-id="5af07-115">Informations de référence MIDI</span><span class="sxs-lookup"><span data-stu-id="5af07-115">MIDI Reference</span></span>

<span data-ttu-id="5af07-116">Cette section décrit les fonctions, les macros, les messages et les structures associés à l’interface MIDI (Musical Instrument Digital Interface).</span><span class="sxs-lookup"><span data-stu-id="5af07-116">This section describes the functions, macros, messages, and structures associated with the Musical Instrument Digital Interface (MIDI).</span></span> <span data-ttu-id="5af07-117">Ces éléments sont regroupés comme suit.</span><span class="sxs-lookup"><span data-stu-id="5af07-117">These elements are grouped as follows.</span></span>

## <a name="allocating-and-managing-buffers"></a><span data-ttu-id="5af07-118">Allocation et gestion des mémoires tampons</span><span class="sxs-lookup"><span data-stu-id="5af07-118">Allocating and Managing Buffers</span></span>

-   [<span data-ttu-id="5af07-119">**MIDIHDR**</span><span class="sxs-lookup"><span data-stu-id="5af07-119">**MIDIHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)
-   [<span data-ttu-id="5af07-120">**midiInAddBuffer**</span><span class="sxs-lookup"><span data-stu-id="5af07-120">**midiInAddBuffer**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)
-   [<span data-ttu-id="5af07-121">**midiInPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="5af07-121">**midiInPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)
-   [<span data-ttu-id="5af07-122">**midiInUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="5af07-122">**midiInUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)
-   [<span data-ttu-id="5af07-123">**midiOutPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="5af07-123">**midiOutPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)
-   [<span data-ttu-id="5af07-124">**midiOutUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="5af07-124">**midiOutUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader)

## <a name="callback-functions"></a><span data-ttu-id="5af07-125">Fonctions de rappel</span><span class="sxs-lookup"><span data-stu-id="5af07-125">Callback Functions</span></span>

-   <span data-ttu-id="5af07-126">[**MidiInProc**](/previous-versions//dd798460(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5af07-126">[**MidiInProc**](/previous-versions//dd798460(v=vs.85))</span></span>
-   <span data-ttu-id="5af07-127">[**MidiOutProc**](/previous-versions//dd798478(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5af07-127">[**MidiOutProc**](/previous-versions//dd798478(v=vs.85))</span></span>

## <a name="device-capabilities"></a><span data-ttu-id="5af07-128">Fonctionnalités de l’appareil</span><span class="sxs-lookup"><span data-stu-id="5af07-128">Device Capabilities</span></span>

-   [<span data-ttu-id="5af07-129">**MIDIINCAPS**</span><span class="sxs-lookup"><span data-stu-id="5af07-129">**MIDIINCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps)
-   [<span data-ttu-id="5af07-130">**midiInGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="5af07-130">**midiInGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps)
-   [<span data-ttu-id="5af07-131">**midiInGetID**</span><span class="sxs-lookup"><span data-stu-id="5af07-131">**midiInGetID**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetid)
-   [<span data-ttu-id="5af07-132">**midiInGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="5af07-132">**midiInGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs)
-   [<span data-ttu-id="5af07-133">**MIDIOUTCAPS**</span><span class="sxs-lookup"><span data-stu-id="5af07-133">**MIDIOUTCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps)
-   [<span data-ttu-id="5af07-134">**midiOutGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="5af07-134">**midiOutGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps)
-   [<span data-ttu-id="5af07-135">**midiOutGetID**</span><span class="sxs-lookup"><span data-stu-id="5af07-135">**midiOutGetID**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetid)
-   [<span data-ttu-id="5af07-136">**midiOutGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="5af07-136">**midiOutGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs)
-   [<span data-ttu-id="5af07-137">**MIDISTRMBUFFVER**</span><span class="sxs-lookup"><span data-stu-id="5af07-137">**MIDISTRMBUFFVER**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midistrmbuffver)

## <a name="error-processing"></a><span data-ttu-id="5af07-138">Erreur lors du traitement</span><span class="sxs-lookup"><span data-stu-id="5af07-138">Error Processing</span></span>

-   [<span data-ttu-id="5af07-139">**midiInGetErrorText**</span><span class="sxs-lookup"><span data-stu-id="5af07-139">**midiInGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext)
-   [<span data-ttu-id="5af07-140">**midiOutGetErrorText**</span><span class="sxs-lookup"><span data-stu-id="5af07-140">**midiOutGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext)
-   [<span data-ttu-id="5af07-141">**\_erreur MIM**</span><span class="sxs-lookup"><span data-stu-id="5af07-141">**MIM\_ERROR**</span></span>](mim-error.md)
-   [<span data-ttu-id="5af07-142">**\_LONGERROR MIM**</span><span class="sxs-lookup"><span data-stu-id="5af07-142">**MIM\_LONGERROR**</span></span>](mim-longerror.md)
-   [<span data-ttu-id="5af07-143">**MM \_ \_ erreur MIM**</span><span class="sxs-lookup"><span data-stu-id="5af07-143">**MM\_MIM\_ERROR**</span></span>](mm-mim-error.md)
-   [<span data-ttu-id="5af07-144">**MM \_ \_ LONGERROR MIM**</span><span class="sxs-lookup"><span data-stu-id="5af07-144">**MM\_MIM\_LONGERROR**</span></span>](mm-mim-longerror.md)

## <a name="managing-midi-streams"></a><span data-ttu-id="5af07-145">Gestion des flux MIDI</span><span class="sxs-lookup"><span data-stu-id="5af07-145">Managing MIDI Streams</span></span>

-   [<span data-ttu-id="5af07-146">**midiStreamClose**</span><span class="sxs-lookup"><span data-stu-id="5af07-146">**midiStreamClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)
-   [<span data-ttu-id="5af07-147">**midiStreamOpen**</span><span class="sxs-lookup"><span data-stu-id="5af07-147">**midiStreamOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)
-   [<span data-ttu-id="5af07-148">**midiStreamOut**</span><span class="sxs-lookup"><span data-stu-id="5af07-148">**midiStreamOut**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)
-   [<span data-ttu-id="5af07-149">**midiStreamPause**</span><span class="sxs-lookup"><span data-stu-id="5af07-149">**midiStreamPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)
-   [<span data-ttu-id="5af07-150">**midiStreamPosition**</span><span class="sxs-lookup"><span data-stu-id="5af07-150">**midiStreamPosition**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition)
-   [<span data-ttu-id="5af07-151">**midiStreamProperty**</span><span class="sxs-lookup"><span data-stu-id="5af07-151">**midiStreamProperty**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamproperty)
-   [<span data-ttu-id="5af07-152">**midiStreamRestart**</span><span class="sxs-lookup"><span data-stu-id="5af07-152">**midiStreamRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)
-   [<span data-ttu-id="5af07-153">**midiStreamStop**</span><span class="sxs-lookup"><span data-stu-id="5af07-153">**midiStreamStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)

## <a name="opening-and-closing-devices"></a><span data-ttu-id="5af07-154">Ouverture et fermeture des appareils</span><span class="sxs-lookup"><span data-stu-id="5af07-154">Opening and Closing Devices</span></span>

-   [<span data-ttu-id="5af07-155">**midiInClose**</span><span class="sxs-lookup"><span data-stu-id="5af07-155">**midiInClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)
-   [<span data-ttu-id="5af07-156">**midiInOpen**</span><span class="sxs-lookup"><span data-stu-id="5af07-156">**midiInOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)
-   [<span data-ttu-id="5af07-157">**midiOutClose**</span><span class="sxs-lookup"><span data-stu-id="5af07-157">**midiOutClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose)
-   [<span data-ttu-id="5af07-158">**midiOutOpen**</span><span class="sxs-lookup"><span data-stu-id="5af07-158">**midiOutOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)
-   [<span data-ttu-id="5af07-159">**\_fermeture MIM**</span><span class="sxs-lookup"><span data-stu-id="5af07-159">**MIM\_CLOSE**</span></span>](mim-close.md)
-   [<span data-ttu-id="5af07-160">**MIM \_ ouvert**</span><span class="sxs-lookup"><span data-stu-id="5af07-160">**MIM\_OPEN**</span></span>](mim-open.md)
-   [<span data-ttu-id="5af07-161">**MM \_ MIM \_ proche**</span><span class="sxs-lookup"><span data-stu-id="5af07-161">**MM\_MIM\_CLOSE**</span></span>](mm-mim-close.md)
-   [<span data-ttu-id="5af07-162">**MM \_ MIM \_ ouvert**</span><span class="sxs-lookup"><span data-stu-id="5af07-162">**MM\_MIM\_OPEN**</span></span>](mm-mim-open.md)
-   [<span data-ttu-id="5af07-163">**\_fermeture MOM de mm \_**</span><span class="sxs-lookup"><span data-stu-id="5af07-163">**MM\_MOM\_CLOSE**</span></span>](mm-mom-close.md)
-   [<span data-ttu-id="5af07-164">**\_ouverture de MOM mm \_**</span><span class="sxs-lookup"><span data-stu-id="5af07-164">**MM\_MOM\_OPEN**</span></span>](mm-mom-open.md)
-   [<span data-ttu-id="5af07-165">**\_fermeture MOM**</span><span class="sxs-lookup"><span data-stu-id="5af07-165">**MOM\_CLOSE**</span></span>](mom-close.md)
-   [<span data-ttu-id="5af07-166">**MOM \_ ouvert**</span><span class="sxs-lookup"><span data-stu-id="5af07-166">**MOM\_OPEN**</span></span>](mom-open.md)

## <a name="output-devices"></a><span data-ttu-id="5af07-167">Périphériques de sortie</span><span class="sxs-lookup"><span data-stu-id="5af07-167">Output Devices</span></span>

-   [<span data-ttu-id="5af07-168">Tableau de la matrice</span><span class="sxs-lookup"><span data-stu-id="5af07-168">KEYARRAY</span></span>](keyarray.md)
-   [<span data-ttu-id="5af07-169">**midiOutCacheDrumPatches**</span><span class="sxs-lookup"><span data-stu-id="5af07-169">**midiOutCacheDrumPatches**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches)
-   [<span data-ttu-id="5af07-170">**midiOutCachePatches**</span><span class="sxs-lookup"><span data-stu-id="5af07-170">**midiOutCachePatches**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)
-   [<span data-ttu-id="5af07-171">**midiOutGetVolume**</span><span class="sxs-lookup"><span data-stu-id="5af07-171">**midiOutGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume)
-   [<span data-ttu-id="5af07-172">**midiOutSetVolume**</span><span class="sxs-lookup"><span data-stu-id="5af07-172">**midiOutSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume)
-   [<span data-ttu-id="5af07-173">PATCHARRAY</span><span class="sxs-lookup"><span data-stu-id="5af07-173">PATCHARRAY</span></span>](patcharray.md)

## <a name="playing-a-message-or-messages"></a><span data-ttu-id="5af07-174">La diffusion d’un message ou de messages</span><span class="sxs-lookup"><span data-stu-id="5af07-174">Playing a Message or Messages</span></span>

-   [<span data-ttu-id="5af07-175">**MEVT \_ EVENTPARM**</span><span class="sxs-lookup"><span data-stu-id="5af07-175">**MEVT\_EVENTPARM**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm)
-   [<span data-ttu-id="5af07-176">**\_eventType MEVT**</span><span class="sxs-lookup"><span data-stu-id="5af07-176">**MEVT\_EVENTTYPE**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype)
-   [<span data-ttu-id="5af07-177">**MIDIEVENT**</span><span class="sxs-lookup"><span data-stu-id="5af07-177">**MIDIEVENT**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midievent)
-   [<span data-ttu-id="5af07-178">**midiOutLongMsg**</span><span class="sxs-lookup"><span data-stu-id="5af07-178">**midiOutLongMsg**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)
-   [<span data-ttu-id="5af07-179">**midiOutReset**</span><span class="sxs-lookup"><span data-stu-id="5af07-179">**midiOutReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)
-   [<span data-ttu-id="5af07-180">**midiOutShortMsg**</span><span class="sxs-lookup"><span data-stu-id="5af07-180">**midiOutShortMsg**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg)
-   [<span data-ttu-id="5af07-181">**midiStreamOut**</span><span class="sxs-lookup"><span data-stu-id="5af07-181">**midiStreamOut**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)
-   [<span data-ttu-id="5af07-182">**midiStreamPause**</span><span class="sxs-lookup"><span data-stu-id="5af07-182">**midiStreamPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)
-   [<span data-ttu-id="5af07-183">**midiStreamRestart**</span><span class="sxs-lookup"><span data-stu-id="5af07-183">**midiStreamRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)
-   [<span data-ttu-id="5af07-184">**midiStreamStop**</span><span class="sxs-lookup"><span data-stu-id="5af07-184">**midiStreamStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)
-   [<span data-ttu-id="5af07-185">**MM \_ MOM \_ terminé**</span><span class="sxs-lookup"><span data-stu-id="5af07-185">**MM\_MOM\_DONE**</span></span>](mm-mom-done.md)
-   [<span data-ttu-id="5af07-186">**MM \_ \_ POSITIONCB MOM**</span><span class="sxs-lookup"><span data-stu-id="5af07-186">**MM\_MOM\_POSITIONCB**</span></span>](mm-mom-positioncb.md)
-   [<span data-ttu-id="5af07-187">**MOM \_ terminé**</span><span class="sxs-lookup"><span data-stu-id="5af07-187">**MOM\_DONE**</span></span>](mom-done.md)
-   [<span data-ttu-id="5af07-188">**\_POSITIONCB MOM**</span><span class="sxs-lookup"><span data-stu-id="5af07-188">**MOM\_POSITIONCB**</span></span>](mom-positioncb.md)

## <a name="recording"></a><span data-ttu-id="5af07-189">Enregistrement</span><span class="sxs-lookup"><span data-stu-id="5af07-189">Recording</span></span>

-   [<span data-ttu-id="5af07-190">**midiConnect**</span><span class="sxs-lookup"><span data-stu-id="5af07-190">**midiConnect**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiconnect)
-   [<span data-ttu-id="5af07-191">**midiDisconnect**</span><span class="sxs-lookup"><span data-stu-id="5af07-191">**midiDisconnect**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mididisconnect)
-   [<span data-ttu-id="5af07-192">**midiInReset**</span><span class="sxs-lookup"><span data-stu-id="5af07-192">**midiInReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)
-   [<span data-ttu-id="5af07-193">**midiInStart**</span><span class="sxs-lookup"><span data-stu-id="5af07-193">**midiInStart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)
-   [<span data-ttu-id="5af07-194">**midiInStop**</span><span class="sxs-lookup"><span data-stu-id="5af07-194">**midiInStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)
-   [<span data-ttu-id="5af07-195">**MIDIPROPTEMPO**</span><span class="sxs-lookup"><span data-stu-id="5af07-195">**MIDIPROPTEMPO**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midiproptempo)
-   [<span data-ttu-id="5af07-196">**MIDIPROPTIMEDIV**</span><span class="sxs-lookup"><span data-stu-id="5af07-196">**MIDIPROPTIMEDIV**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midiproptimediv)
-   [<span data-ttu-id="5af07-197">**\_données MIM**</span><span class="sxs-lookup"><span data-stu-id="5af07-197">**MIM\_DATA**</span></span>](mim-data.md)
-   [<span data-ttu-id="5af07-198">**\_LONGDATA MIM**</span><span class="sxs-lookup"><span data-stu-id="5af07-198">**MIM\_LONGDATA**</span></span>](mim-longdata.md)
-   [<span data-ttu-id="5af07-199">**\_MOREDATA MIM**</span><span class="sxs-lookup"><span data-stu-id="5af07-199">**MIM\_MOREDATA**</span></span>](mim-moredata.md)
-   [<span data-ttu-id="5af07-200">**MM \_ \_ données MIM**</span><span class="sxs-lookup"><span data-stu-id="5af07-200">**MM\_MIM\_DATA**</span></span>](mm-mim-data.md)
-   [<span data-ttu-id="5af07-201">**MM \_ \_ MOREDATA MIM**</span><span class="sxs-lookup"><span data-stu-id="5af07-201">**MM\_MIM\_MOREDATA**</span></span>](mm-mim-moredata.md)
-   [<span data-ttu-id="5af07-202">**MM \_ \_ LONGDATA MIM**</span><span class="sxs-lookup"><span data-stu-id="5af07-202">**MM\_MIM\_LONGDATA**</span></span>](mm-mim-longdata.md)

## <a name="sending-messages-to-devices"></a><span data-ttu-id="5af07-203">Envoi de messages à des appareils</span><span class="sxs-lookup"><span data-stu-id="5af07-203">Sending Messages to Devices</span></span>

-   [<span data-ttu-id="5af07-204">**midiInMessage**</span><span class="sxs-lookup"><span data-stu-id="5af07-204">**midiInMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinmessage)
-   [<span data-ttu-id="5af07-205">**midiOutMessage**</span><span class="sxs-lookup"><span data-stu-id="5af07-205">**midiOutMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutmessage)

## <a name="related-topics"></a><span data-ttu-id="5af07-206">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5af07-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5af07-207">Interface MIDI (Musical Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="5af07-207">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> </dl>

 

 
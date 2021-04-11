---
title: Référence sur l’audio Waveform
description: Cette section répertorie les fonctions, structures et messages associés à la forme d’onde audio, qui sont documentées sous référence multimédia. Ces éléments sont regroupés comme suit.
ms.assetid: 723953f7-b38e-4f24-8d54-9849e013011d
keywords:
- Windows Multimedia, référence audio Waveform
- multimédia, référence audio de forme d’onde
- audio multimédia, référence de forme d’onde
- audio, référence de forme d’onde
- Multimédia Windows, Waveform Audio
- multimédia, audio Waveform
- audio multimédia, forme d’onde
- audio, forme d’onde
- onde audio, référence
- Référence audio Waveform, à propos de
- référence pour wavefore audio, à propos de
- Référence audio Waveform, appareils auxiliaires
- référence pour wavefore audio, appareils auxiliaires
- Référence audio Waveform, lecture
- référence pour l’audio wavefore, lecture
- Référence audio Waveform, Erreurs
- référence pour wavefore audio, Erreurs
- Référence audio Waveform, ouverture
- référence pour l’audio wavefore, ouverture
- Référence audio Waveform, fermeture
- référence pour l’audio wavefore, fermeture
- Référence audio Waveform, inclinaison
- référence pour l’audio wavefore, la tonalité
- Référence audio Waveform, volume
- référence pour wavefore audio, volume
- Référence audio Waveform, messages
- informations de référence sur l’audio wavefore, messages
- Référence audio de forme d’onde, position actuelle
- référence pour l’audio wavefore, position actuelle
- Référence audio Waveform, enregistrement
- informations de référence sur l’audio wavefore, enregistrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c74b37984b2d3fab5dad1ea0df4f1f62dfa1855e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031150"
---
# <a name="waveform-audio-reference"></a><span data-ttu-id="52911-135">Référence sur l’audio Waveform</span><span class="sxs-lookup"><span data-stu-id="52911-135">Waveform Audio Reference</span></span>

<span data-ttu-id="52911-136">Cette section répertorie les fonctions, structures et messages associés à la forme d’onde audio, qui sont documentées sous [référence multimédia](multimedia-reference.md).</span><span class="sxs-lookup"><span data-stu-id="52911-136">This section lists the functions, structures, and messages associated with waveform audio, which are documented under [Multimedia Reference](multimedia-reference.md).</span></span> <span data-ttu-id="52911-137">Ces éléments sont regroupés comme suit.</span><span class="sxs-lookup"><span data-stu-id="52911-137">These elements are grouped as follows.</span></span>

## <a name="auxiliary-devices"></a><span data-ttu-id="52911-138">Périphériques auxiliaires</span><span class="sxs-lookup"><span data-stu-id="52911-138">Auxiliary Devices</span></span>

-   [<span data-ttu-id="52911-139">**AUXCAPS**</span><span class="sxs-lookup"><span data-stu-id="52911-139">**AUXCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps)
-   [<span data-ttu-id="52911-140">**auxGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="52911-140">**auxGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)
-   [<span data-ttu-id="52911-141">**auxGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="52911-141">**auxGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)
-   [<span data-ttu-id="52911-142">**auxGetVolume**</span><span class="sxs-lookup"><span data-stu-id="52911-142">**auxGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxgetvolume)
-   [<span data-ttu-id="52911-143">**auxOutMessage**</span><span class="sxs-lookup"><span data-stu-id="52911-143">**auxOutMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxoutmessage)
-   [<span data-ttu-id="52911-144">**auxSetVolume**</span><span class="sxs-lookup"><span data-stu-id="52911-144">**auxSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxsetvolume)

## <a name="easy-playback"></a><span data-ttu-id="52911-145">Lecture facile</span><span class="sxs-lookup"><span data-stu-id="52911-145">Easy Playback</span></span>

-   <span data-ttu-id="52911-146">[**PlaySound**](/previous-versions//dd743680(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="52911-146">[**PlaySound**](/previous-versions//dd743680(v=vs.85))</span></span>
-   <span data-ttu-id="52911-147">[**sndPlaySound**](/previous-versions//dd798676(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="52911-147">[**sndPlaySound**](/previous-versions//dd798676(v=vs.85))</span></span>

## <a name="errors"></a><span data-ttu-id="52911-148">Erreurs</span><span class="sxs-lookup"><span data-stu-id="52911-148">Errors</span></span>

-   [<span data-ttu-id="52911-149">**waveInGetErrorText**</span><span class="sxs-lookup"><span data-stu-id="52911-149">**waveInGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingeterrortext)
-   [<span data-ttu-id="52911-150">**waveOutGetErrorText**</span><span class="sxs-lookup"><span data-stu-id="52911-150">**waveOutGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgeterrortext)

## <a name="opening-and-closing"></a><span data-ttu-id="52911-151">Ouverture et fermeture</span><span class="sxs-lookup"><span data-stu-id="52911-151">Opening and Closing</span></span>

-   [<span data-ttu-id="52911-152">**PCMWAVEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="52911-152">**PCMWAVEFORMAT**</span></span>](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat)
-   [<span data-ttu-id="52911-153">**\_fermeture de Wim de mm \_**</span><span class="sxs-lookup"><span data-stu-id="52911-153">**MM\_WIM\_CLOSE**</span></span>](mm-wim-close.md)
-   [<span data-ttu-id="52911-154">**fichier \_ Wim \_ Open**</span><span class="sxs-lookup"><span data-stu-id="52911-154">**MM\_WIM\_OPEN**</span></span>](mm-wim-open.md)
-   [<span data-ttu-id="52911-155">**MM \_ WOM \_ Fermer**</span><span class="sxs-lookup"><span data-stu-id="52911-155">**MM\_WOM\_CLOSE**</span></span>](mm-wom-close.md)
-   [<span data-ttu-id="52911-156">**MM \_ WOM \_ ouverts**</span><span class="sxs-lookup"><span data-stu-id="52911-156">**MM\_WOM\_OPEN**</span></span>](mm-wom-open.md)
-   [<span data-ttu-id="52911-157">**WAVEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="52911-157">**WAVEFORMAT**</span></span>](/windows/win32/api/mmreg/ns-mmreg-waveformat)
-   [<span data-ttu-id="52911-158">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="52911-158">**WAVEFORMATEX**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex)
-   [<span data-ttu-id="52911-159">**waveInClose**</span><span class="sxs-lookup"><span data-stu-id="52911-159">**waveInClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose)
-   <span data-ttu-id="52911-160">[**waveInProc**](/previous-versions//dd743849(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="52911-160">[**waveInProc**](/previous-versions//dd743849(v=vs.85))</span></span>
-   [<span data-ttu-id="52911-161">**waveInOpen**</span><span class="sxs-lookup"><span data-stu-id="52911-161">**waveInOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen)
-   [<span data-ttu-id="52911-162">**waveOutClose**</span><span class="sxs-lookup"><span data-stu-id="52911-162">**waveOutClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose)
-   <span data-ttu-id="52911-163">[**waveOutProc**](/previous-versions//dd743869(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="52911-163">[**waveOutProc**](/previous-versions//dd743869(v=vs.85))</span></span>
-   [<span data-ttu-id="52911-164">**waveOutOpen**</span><span class="sxs-lookup"><span data-stu-id="52911-164">**waveOutOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen)
-   [<span data-ttu-id="52911-165">**fermeture de WIM \_**</span><span class="sxs-lookup"><span data-stu-id="52911-165">**WIM\_CLOSE**</span></span>](wim-close.md)
-   [<span data-ttu-id="52911-166">**\_ouvrir Wim**</span><span class="sxs-lookup"><span data-stu-id="52911-166">**WIM\_OPEN**</span></span>](wim-open.md)
-   [<span data-ttu-id="52911-167">**WOM \_ Fermer**</span><span class="sxs-lookup"><span data-stu-id="52911-167">**WOM\_CLOSE**</span></span>](wom-close.md)
-   [<span data-ttu-id="52911-168">**WOM \_ ouvrir**</span><span class="sxs-lookup"><span data-stu-id="52911-168">**WOM\_OPEN**</span></span>](wom-open.md)

## <a name="pitch"></a><span data-ttu-id="52911-169">Inclinaison</span><span class="sxs-lookup"><span data-stu-id="52911-169">Pitch</span></span>

-   [<span data-ttu-id="52911-170">**waveOutGetPitch**</span><span class="sxs-lookup"><span data-stu-id="52911-170">**waveOutGetPitch**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetpitch)
-   [<span data-ttu-id="52911-171">**waveOutSetPitch**</span><span class="sxs-lookup"><span data-stu-id="52911-171">**waveOutSetPitch**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetpitch)

## <a name="playback-rate"></a><span data-ttu-id="52911-172">Vitesse de lecture</span><span class="sxs-lookup"><span data-stu-id="52911-172">Playback Rate</span></span>

-   [<span data-ttu-id="52911-173">**waveOutGetPlaybackRate**</span><span class="sxs-lookup"><span data-stu-id="52911-173">**waveOutGetPlaybackRate**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetplaybackrate)
-   [<span data-ttu-id="52911-174">**waveOutSetPlaybackRate**</span><span class="sxs-lookup"><span data-stu-id="52911-174">**waveOutSetPlaybackRate**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetplaybackrate)

## <a name="playback-progress"></a><span data-ttu-id="52911-175">Progression de la lecture</span><span class="sxs-lookup"><span data-stu-id="52911-175">Playback Progress</span></span>

-   [<span data-ttu-id="52911-176">**MM \_ WOM \_ terminé**</span><span class="sxs-lookup"><span data-stu-id="52911-176">**MM\_WOM\_DONE**</span></span>](mm-wom-done.md)
-   [<span data-ttu-id="52911-177">**waveOutBreakLoop**</span><span class="sxs-lookup"><span data-stu-id="52911-177">**waveOutBreakLoop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop)
-   [<span data-ttu-id="52911-178">**waveOutPause**</span><span class="sxs-lookup"><span data-stu-id="52911-178">**waveOutPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)
-   [<span data-ttu-id="52911-179">**waveOutReset**</span><span class="sxs-lookup"><span data-stu-id="52911-179">**waveOutReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)
-   [<span data-ttu-id="52911-180">**waveOutRestart**</span><span class="sxs-lookup"><span data-stu-id="52911-180">**waveOutRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart)
-   [<span data-ttu-id="52911-181">**WOM \_ terminé**</span><span class="sxs-lookup"><span data-stu-id="52911-181">**WOM\_DONE**</span></span>](wom-done.md)

## <a name="playing"></a><span data-ttu-id="52911-182">Lecture en cours</span><span class="sxs-lookup"><span data-stu-id="52911-182">Playing</span></span>

-   [<span data-ttu-id="52911-183">**MM \_ WOM \_ terminé**</span><span class="sxs-lookup"><span data-stu-id="52911-183">**MM\_WOM\_DONE**</span></span>](mm-wom-done.md)
-   [<span data-ttu-id="52911-184">**WAVEHDR**</span><span class="sxs-lookup"><span data-stu-id="52911-184">**WAVEHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)
-   [<span data-ttu-id="52911-185">**waveOutPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="52911-185">**waveOutPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)
-   [<span data-ttu-id="52911-186">**waveOutUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="52911-186">**waveOutUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader)
-   [<span data-ttu-id="52911-187">**waveOutWrite**</span><span class="sxs-lookup"><span data-stu-id="52911-187">**waveOutWrite**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite)
-   [<span data-ttu-id="52911-188">**WOM \_ terminé**</span><span class="sxs-lookup"><span data-stu-id="52911-188">**WOM\_DONE**</span></span>](wom-done.md)

## <a name="querying-a-device"></a><span data-ttu-id="52911-189">Interrogation d’un appareil</span><span class="sxs-lookup"><span data-stu-id="52911-189">Querying a Device</span></span>

-   [<span data-ttu-id="52911-190">**WAVEINCAPS**</span><span class="sxs-lookup"><span data-stu-id="52911-190">**WAVEINCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)
-   [<span data-ttu-id="52911-191">**waveInGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="52911-191">**waveInGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)
-   [<span data-ttu-id="52911-192">**waveInGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="52911-192">**waveInGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)
-   [<span data-ttu-id="52911-193">**WAVEOUTCAPS**</span><span class="sxs-lookup"><span data-stu-id="52911-193">**WAVEOUTCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)
-   [<span data-ttu-id="52911-194">**waveOutGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="52911-194">**waveOutGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps)
-   [<span data-ttu-id="52911-195">**waveOutGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="52911-195">**waveOutGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs)

## <a name="recording"></a><span data-ttu-id="52911-196">Enregistrement</span><span class="sxs-lookup"><span data-stu-id="52911-196">Recording</span></span>

-   [<span data-ttu-id="52911-197">**\_données Wim \_ mm**</span><span class="sxs-lookup"><span data-stu-id="52911-197">**MM\_WIM\_DATA**</span></span>](mm-wim-data.md)
-   [<span data-ttu-id="52911-198">**waveInAddBuffer**</span><span class="sxs-lookup"><span data-stu-id="52911-198">**waveInAddBuffer**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer)
-   [<span data-ttu-id="52911-199">**waveInPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="52911-199">**waveInPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader)
-   [<span data-ttu-id="52911-200">**waveInReset**</span><span class="sxs-lookup"><span data-stu-id="52911-200">**waveInReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)
-   [<span data-ttu-id="52911-201">**waveInStart**</span><span class="sxs-lookup"><span data-stu-id="52911-201">**waveInStart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)
-   [<span data-ttu-id="52911-202">**waveInStop**</span><span class="sxs-lookup"><span data-stu-id="52911-202">**waveInStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinstop)
-   [<span data-ttu-id="52911-203">**waveInUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="52911-203">**waveInUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader)
-   [<span data-ttu-id="52911-204">**\_données Wim**</span><span class="sxs-lookup"><span data-stu-id="52911-204">**WIM\_DATA**</span></span>](wim-data.md)

## <a name="retrieving-device-identifiers"></a><span data-ttu-id="52911-205">Récupération des identificateurs d’appareil</span><span class="sxs-lookup"><span data-stu-id="52911-205">Retrieving Device Identifiers</span></span>

-   [<span data-ttu-id="52911-206">**waveInGetID**</span><span class="sxs-lookup"><span data-stu-id="52911-206">**waveInGetID**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingetid)
-   [<span data-ttu-id="52911-207">**waveOutGetID**</span><span class="sxs-lookup"><span data-stu-id="52911-207">**waveOutGetID**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetid)

## <a name="retrieving-the-current-position"></a><span data-ttu-id="52911-208">Récupération de la position actuelle</span><span class="sxs-lookup"><span data-stu-id="52911-208">Retrieving the Current Position</span></span>

-   [<span data-ttu-id="52911-209">**waveInGetPosition**</span><span class="sxs-lookup"><span data-stu-id="52911-209">**waveInGetPosition**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingetposition)
-   [<span data-ttu-id="52911-210">**waveOutGetPosition**</span><span class="sxs-lookup"><span data-stu-id="52911-210">**waveOutGetPosition**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition)

## <a name="sending-custom-messages"></a><span data-ttu-id="52911-211">Envoi de messages personnalisés</span><span class="sxs-lookup"><span data-stu-id="52911-211">Sending Custom Messages</span></span>

-   [<span data-ttu-id="52911-212">**waveInMessage**</span><span class="sxs-lookup"><span data-stu-id="52911-212">**waveInMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinmessage)
-   [<span data-ttu-id="52911-213">**waveOutMessage**</span><span class="sxs-lookup"><span data-stu-id="52911-213">**waveOutMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutmessage)

## <a name="volume"></a><span data-ttu-id="52911-214">Volume</span><span class="sxs-lookup"><span data-stu-id="52911-214">Volume</span></span>

-   [<span data-ttu-id="52911-215">**waveOutGetVolume**</span><span class="sxs-lookup"><span data-stu-id="52911-215">**waveOutGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetvolume)
-   [<span data-ttu-id="52911-216">**waveOutSetVolume**</span><span class="sxs-lookup"><span data-stu-id="52911-216">**waveOutSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetvolume)

## <a name="related-topics"></a><span data-ttu-id="52911-217">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="52911-217">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52911-218">Sons Waveform</span><span class="sxs-lookup"><span data-stu-id="52911-218">Waveform Audio</span></span>](waveform-audio.md)
</dt> </dl>

 

 
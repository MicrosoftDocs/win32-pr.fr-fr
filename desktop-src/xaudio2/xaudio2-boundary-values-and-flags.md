---
description: Constantes XAudio2 qui spécifient des paramètres par défaut, des valeurs maximales et des indicateurs.
ms.assetid: 074ac40e-a17e-7366-1954-6699407b82f7
title: Valeurs limites et indicateurs XAudio2 (Xaudio2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe59f229ea406eb5bf6c6b3f5c124d6d0d19c047
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521709"
---
# <a name="xaudio2-boundary-values-and-flags"></a>Valeurs limites et indicateurs XAudio2

Constantes XAudio2 qui spécifient des paramètres par défaut, des valeurs maximales et des indicateurs.

**Valeurs limites de XAudio2**



| Constante                                                                                                                                                                                                     | Description                                                                                                                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_MAX_BUFFER_BYTES"></span><span id="xaudio2_max_buffer_bytes"></span><dl> <dt>**\_Nombre maximal d’octets dans le \_ tampon XAUDIO2 \_**</dt> </dl>             | Valeur maximale autorisée pour [**la \_ mémoire tampon XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer). AudioBytes.<br/>                                                      |
| <span id="XAUDIO2_MAX_QUEUED_BUFFERS"></span><span id="xaudio2_max_queued_buffers"></span><dl> <dt>**\_ \_ Tampons XAUDIO2 Max mis en file d’attente \_**</dt> </dl>       | Nombre maximal de mémoires tampons autorisées dans une file d’attente vocale.<br/>                                                                                            |
| <span id="XAUDIO2_MAX_BUFFERS_SYSTEM"></span><span id="xaudio2_max_buffers_system"></span><dl> <dt>**\_Système de \_ mémoires tampons Max XAUDIO2 \_**</dt> </dl>       | Nombre maximal de mémoires tampons autorisées pour les threads système (Xbox 360 uniquement).<br/>                                                                          |
| <span id="XAUDIO2_MAX_AUDIO_CHANNELS"></span><span id="xaudio2_max_audio_channels"></span><dl> <dt>**\_Nombre maximal \_ de \_ canaux audio XAUDIO2**</dt> </dl>       | Valeur maximale autorisée pour **WAVEFORMATEX. nChannels**.<br/>                                                                                |
| <span id="XAUDIO2_MIN_SAMPLE_RATE"></span><span id="xaudio2_min_sample_rate"></span><dl> <dt>**\_Taux d' \_ échantillonnage \_ min. XAUDIO2**</dt> </dl>                | Taux d’échantillonnage audio minimal pris en charge.<br/>                                                                                                 |
| <span id="XAUDIO2_MAX_SAMPLE_RATE"></span><span id="xaudio2_max_sample_rate"></span><dl> <dt>**\_Taux d' \_ échantillonnage \_ Max XAUDIO2**</dt> </dl>                | Taux d’échantillonnage audio maximal pris en charge.<br/>                                                                                                 |
| <span id="XAUDIO2_MAX_VOLUME_LEVEL"></span><span id="xaudio2_max_volume_level"></span><dl> <dt>**\_Niveau de \_ volume \_ Max XAUDIO2**</dt> </dl>             | Niveau de volume maximal autorisé.<br/>                                                                                                        |
| <span id="XAUDIO2_MIN_FREQ_RATIO"></span><span id="xaudio2_min_freq_ratio"></span><dl> <dt>**XAUDIO2 \_ Min \_ \_ fréquence**</dt> </dl>                   | Taux de fréquence minimal autorisé dans une voix source.<br/>                                                                                   |
| <span id="XAUDIO2_MAX_FREQ_RATIO"></span><span id="xaudio2_max_freq_ratio"></span><dl> <dt>**Taux de XAUDIO2 \_ Max. \_ \_**</dt> </dl>                   | Taux de fréquence maximal autorisé dans une voix source.<br/>                                                                                   |
| <span id="XAUDIO2_DEFAULT_FREQ_RATIO"></span><span id="xaudio2_default_freq_ratio"></span><dl> <dt>**XAUDIO2 \_ \_ taux de \_ fréquence par défaut**</dt> </dl>       | Valeur par défaut de l’argument **MaxFrequencyRatio** de [**IXAudio2 :: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice).<br/> |
| <span id="XAUDIO2_MAX_FILTER_ONEOVERQ"></span><span id="xaudio2_max_filter_oneoverq"></span><dl> <dt>**XAUDIO2 \_ \_ filtre Max \_ ONEOVERQ**</dt> </dl>    | Valeur maximale pour [**les \_ \_ paramètres de filtre XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters).**OneOverQ**.<br/>                                     |
| <span id="XAUDIO2_MAX_FILTER_FREQUENCY"></span><span id="xaudio2_max_filter_frequency"></span><dl> <dt>**\_Fréquence du \_ filtre \_ Max XAUDIO2**</dt> </dl> | Valeur maximale pour [**les \_ \_ paramètres de filtre XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters).**Fréquence**.<br/>                                    |
| <span id="XAUDIO2_MAX_LOOP_COUNT"></span><span id="xaudio2_max_loop_count"></span><dl> <dt>**\_Nombre maximal de \_ boucles \_ XAUDIO2**</dt> </dl>                   | Valeur maximale qui ne sera pas traitée comme une boucle infinie pour la [**\_ mémoire tampon XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**LoopCount**.<br/>              |
| <span id="XAUDIO2_MAX_INSTANCES"></span><span id="xaudio2_max_instances"></span><dl> <dt>**\_Nombre maximal d' \_ instances XAUDIO2**</dt> </dl>                       | Nombre maximal d’instances simultanées de XAudio2 autorisées sur Xbox 360.<br/>                                                                       |



**Valeurs XAudio2 avec une signification spéciale**



| Constante                                                                                                                                                                                              | Description                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_COMMIT_NOW"></span><span id="xaudio2_commit_now"></span><dl> <dt>**XAUDIO2 \_ valider \_ maintenant**</dt> </dl>                         | Utilisé comme paramètre pour les méthodes avec un argument OperationSet. Pour plus d’informations, consultez [jeux d’opérations XAudio2](xaudio2-operation-sets.md) .<br/>                  |
| <span id="XAUDIO2_COMMIT_ALL"></span><span id="xaudio2_commit_all"></span><dl> <dt>**XAUDIO2 \_ valider \_ tout**</dt> </dl>                         | Utilisé en tant que paramètre dans [**IXAudio2 :: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges).<br/>                                                                   |
| <span id="XAUDIO2_INVALID_OPSET"></span><span id="xaudio2_invalid_opset"></span><dl> <dt>**XAUDIO2 \_ non valide \_ OPSET**</dt> </dl>                | Spécifie une valeur non valide pour les arguments OperationSet. Pour plus d’informations, consultez [jeux d’opérations XAudio2](xaudio2-operation-sets.md) .<br/>                         |
| <span id="XAUDIO2_NO_LOOP_REGION"></span><span id="xaudio2_no_loop_region"></span><dl> <dt>**XAUDIO2 \_ aucune \_ région de boucle \_**</dt> </dl>            | Spécifie aucune région de boucle, utilisée dans la [**\_ mémoire tampon XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**LoopCount**.<br/>                                                                    |
| <span id="XAUDIO2_LOOP_INFINITE"></span><span id="xaudio2_loop_infinite"></span><dl> <dt>**\_Boucle XAUDIO2 \_ infinie**</dt> </dl>                | Spécifie une boucle infinie, utilisée dans la [**\_ mémoire tampon XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**LoopCount**.<br/>                                                                  |
| <span id="XAUDIO2_DEFAULT_CHANNELS"></span><span id="xaudio2_default_channels"></span><dl> <dt>**XAUDIO2 \_ les \_ canaux par défaut**</dt> </dl>       | Spécifie le nombre de canaux par défaut pour la plateforme actuelle, utilisé dans [**IXAudio2 :: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).<br/> |
| <span id="XAUDIO2_DEFAULT_SAMPLERATE"></span><span id="xaudio2_default_samplerate"></span><dl> <dt>**XAUDIO2 \_ par défaut \_ samplerate**</dt> </dl> | Spécifie le taux d’échantillonnage par défaut pour la plateforme actuelle, utilisé dans [**IXAudio2 :: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).<br/>        |



**Indicateurs XAudio2**



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_DEBUG_ENGINE"></span><span id="xaudio2_debug_engine"></span><dl> <dt><strong>XAUDIO2_DEBUG_ENGINE</strong></dt> </dl></td>
<td style="text-align: left;">Spécifie que la version Debug/Checked du moteur audio doit être utilisée à la place de la version Release. Consultez <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create</strong></a>.<br/>
<blockquote>
[!Note]<br />
Cet indicateur n’est pas pris en charge sur Windows 8 ou Windows 10.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_VOICE_NOPITCH"></span><span id="xaudio2_voice_nopitch"></span><dl> <dt><strong>XAUDIO2_VOICE_NOPITCH</strong></dt> </dl></td>
<td style="text-align: left;">Spécifie qu’une voix source n’utilise pas le décalage de la hauteur de page, consultez <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2 :: CreateSourceVoice</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_VOICE_NOSRC"></span><span id="xaudio2_voice_nosrc"></span><dl> <dt><strong>XAUDIO2_VOICE_NOSRC</strong></dt> </dl></td>
<td style="text-align: left;">Spécifie qu’aucune conversion de taux d’échantillonnage n’est disponible sur une voix source, les sorties de la voix doivent avoir le même taux d’échantillonnage. Consultez <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2 :: CreateSourceVoice</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_VOICE_USEFILTER"></span><span id="xaudio2_voice_usefilter"></span><dl> <dt><strong>XAUDIO2_VOICE_USEFILTER</strong></dt> </dl></td>
<td style="text-align: left;">Spécifie que l’effet de filtre doit être disponible sur une voix. Consultez <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2 :: CreateSourceVoice</strong></a> et <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice"><strong>IXAudio2 :: CreateSubmixVoice</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_PLAY_TAILS"></span><span id="xaudio2_play_tails"></span><dl> <dt><strong>XAUDIO2_PLAY_TAILS</strong></dt> </dl></td>
<td style="text-align: left;">Spécifie qu’une voix doit continuer à émettre une sortie d’effet une fois qu’elle a été arrêtée. Consultez <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop"><strong>IXAudio2SourceVoice :: Stop</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_END_OF_STREAM"></span><span id="xaudio2_end_of_stream"></span><dl> <dt><strong>XAUDIO2_END_OF_STREAM</strong></dt> </dl></td>
<td style="text-align: left;">Indique la dernière mémoire tampon dans un flux. Consultez <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer"><strong>XAUDIO2_BUFFER</strong></a>. <strong>Indicateurs</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_STOP_ENGINE_WHEN_IDLE"></span><span id="xaudio2_stop_engine_when_idle"></span><dl> <dt><strong>XAUDIO2_STOP_ENGINE_WHEN_IDLE</strong></dt> </dl></td>
<td style="text-align: left;">Spécifie que le moteur audio doit s’arrêter quand aucune voix source n’est démarrée et ne démarre pas au démarrage d’une voix. Consultez <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_SEND_USEFILTER"></span><span id="xaudio2_send_usefilter"></span><dl> <dt><strong>XAUDIO2_SEND_USEFILTER</strong></dt> </dl></td>
<td style="text-align: left;">Indique qu’un filtre doit être utilisé sur un envoi vocal. Consultez <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_send_descriptor"><strong>XAUDIO2_SEND_DESCRIPTOR</strong></a>. <strong>Indicateurs</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_1024_QUANTUM"></span><span id="xaudio2_1024_quantum"></span><dl> <dt><strong>XAUDIO2_1024_QUANTUM</strong></dt> </dl></td>
<td style="text-align: left;">Spécifie un quantum de traitement non défini par défaut de 21,33 ms (1024 exemples à 48 kHz). Consultez <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_NO_VIRTUAL_AUDIO_CLIENT"></span><span id="xaudio2_no_virtual_audio_client"></span><dl> <dt><strong>XAUDIO2_NO_VIRTUAL_AUDIO_CLIENT</strong></dt> </dl></td>
<td style="text-align: left;">Spécifie qu’un client audio virtuel ne doit pas être utilisé. Consultez <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice"><strong>IXAudio2 :: CreateMasteringVoice</strong></a>.<br/>
<blockquote>
[!Note]<br />
Sur les appareils de la famille d’appareils mobiles, un client audio virtuel est toujours utilisé, que cet indicateur soit utilisé ou non.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



**Paramètres par défaut de XAudio2 pour le filtre vocal intégré**



| Constante                                                                                                                                                                                                                 | Description                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_DEFAULT_FILTER_TYPE"></span><span id="xaudio2_default_filter_type"></span><dl> <dt>**\_Type de \_ filtre par défaut XAUDIO2 \_**</dt> </dl>                | Spécifie le type de filtre par défaut à utiliser avec les voix et les émissions vocales.<br/>          |
| <span id="XAUDIO2_DEFAULT_FILTER_FREQUENCY"></span><span id="xaudio2_default_filter_frequency"></span><dl> <dt>**\_Fréquence du \_ filtre par défaut XAUDIO2 \_**</dt> </dl> | Spécifie la fréquence de filtre par défaut à utiliser avec les voix et les émissions vocales.<br/>     |
| <span id="XAUDIO2_DEFAULT_FILTER_ONEOVERQ"></span><span id="xaudio2_default_filter_oneoverq"></span><dl> <dt>**XAUDIO2 \_ filtre par défaut \_ \_ ONEOVERQ**</dt> </dl>    | Spécifie la fréquence de filtrage par défaut à utiliser avec les voix et les émissions vocales.<br/> |



## <a name="remarks"></a>Notes

### <a name="platform-requirements"></a>Conditions requises par la plateforme

Windows 10 (XAudio 2.9); Windows 8, Windows Phone 8 (XAudio 2,8); SDK DirectX (XAudio 2,7)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|--------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Xaudio2. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[XAudio2 :: constants](constants.md)
</dt> </dl>

 

 

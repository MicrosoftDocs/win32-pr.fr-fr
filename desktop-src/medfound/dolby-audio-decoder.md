---
description: Le décodeur Dolby audio est une table MFT qui décode Dolby Digital (AC-3) et Dolby Digital plus.
ms.assetid: A968914A-E4C5-4472-8776-C73F5910089A
title: Décodeur audio Dolby
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ae38516edd935def5d9b2b041c942a729c45c61
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479865"
---
# <a name="dolby-audio-decoder"></a>Décodeur audio Dolby

Le décodeur Dolby audio est une [Media Foundation transformation](media-foundation-transforms.md) (MFT) qui décode les types de flux suivants :

-   Dolby Digital, également appelé Dolby AC-3
-   Dolby Digital plus, également appelé AC-3 amélioré (E-AC-3)

> [!IMPORTANT]
> pour les versions de Windows antérieures à Windows 8, l’implémentation microsoft de la technologie dolby digital est limitée aux termes du programme de gestion de licences dolby digital à utiliser par les applications microsoft.

 

Pour plus d’informations sur ces formats, reportez-vous à la version B du document de la *norme de compression audio numérique (ATSC-3, E-AC-3)*.

Le décodeur peut également convertir un flux Dolby Digital plus en format Dolby Digital pour la sortie AC-3 S/PIDF, ou formater un flux Dolby Digital plus pour la sortie numérique HDMI.

## <a name="class-identifier"></a>Identificateur de classe

L’identificateur de classe (CLSID) du décodeur Dolby audio est **CLSID \_ CMSDDPlusDecMFT**, défini dans le fichier d’en-tête wmcodecdsp. h.

## <a name="input-types"></a>Types d’entrée

Le décodeur audio Dolby prend en charge les sous-types d’entrée suivants.



| Subtype                                 | Description                                                                                                                                                 | En-tête       |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| **MEDIASUBTYPE \_ Dolby \_ AC3**            | Audio Dolby Digital.                                                                                                                                        | mfapi. h      |
| **MEDIASUBTYPE \_ DVM**                   | Audio Dolby Digital ; consultez [**sous-types audio**](../directshow/audio-subtypes.md). Ce sous-type peut être utilisé de façon interchangeable avec **MEDIASUBTYPE \_ Dolby \_ AC3**.<br/> | wmcodecdsp. h |
| **MFAudioFormat \_ Dolby \_ Digital \_ plus** | Audio Dolby Digital plus.                                                                                                                                   | mfapi. h      |



 

Le tableau suivant répertorie les attributs requis et facultatifs pour le type de média d’entrée.




| Attribut | Description | Notes | 
|-----------|-------------|---------|
| <a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a> | Type principal. | Obligatoire. Doit être <strong>MFMediaType_Audio</strong>. | 
| <a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a> | Sous-type audio. | Obligatoire. Pour plus d’informations, consultez le tableau précédent. | 
| <a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a> | Taux d’échantillonnage, en échantillons par seconde. | facultatif. Les valeurs valides sont les suivantes : 48000, 44100, 32000, 24000, 22050 et 16000. Si cet attribut n’est pas défini, la valeur par défaut est 48000. <br /><blockquote>[!Note]<br />Les flux Dolby AC-3 sont limités aux trois tarifs les plus élevés de cette liste.</blockquote><br /> | 
| <a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a> | Nombre de canaux, y compris le canal à fréquence faible (LFE), le cas échéant. | facultatif. Les valeurs valides sont comprises entre 1 (mono) et 8 (configuration de canal 7,1). Si cet attribut n’est pas défini, la valeur par défaut est 2 (stéréo). | 
| <a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a> | Spécifie l’affectation des canaux audio aux positions des haut-parleurs. | facultatif. S’il est spécifié, la valeur doit être cohérente avec le nombre de canaux audio. Si l’attribut n’est pas défini, le décodeur utilise un masque de canal par défaut, en fonction du nombre de canaux. | 




 

Le tableau suivant répertorie les configurations Dolby Channel prises en charge.




| Configuration du canal | Nombre de canaux | Masques de canal | 
|-----------------------|--------------------|---------------|
| 1/0 (mono) | 1 | 0x4 (<strong>SPEAKER_FRONT_CENTER</strong>) | 
| 2/0 (stéréo) ou 1 + 1 (double mono) | 2 | 0x3 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong>) | 
| 3/0 | 3 | 0x7 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | SPEAKER_FRONT_CENTER) | 
| 2/1 | 3 | 0x103 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_BACK_CENTER</strong>) | 
| 3/1 | 4 | 0x107 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_BACK_CENTER</strong>) | 
| 2/2 | 4 | 0x33 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong>)<br /> ou<br /> 0x603 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_SIDE_LEFT</strong> | <strong>SPEAKER_SIDE_RIGHT</strong>) <br /> | 
| 3/2 | 5 | 0x37 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong>)<br /> ou<br /> 0x607 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_SIDE_LEFT</strong> | <strong>SPEAKER_SIDE_RIGHT</strong>) <br /> | 
| 3/2 + LFE | 6 | 0x3F (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_LOW_FREQUENCY</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong>)<br /> ou<br /> 0x60F (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_LOW_FREQUENCY</strong> | <strong>SPEAKER_SIDE_LEFT</strong> | <strong>SPEAKER_SIDE_RIGHT</strong>)<br /> | 
| 3/2/2 + LFE<blockquote>[!Note]<br />Dolby Digital plus uniquement.</blockquote><br /><br /> | 8 | 0x63F (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_LOW_FREQUENCY</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong> | SPEAKER_SIDE_LEFT | SPEAKER_SIDE_RIGHT) | 




 

En outre, les configurations de canal 1/0, 2/0, 3/0, 2/1, 3/1 et 2/2 peuvent également apparaître avec un canal LFE.

## <a name="output-types"></a>Types de sortie

Le décodeur audio Dolby prend en charge les sous-types de sortie suivants.



| Subtype                                                   | Description                                                                                                                               | En-tête    |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| **MFAudioFormat \_ Dolby \_ AC3 \_ SPDIF**                      | Audio Dolby AC-3 formaté pour la sortie numérique S/PDIF.                                                                                     | mfapi. h   |
| **KSDATAFORMAT \_ sous-type \_ IEC61937 \_ Dolby \_ Digital \_ plus** | Audio Dolby Digital plus formaté pour la sortie numérique HDMI.                                                                               | ksmedia. h |
| **MFAudioFormat \_ float**                                  | Audio PCM à virgule flottante IEEE 32 bits<br/> **Windows 10**: stéréo, 5,1, 7,1<br/> **Versions précédentes**: stéréo, 5,1<br/> | mfapi. h   |
| **\_PCM MFAudioFormat**                                    | audio PCM 16 bits<br/> **Windows 10**: stéréo, 5,1, 7,1<br/> **Versions précédentes**: stéréo, 5,1<br/>                     | mfapi. h   |



 

Le tableau suivant répertorie les attributs obligatoires et facultatifs pour le type de média de sortie.




| Attribut | Description | Notes | 
|-----------|-------------|---------|
| <a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a> | Type principal. | Obligatoire. Doit être <strong>MFMediaType_Audio</strong>. | 
| <a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a> | Sous-type audio. | Obligatoire. Pour plus d’informations, consultez le tableau précédent. | 
| <a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a> | Taux d’échantillonnage, en échantillons par seconde. | Obligatoire. Les valeurs valides sont les suivantes : 48000, 44100, 32000, 24000, 22050 et 16000. Le taux d’échantillonnage de sortie doit être identique au taux d’échantillonnage d’entrée. Le décodeur ne peut pas modifier la fréquence d’échantillonnage du flux. | 
| <a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a> | Nombre de canaux, y compris le canal à fréquence faible (LFE), le cas échéant. | Requis pour la sortie PCM. <br /> Non nécessaire pour la sortie numérique. <br /> Si le type d’entrée est mono, stéréo ou double-mono (tout sans canal LFE), la seule valeur valide est 2, pour la sortie stéréo. Dans le cas contraire, la valeur peut être : <br /><ul><li>2 pour downmix stéréo</li><li>6 pour les configurations de canal 5,1</li><li>8 pour les configurations de canal 7,1</li></ul> | 
| <a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a> | Spécifie l’affectation des canaux audio aux positions des haut-parleurs. | Requis pour la sortie PCM si le nombre de canaux est supérieur à 2. La valeur doit être :<br /><ul><li>0x3 pour sortie stéréo</li><li>0x3F pour sortie de canal 5,1</li><li>0x63F pour la sortie du canal 7,1</li></ul>Non nécessaire pour la sortie numérique. <br /> | 
| <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a> | Nombre de bits par échantillon audio. | Requis pour la sortie PCM. La valeur doit être 32 pour <strong>MFAudioFormat_Float</strong>, et 16 pour <strong>MFAudioFormat_PCM</strong>.<br /> Non nécessaire pour la sortie numérique.<br /> | 
| <a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a> | Nombre de bits de données audio valides dans chaque exemple audio. | Facultatif pour la sortie PCM. Si cette valeur est définie, la valeur doit être identique à <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.<br /> Non nécessaire pour les sous-types de sortie numérique.<br /> | 
| <a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a> | Alignement de bloc, en octets. | Facultatif pour la sortie PCM. Non nécessaire pour la sortie numérique. | 
| <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> | Nombre moyen d’octets par seconde. | Facultatif pour la sortie PCM. Non nécessaire pour la sortie numérique. | 




 

## <a name="transform-attributes"></a>Attributs de transformation

Le décodeur audio Dolby implémente la méthode [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . L’application peut utiliser cette méthode pour récupérer ou définir les attributs suivants.



| Attribut                                                                                | Description                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVDecAudioDualMono](../directshow/avdecaudiodualmono-property.md)                        | Spécifie si un flux audio Dolby à 2 canaux est encodé en stéréo ou en double mono. Avant que la première trame Dolby soit décodée, la valeur est **EAVDecAudioDualMono \_ non spécifié**. Une fois le décodage commencé, la valeur reflète le frame Dolby le plus récent.<br/> Lecture seule. <br/> |
| [CODECAPI \_ AVDecAudioDualMonoReproMode](../directshow/avdecaudiodualmonorepromode-property.md)      | Spécifie la manière dont le décodeur reproduit le son double mono. La valeur par défaut **est \_ eAVDecAudioDualMonoReproMode \_ mono gauche**. L’application peut définir cette propriété à tout moment.<br/> En lecture/écriture.<br/>                                                                            |
| [CODECAPI \_ AVDecCommonMeanBitRate](../directshow/avdeccommonmeanbitrate.md)                         | Pour les flux Dolby Digital (AC-3), spécifie la vitesse de transmission du flux d’entrée en bits par seconde. Pour Dolby Digital plus (E-AC3), la valeur est toujours égale à zéro.<br/> Lecture seule.<br/>                                                                                              |
| [CODECAPI \_ AVDecDDDynamicRangeScaleHigh](../directshow/avdecdddynamicrangescalehigh-property.md)    | La coupe de haut niveau lorsque le décodeur effectue un contrôle de plage dynamique.<br/> En lecture/écriture.<br/>                                                                                                                                                                                    |
| [CODECAPI \_ AVDecDDDynamicRangeScaleLow](../directshow/avdecdddynamicrangescalelow-property.md)      | Renforcement de bas niveau lorsque le décodeur effectue un contrôle de plage dynamique.<br/> En lecture/écriture.<br/>                                                                                                                                                                                   |
| [CODECAPI \_ AVDecDDOperationalMode](../directshow/avdecddoperationalmode-property.md)                | Mode de contrôle de compression.<br/> En lecture/écriture.<br/>                                                                                                                                                                                                                          |
| [CODECAPI \_ AVDecDDStereoDownMixMode](codecapi-avdecddstereodownmixmode.md)              | Type de downmix stéréo. Cette propriété s’applique lorsque l’entrée est un flux multicanaux et que la sortie est un flux stéréo.<br/> En lecture/écriture.<br/>                                                                                                                           |
| [\_modification du \_ format dynamique de la prise en charge de \_ MFT \_](mft-support-dynamic-format-change-attribute.md) | Cet attribut retourne la **valeur false**, ce qui indique que le décodeur doit être vidé avant qu’un nouveau type d’entrée soit défini.<br/> En lecture/écriture.<br/>                                                                                                                                          |



 

## <a name="remarks"></a>Remarques

Le décodeur accepte uniquement les flux Dolby bruts, comme défini par un/52B. les charges utiles telles que les Flux élémentaires par paquets (PES) ne sont pas prises en charge. Pour Dolby Digital plus, le décodeur décode jusqu’à 5,1 canaux. sur Windows 10, les flux de canal 7,1 sont décodés sans downmix. Sur les versions précédentes du système d’exploitation, si le flux est 7,1 canaux, seul le canal 5,1 downmix sera décodé. Si le flux est Dolby Digital plus avec plus d’un sous-flux indépendant, seul le sous-flux indépendant 0 est décodé. Le décodeur ignore les autres sous-flux indépendants. En outre, le décodeur ignore tous les sous-flux dépendants. Le décodeur prend en charge le déchiffrement et le décodage des flux protégés par la technologie de Rights Management numérique (DRM).

Si le type de média d’entrée a une configuration de canal autre que mono, stéréo ou double-mono (tout cela sans canal LFE), le décodeur fournit deux options pour les configurations de canal de sortie :

-   sortie à 8 canaux (configuration de canal 7,1)
-   sortie à 6 canaux (configuration de canal 5,1)
-   Downmix stéréo

Si l’option stéréo downmix est sélectionnée, le type de downmix peut être défini sur la table MFT à l’aide de la propriété [CODECAPI \_ AVDecDDStereoDownMixMode](codecapi-avdecddstereodownmixmode.md) .

Si le type de sortie est **MFAudioFormat \_ Dolby \_ AC3 \_ SPDIF**, chaque mémoire tampon de sortie contient 6 144 octets. La mémoire tampon commence par un en-tête S/PDIF de 8 octets, suivi d’une trame AC-3 compressée, suivie d’un remplissage de zéro à 6 144 octets.

Si le type de sortie est **KSDATAFORMAT \_ SubType \_ IEC61937 \_ Dolby \_ Digital \_ plus**, chaque mémoire tampon de sortie contient 24 576 octets. La mémoire tampon commence par un en-tête S/PDIF de 8 octets, suivi de 1 à 6 frames Dolby Digital plus compressés correspondant aux exemples PCM 1 536, suivi de zéro remplissage à 24 576 octets. Pour la sortie HDMI, seul le sous-flux indépendant 0 est compressé.

La table MFT du décodeur est inscrite avec l’indicateur d' **énumération MFT d’indicateur \_ \_ \_ FIELDOFUSE**, qui indique que la table MFT doit être déverrouillée par l’application avant d’être utilisée. Pour plus d’informations, consultez [restrictions relatives au champ d’utilisation](field-of-use-restrictions.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                  |
| DLL<br/>                      | <dl> <dt>Msauddecmft.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets codec](codecobjects.md)
</dt> </dl>

 

 

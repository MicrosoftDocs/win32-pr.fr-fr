---
description: Cette rubrique explique comment spécifier le format d’un flux AAC (Advanced Audio encodage) dans Media Foundation.
ms.assetid: 82218bc5-6660-4253-b50c-b6d9f30be3d5
title: Types de média AAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae70661478ad0d2267c951c80fc4a63d98c15267
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479885"
---
# <a name="aac-media-types"></a>Types de média AAC

Cette rubrique explique comment spécifier le format d’un flux AAC (Advanced Audio encodage) dans Media Foundation.

Deux sous-types sont définis pour le son AAC :



| Subtype                     | Description          | En-tête       |
|-----------------------------|----------------------|--------------|
| **MFAudioFormat \_ AAC**      | AAC brut ou ADTS AAC. | mfapi. h      |
| **MEDIASUBTYPE \_ brut \_ AAC1** | AAC brut.             | wmcodecdsp. h |



 

<dl> <dt>

<span id="MFAudioFormat_AAC"></span><span id="mfaudioformat_aac"></span><span id="MFAUDIOFORMAT_AAC"></span>MFAudioFormat \_ AAC
</dt> <dd>

Pour ce sous-type, le type de média donne le taux d’échantillonnage et le nombre de canaux avant l’application des outils de réplication en bande spectrale (SBR) et de la stéréo paramétrique (PS), le cas échéant. L’effet de l’outil SBR est de doubler le taux d’échantillonnage décodé par rapport au taux d’échantillonnage AAC-LC de base. L’effet de l’outil PS est de décoder le stéréo à partir d’un flux en AAC-LC Core à canaux mono.

Ce sous-type est équivalent à **MEDIASUBTYPE \_ MPEG \_ HEAAC**, défini dans wmcodecdsp. h. Consultez [GUID de sous-type audio](audio-subtype-guids.md).

</dd> <dt>

<span id="MEDIASUBTYPE_RAW_AAC1"></span><span id="mediasubtype_raw_aac1"></span>MEDIASUBTYPE \_ brut \_ AAC1
</dt> <dd>

Ce sous-type est utilisé pour AAC contenu dans un fichier AVI avec la balise de format audio égale au \_ format Wave \_ RAW \_ AAC1 (0x00FF).

Pour ce sous-type, le type de média donne le taux d’échantillonnage et le nombre de canaux après l’application des outils SBR et PS, le cas échéant.

</dd> </dl>

Les attributs de type de média suivants s’appliquent à l’audio AAC.




| Attribut | Description | 
|-----------|-------------|
| <a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a> | Type principal. Doit être <strong>MFMediaType_Audio</strong>. | 
| <a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a> | Sous-type audio. Pour plus d’informations, reportez-vous à la description précédente. | 
| <a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a> | Profil et niveau audio. <br /> La valeur de cet attribut est le champ <strong>audioProfileLevelIndication</strong> , tel que défini par la norme ISO/IEC 14496-3.<br /> S’il est inconnu, défini à zéro ou à 0xFE (« aucun profil audio n’est spécifié »).<br /> | 
| <a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a> | Vitesse de transmission du flux AAC encodé, en octets par seconde. | 
| <a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> | Type de charge utile.<br /> S’applique uniquement aux <strong>MFAudioFormat_AAC</strong>.<br /><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> est facultatif. Si cet attribut n’est pas spécifié, la valeur par défaut 0 est utilisée, qui spécifie que le flux contient uniquement des éléments raw_data_block.<br /> | 
| <a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a> | Profondeur de bit du fichier audio PCM décodé. | 
| <a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a> | Attribution de canaux audio aux positions des orateurs. | 
| <a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a> | Nombre de canaux, y compris le canal à fréquence faible (LFE), le cas échéant.<br /> L’interprétation de cette valeur dépend du sous-type de média, comme décrit précédemment.<br /> | 
| <a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a> | Taux d’échantillonnage, en échantillons par seconde.<br /> L’interprétation de cette valeur dépend du sous-type de média, comme décrit précédemment.<br /> | 
| <a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a> | La valeur de cet attribut dépend du sous-type :<br /><ul><li><strong>MFAudioFormat_AAC</strong>: contient la partie de la structure <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> qui apparaît après la structure <strong>WAVEFORMATEX</strong> (autrement dit, après le membre <strong>wfx</strong> ). Cela est suivi des données AudioSpecificConfig (), telles que définies par la norme ISO/IEC 14496-3.</li><li><strong>MEDIASUBTYPE_RAW_AAC1</strong>: contient les données AudioSpecificConfig ().</li></ul> | 




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de média audio](audio-media-types.md)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> <dt>

[Prise en charge MPEG-4 dans Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 


---
description: GUID de sous-type audio
ms.assetid: c38a1194-e2d8-42ca-8581-4054171f6f44
title: GUID de sous-type audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26b61dc7c8bb828deb6278b037dd6128afcaf1f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296355"
---
# <a name="audio-subtype-guids"></a>GUID de sous-type audio

Les GUID de sous-type audio suivants sont définis. Pour spécifier le sous-type, définissez l’attribut de sous- [**\_ \_ type MF MT**](mf-mt-subtype-attribute.md) sur le type de média. Sauf indication contraire, ces constantes sont définies dans le fichier d’en-tête mfapi. h.

Quand ces sous-types sont utilisés, affectez à l’attribut de [ \_ \_ \_ type principal MF MT](mf-mt-major-type-attribute.md) la valeur **MFMediaType \_ audio**.




| GUID | Description | Balise de format (FOURCC) | 
|------|-------------|---------------------|
| <strong>MEDIASUBTYPE_RAW_AAC1</strong> | Codage audio avancé (AAC).<br /> Ce sous-type est utilisé pour l’AAC contenu dans un fichier AVI dont la balise de format audio est égale à 0x00FF. <br /> Pour plus d’informations, consultez <a href="aac-decoder.md"><strong>décodeur AAC</strong></a>.<br /> Défini dans wmcodecdsp. h<br /> | WAVE_FORMAT_RAW_AAC1 (0x00FF) | 
| <strong>MFAudioFormat_AAC</strong> | Codage audio avancé (AAC).<br /><blockquote>[!Note]<br />Équivalent à MEDIASUBTYPE_MPEG_HEAAC, défini dans wmcodecdsp. h.</blockquote><br /> Le flux peut contenir des données AAC brutes ou des données AAC dans un flux ADTS (audio Data Transport Stream).<br /> Pour plus d'informations, consultez les pages suivantes :<br /><ul><li><a href="aac-decoder.md"><strong>Décodeur AAC</strong></a></li><li><a href="mpeg-4-file-source.md">Source de fichier MPEG-4</a></li></ul> | WAVE_FORMAT_MPEG_HEAAC (0x1610) | 
| <strong>MFAudioFormat_ADTS</strong> | Non utilisé. | WAVE_FORMAT_MPEG_ADTS_AAC (0x1600) | 
| <strong>MFAudioFormat_ALAC</strong> | Codec audio Apple sans perte<br /> pris en charge dans Windows 10 et versions ultérieures.<br /> | WAVE_FORMAT_ALAC (0x6C61) | 
| <strong>MFAudioFormat_AMR_NB</strong> | Adaptative audio à plusieurs débits<br /> pris en charge dans Windows 8.1 et versions ultérieures.<br /> | WAVE_FORMAT_AMR_NB | 
| <strong>MFAudioFormat_AMR_WB</strong> | Adaptative audio à large bande à débit multiple<br /> pris en charge dans Windows 8.1 et versions ultérieures.<br /> | WAVE_FORMAT_AMR_WB | 
| <strong>MFAudioFormat_AMR_WP</strong> | pris en charge dans Windows 8.1 et versions ultérieures.<br /> | WAVE_FORMAT_AMR_WP | 
| <strong>MFAudioFormat_Dolby_AC3</strong> | Dolby Digital (AC-3).<br /> Même valeur GUID que <strong>MEDIASUBTYPE_DOLBY_AC3</strong>, qui est définie dans ksuuids. h<br /> | Aucun. | 
| <strong>MFAudioFormat_Dolby_AC3_SPDIF</strong> | Audio Dolby AC-3 sur Sony/Philips Digital Interface (S/PDIF).<br /> Cette valeur GUID est identique aux sous-types suivants :<br /><ul><li><strong>KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL</strong>, défini dans ksmedia. h.</li><li><strong>MEDIASUBTYPE_DOLBY_AC3_SPDIF</strong>, défini dans UUID. h.</li></ul> | WAVE_FORMAT_DOLBY_AC3_SPDIF (0x0092) | 
| <strong>MFAudioFormat_Dolby_DDPlus</strong> | Dolby Digital plus.<br /> Même valeur GUID que <strong>MEDIASUBTYPE_DOLBY_DDPLUS</strong>, qui est définie dans wmcodecdsp. h.<br /> | None | 
| <strong>MFAudioFormat_DRM</strong> | Données audio chiffrées utilisées avec un chemin d’accès audio sécurisé. | WAVE_FORMAT_DRM (0x0009) | 
| <strong>MFAudioFormat_DTS</strong> | Audio Digital Theater Systems (DTS). | WAVE_FORMAT_DTS (0x0008) | 
| <strong>MFAudioFormat_FLAC</strong> | Codec audio sans perte gratuit<br /> pris en charge dans Windows 10 et versions ultérieures.<br /> | WAVE_FORMAT_FLAC (0xF1AC) | 
| <strong>MFAudioFormat_Float</strong> | Audio à virgule flottante IEEE non compressé. | WAVE_FORMAT_IEEE_FLOAT (0x0003) | 
| <strong>MFAudioFormat_Float_SpatialObjects</strong> | Audio à virgule flottante IEEE non compressé. | None | 
| <strong>MFAudioFormat_MP3</strong> | MPEG Audio Layer-3 (MP3). | WAVE_FORMAT_MPEGLAYER3 (0x0055) | 
| <strong>MFAudioFormat_MPEG</strong> | Charge utile MPEG-1. | WAVE_FORMAT_MPEG (0x0050) | 
| <strong>MFAudioFormat_MSP1</strong> | Windows Codec audio Media Audio 9. | WAVE_FORMAT_WMAVOICE9 (0x000A) | 
| <strong>MFAudioFormat_Opus</strong> | Opus<br /> pris en charge dans Windows 10 et versions ultérieures.<br /> | WAVE_FORMAT_OPUS (0x704F) | 
| <strong>MFAudioFormat_PCM</strong> | Audio PCM non compressé. | WAVE_FORMAT_PCM (1) | 
| <strong>MFAudioFormat_QCELP</strong> | QCELP (code Qualcomm avec prédiction linéaire incorrecte). | None | 
| <strong>MFAudioFormat_WMASPDIF</strong> | Windows codec Media Audio 9 Professional sur S/PDIF. | WAVE_FORMAT_WMASPDIF (0x0164) | 
| <strong>MFAudioFormat_WMAudio_Lossless</strong> | Windows codec Media Audio 9 Lossless ou Windows Media Audio codec 9,1. | WAVE_FORMAT_WMAUDIO_LOSSLESS (0x0163) | 
| <strong>MFAudioFormat_WMAudioV8</strong> | Windows codec Media Audio 8, codec Windows Media Audio 9 ou Windows Media Audio codec 9,1. | WAVE_FORMAT_WMAUDIO2 (0x0161) | 
| <strong>MFAudioFormat_WMAudioV9</strong> | Windows codec Media Audio 9 Professional ou Windows Media Audio codec Professional 9,1. | WAVE_FORMAT_WMAUDIO3 (0x0162) | 




 

Les balises de format répertoriées dans la troisième colonne de cette table sont utilisées dans la structure **WAVEFORMATEX** , et sont définies dans le fichier d’en-tête mmreg. h.

Pour une balise de format audio donnée, vous pouvez créer un GUID de sous-type audio comme suit :

1.  Commencez par la valeur **MFAudioFormat \_ base**, qui est définie dans mfaph. i.
2.  Remplacez le premier **DWORD** de ce GUID par la balise format.

Vous pouvez utiliser la macro [**définir le \_ \_ GUID du MediaType**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid) pour définir une nouvelle constante GUID qui suit ce modèle.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de média audio](audio-media-types.md)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[GUID de type de média](media-type-guids.md)
</dt> <dt>

[Types de médias](media-types.md)
</dt> </dl>

 

 





---
description: GUID de sous-type audio
ms.assetid: c38a1194-e2d8-42ca-8581-4054171f6f44
title: GUID de sous-type audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04192f19f530c288b9aef7b5718b8329ea108bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484129"
---
# <a name="audio-subtype-guids"></a>GUID de sous-type audio

Les GUID de sous-type audio suivants sont définis. Pour spécifier le sous-type, définissez l’attribut de sous- [**\_ \_ type MF MT**](mf-mt-subtype-attribute.md) sur le type de média. Sauf indication contraire, ces constantes sont définies dans le fichier d’en-tête mfapi. h.

Quand ces sous-types sont utilisés, affectez à l’attribut de [ \_ \_ \_ type principal MF MT](mf-mt-major-type-attribute.md) la valeur **MFMediaType \_ audio**.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>GUID</th>
<th>Description</th>
<th>Balise de format (FOURCC)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>MEDIASUBTYPE_RAW_AAC1</strong></td>
<td>Codage audio avancé (AAC).<br/> Ce sous-type est utilisé pour l’AAC contenu dans un fichier AVI dont la balise de format audio est égale à 0x00FF. <br/> Pour plus d’informations, consultez <a href="aac-decoder.md"><strong>décodeur AAC</strong></a>.<br/> Défini dans wmcodecdsp. h<br/></td>
<td>WAVE_FORMAT_RAW_AAC1 (0x00FF)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_AAC</strong></td>
<td>Codage audio avancé (AAC).<br/>
<blockquote>
[!Note]<br />
Équivalent à MEDIASUBTYPE_MPEG_HEAAC, défini dans wmcodecdsp. h.
</blockquote>
<br/> Le flux peut contenir des données AAC brutes ou des données AAC dans un flux ADTS (audio Data Transport Stream).<br/> Pour plus d’informations, consultez :<br/>
<ul>
<li><a href="aac-decoder.md"><strong>Décodeur AAC</strong></a></li>
<li><a href="mpeg-4-file-source.md">Source de fichier MPEG-4</a></li>
</ul></td>
<td>WAVE_FORMAT_MPEG_HEAAC (0x1610)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_ADTS</strong></td>
<td>Non utilisé.</td>
<td>WAVE_FORMAT_MPEG_ADTS_AAC (0x1600)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_ALAC</strong></td>
<td>Codec audio Apple sans perte<br/> Pris en charge dans Windows 10 et versions ultérieures.<br/></td>
<td>WAVE_FORMAT_ALAC (0x6C61)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_AMR_NB</strong></td>
<td>Adaptative audio à plusieurs débits<br/> Pris en charge dans Windows 8.1 et versions ultérieures.<br/></td>
<td>WAVE_FORMAT_AMR_NB</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_AMR_WB</strong></td>
<td>Adaptative audio à large bande à débit multiple<br/> Pris en charge dans Windows 8.1 et versions ultérieures.<br/></td>
<td>WAVE_FORMAT_AMR_WB</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_AMR_WP</strong></td>
<td>Pris en charge dans Windows 8.1 et versions ultérieures.<br/></td>
<td>WAVE_FORMAT_AMR_WP</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_Dolby_AC3</strong></td>
<td>Dolby Digital (AC-3).<br/> Même valeur GUID que <strong>MEDIASUBTYPE_DOLBY_AC3</strong>, qui est définie dans ksuuids. h<br/></td>
<td>Aucun</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_Dolby_AC3_SPDIF</strong></td>
<td>Audio Dolby AC-3 sur Sony/Philips Digital Interface (S/PDIF).<br/> Cette valeur GUID est identique aux sous-types suivants :<br/>
<ul>
<li><strong>KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL</strong>, défini dans ksmedia. h.</li>
<li><strong>MEDIASUBTYPE_DOLBY_AC3_SPDIF</strong>, défini dans UUID. h.</li>
</ul></td>
<td>WAVE_FORMAT_DOLBY_AC3_SPDIF (0x0092)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_Dolby_DDPlus</strong></td>
<td>Dolby Digital plus.<br/> Même valeur GUID que <strong>MEDIASUBTYPE_DOLBY_DDPLUS</strong>, qui est définie dans wmcodecdsp. h.<br/></td>
<td>Aucun</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_DRM</strong></td>
<td>Données audio chiffrées utilisées avec un chemin d’accès audio sécurisé.</td>
<td>WAVE_FORMAT_DRM (0x0009)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_DTS</strong></td>
<td>Audio Digital Theater Systems (DTS).</td>
<td>WAVE_FORMAT_DTS (0x0008)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_FLAC</strong></td>
<td>Codec audio sans perte gratuit<br/> Pris en charge dans Windows 10 et versions ultérieures.<br/></td>
<td>WAVE_FORMAT_FLAC (0xF1AC)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_Float</strong></td>
<td>Audio à virgule flottante IEEE non compressé.</td>
<td>WAVE_FORMAT_IEEE_FLOAT (0x0003)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_Float_SpatialObjects</strong></td>
<td>Audio à virgule flottante IEEE non compressé.</td>
<td>Aucun</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_MP3</strong></td>
<td>MPEG Audio Layer-3 (MP3).</td>
<td>WAVE_FORMAT_MPEGLAYER3 (0x0055)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_MPEG</strong></td>
<td>Charge utile MPEG-1.</td>
<td>WAVE_FORMAT_MPEG (0x0050)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_MSP1</strong></td>
<td>Codec vocal Windows Media Audio 9.</td>
<td>WAVE_FORMAT_WMAVOICE9 (0x000A)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_Opus</strong></td>
<td>Opus<br/> Pris en charge dans Windows 10 et versions ultérieures.<br/></td>
<td>WAVE_FORMAT_OPUS (0x704F)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_PCM</strong></td>
<td>Audio PCM non compressé.</td>
<td>WAVE_FORMAT_PCM (1)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_QCELP</strong></td>
<td>QCELP (code Qualcomm avec prédiction linéaire incorrecte).</td>
<td>Aucun</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_WMASPDIF</strong></td>
<td>Codec Windows Media Audio 9 Professional sur S/PDIF.</td>
<td>WAVE_FORMAT_WMASPDIF (0x0164)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_WMAudio_Lossless</strong></td>
<td>Codec Windows Media Audio 9 Lossless ou Windows Media Audio Codec 9,1.</td>
<td>WAVE_FORMAT_WMAUDIO_LOSSLESS (0x0163)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_WMAudioV8</strong></td>
<td>Codec Windows Media Audio 8, Windows Media Audio 9 codec ou Windows Media Audio Codec 9,1.</td>
<td>WAVE_FORMAT_WMAUDIO2 (0x0161)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_WMAudioV9</strong></td>
<td>Codec Windows Media Audio 9 Professional ou Windows Media Audio Codec professionnel 9,1.</td>
<td>WAVE_FORMAT_WMAUDIO3 (0x0162)</td>
</tr>
</tbody>
</table>



 

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

 

 





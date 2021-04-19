---
description: Le tableau suivant décrit les principaux types de médias.
ms.assetid: 718a07f6-e2e4-4670-b9cf-982b53abffd2
title: Types principaux (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e5722cbad713f2fb9ae876e58941bde44c2e110
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541087"
---
# <a name="major-types"></a>Types principaux

Le tableau suivant décrit les principaux types de médias.



| GUID                                                                                                                                                                                                                                  | Description                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| <span id="MEDIATYPE_AnalogAudio"></span><span id="mediatype_analogaudio"></span><span id="MEDIATYPE_ANALOGAUDIO"></span><dl> <dt>**AnalogAudio de MEDIATYPE \_**</dt> </dl>         | Audio analogique.<br/>                                                                                  |
| <span id="MEDIATYPE_AnalogVideo"></span><span id="mediatype_analogvideo"></span><span id="MEDIATYPE_ANALOGVIDEO"></span><dl> <dt>**AnalogVideo de MEDIATYPE \_**</dt> </dl>         | Vidéo analogique.<br/>                                                                                  |
| <span id="MEDIATYPE_Audio"></span><span id="mediatype_audio"></span><span id="MEDIATYPE_AUDIO"></span><dl> <dt>**Audio de MEDIATYPE \_**</dt> </dl>                                 | HD. Consultez [sous-types audio](audio-subtypes.md).<br/>                                               |
| <span id="MEDIATYPE_AUXLine21Data"></span><span id="mediatype_auxline21data"></span><span id="MEDIATYPE_AUXLINE21DATA"></span><dl> <dt>**AUXLine21Data de MEDIATYPE \_**</dt> </dl> | Données de ligne 21. Utilisé par les sous-titres. Consultez la [**ligne 21 types de médias**](line-21-media-types.md).<br/> |
| <span id="MEDIATYPE_File"></span><span id="mediatype_file"></span><span id="MEDIATYPE_FILE"></span><dl> <dt>**\_Fichier MediaType**</dt> </dl>                                     | Fichier. (Obsolète)<br/>                                                                               |
| <span id="MEDIATYPE_Interleaved"></span><span id="mediatype_interleaved"></span><span id="MEDIATYPE_INTERLEAVED"></span><dl> <dt>**MEDIATYPE \_ entrelacé**</dt> </dl>         | Audio et vidéo entrelacés. Utilisé pour la vidéo numérique (DV).<br/>                                      |
| <span id="MEDIATYPE_LMRT"></span><span id="mediatype_lmrt"></span><dl> <dt>**LMRT de MEDIATYPE \_**</dt> </dl>                                                                      | Obsolète. Ne pas utiliser.<br/>                                                                          |
| <span id="MEDIATYPE_Midi"></span><span id="mediatype_midi"></span><span id="MEDIATYPE_MIDI"></span><dl> <dt>**Midi de MEDIATYPE \_**</dt> </dl>                                     | Format MIDI.<br/>                                                                                   |
| <span id="MEDIATYPE_MPEG2_PES"></span><span id="mediatype_mpeg2_pes"></span><dl> <dt>**\_PES MPEG2 de MediaType \_**</dt> </dl>                                                      | Paquets PES MPEG-2. Consultez [types de média MPEG-2](mpeg-2-media-types.md).<br/>                          |
| <span id="MEDIATYPE_MPEG2_SECTIONS"></span><span id="mediatype_mpeg2_sections"></span><dl> <dt>**SECTIONS de MEDIATYPE \_ MPEG2 \_**</dt> </dl>                                       | Données de section MPEG-2. Consultez [types de média MPEG-2](mpeg-2-media-types.md).<br/>                         |
| <span id="MEDIATYPE_ScriptCommand"></span><span id="mediatype_scriptcommand"></span><span id="MEDIATYPE_SCRIPTCOMMAND"></span><dl> <dt>**Commande de MEDIATYPE \_**</dt> </dl> | Les données sont une commande de script, utilisée par les sous-titres.<br/>                                             |
| <span id="MEDIATYPE_Stream"></span><span id="mediatype_stream"></span><span id="MEDIATYPE_STREAM"></span><dl> <dt>**Flux de MEDIATYPE \_**</dt> </dl>                             | Flux d’octets sans horodatage. Consultez les [**sous-types de flux**](stream-subtypes.md).<br/>               |
| <span id="MEDIATYPE_Text"></span><span id="mediatype_text"></span><span id="MEDIATYPE_TEXT"></span><dl> <dt>**Texte du MEDIATYPE \_**</dt> </dl>                                     | Texte.<br/>                                                                                          |
| <span id="MEDIATYPE_Timecode"></span><span id="mediatype_timecode"></span><span id="MEDIATYPE_TIMECODE"></span><dl> <dt>**\_Code temporel du MediaType**</dt> </dl>                     | Données du code temporel. Remarque : DirectShow ne fournit aucun filtre qui prend en charge ce type de média.<br/>     |
| <span id="MEDIATYPE_URL_STREAM"></span><span id="mediatype_url_stream"></span><dl> <dt>**\_flux d’URL de MediaType \_**</dt> </dl>                                                   | Obsolète. Ne pas utiliser.<br/>                                                                          |
| <span id="MEDIATYPE_VBI"></span><span id="mediatype_vbi"></span><dl> <dt>**VBI de MEDIATYPE \_**</dt> </dl>                                                                         | Données de l’intervalle de blancs vertical (VBI) (pour la télévision). Identique au \_ type KSDATAFORMAT \_ VBI.<br/>       |
| <span id="MEDIATYPE_Video"></span><span id="mediatype_video"></span><span id="MEDIATYPE_VIDEO"></span><dl> <dt>**Vidéo de MEDIATYPE \_**</dt> </dl>                                 | Vidéo. Consultez [sous-types de vidéos](video-subtypes.md).<br/>                                               |



## <a name="remarks"></a>Notes

Le GUID du sous-type définit plus en détail le format. Pour certains formats, le GUID de sous-type peut être MEDIASUBTYPE \_ None, ce qui signifie que le format ne requiert pas de sous-type.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types de médias](media-types.md)
</dt> </dl>

 

 





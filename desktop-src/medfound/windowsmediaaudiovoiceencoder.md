---
description: L’encodeur vocal Windows Media Audio est optimisé pour l’encodage de la voix humaine à des taux de compression élevés. Il s’agit de l’encodeur par défaut pour les flux composés principalement de mots prononcés.
ms.assetid: b3cfa845-4fe1-405f-88e5-4555398639ef
title: Encodeur vocal Windows Media Audio (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bef79f2c3d0c48fee8ec33e08bfb9fdf21c3656b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533440"
---
# <a name="windows-media-audio-voice-encoder"></a>Encodeur vocal Windows Media Audio

L’encodeur vocal Windows Media Audio est optimisé pour l’encodage de la voix humaine à des taux de compression élevés. Il s’agit de l’encodeur par défaut pour les flux composés principalement de mots prononcés.

## <a name="class-identifier"></a>Identificateur de classe

L’identificateur de classe (CLSID) de l’encodeur vocal Windows Media Audio est représenté par la constante **CLSID \_ CWMSPEncMediaObject2**. Vous pouvez créer une instance de l’encodeur vocal en appelant **CoCreateInstance**.

## <a name="output-formats"></a>Formats de sortie

Windows Media Audio contenu encodé en voix est identifié par la balise de format 0x00A.

## <a name="encoder-properties"></a>Propriétés de l’encodeur

L’encodeur vocal Windows Media Audio prend en charge les propriétés suivantes.



<table>
<thead>
<tr class="header">
<th>Propriété</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-wmavoice-enc-bufferwindowproperty.md">MFPKEY_WMAVOICE_ENC_BufferWindow</a></td>
<td>Spécifie la fenêtre de mémoire tampon, en millisecondes, utilisée pour le codec vocal.<br/> <dl> Windows XP et versions ultérieures.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmavoice-enc-decoderdelayproperty.md">MFPKEY_WMAVOICE_ENC_DecoderDelay</a></td>
<td>Spécifie la latence de l’encodeur dans les unités de paquets.<br/> <dl> Windows XP et versions ultérieures.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmavoice-enc-edlproperty.md">MFPKEY_WMAVOICE_ENC_EDL</a></td>
<td>Spécifie les portions de contenu à encoder en musique par le codec vocal.<br/> <dl> Windows XP et versions ultérieures.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md">MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode</a></td>
<td>Spécifie le mode du codec vocal.<br/> <dl> Windows XP et versions ultérieures.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista ou Windows 7<br/>                                       |
| En-tête<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmspdmoe.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets codec](codecobjects.md)
</dt> <dt>

[Utilisation du codec Windows Media Audio Voice](usingthewindowsmediaaudio9voicecodec.md)
</dt> </dl>

 

 





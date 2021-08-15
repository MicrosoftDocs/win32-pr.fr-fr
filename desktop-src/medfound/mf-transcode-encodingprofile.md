---
description: Spécifie le profil de conformité de périphérique pour l’encodage des fichiers ASF.
ms.assetid: 9a6b6402-ff53-4399-8616-06b7768a8737
title: Attribut MF_TRANSCODE_ENCODINGPROFILE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58b44a923abc563a84f3536fd6353ac2a3dd2352e472344edf7053d647674908
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244230"
---
# <a name="mf_transcode_encodingprofile-attribute"></a>\_Attribut ENCODINGPROFILE de transcodage MF \_

Spécifie le profil de conformité de périphérique pour l’encodage des fichiers ASF.

## <a name="data-type"></a>Type de données

**LPWSTR**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetAllocatedString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedstring).

Pour définir cet attribut, appelez [**IMFAttributes :: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Notes

utilisez cet attribut lors du transcodage sur un appareil qui prend en charge Windows support. si cet attribut est défini, l’encodeur utilise le profil de conformité de périphérique, ou modèle, pour Windows codecs multimédias. Définissez l’attribut sur le profil de transcodage avant de générer la topologie de transcodage.

La valeur de cet attribut peut être l’une des chaînes de modèle de conformité énumérées dans les rubriques suivantes :

-   [Modèles de conformité des périphériques audio](../wmformat/audio-device-conformance-templates.md)
-   [Modèles de conformité des périphériques vidéo](../wmformat/video-device-conformance-templates.md)

pour l’encodage Windows Media Video, le générateur de topologies utilise cet attribut pour définir la propriété [**MFPKEY \_ DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) sur l’encodeur. L’encodeur tente d’utiliser le modèle spécifié pour encoder le contenu. Pour obtenir le modèle réel, parcourez les nœuds de la topologie de transcodage pour obtenir un pointeur vers le nœud de l’encodeur. Ensuite, récupérez la valeur de la propriété [**MFPKEY \_ DECODERCOMPLEXITYPROFILE**](mfpkey-decodercomplexityprofileproperty.md) à partir de l’encodeur.

Le générateur de topologies utilise également la valeur de cet attribut pour définir la propriété « DeviceConformanceTemplate » sur le récepteur de média ASF.

Si cet attribut est défini, l’objet de métadonnées du fichier ASF est toujours généré, quelle que soit la valeur spécifiée par l’application de l’attribut de [ \_ \_ \_ \_ transfert de métadonnées d’omission de transcodage MF](mf-transcode-skip-metadata-transfer.md) .

Les valeurs typiques de cet attribut sont les suivantes :



| Valeur   | Description                      |
|---------|----------------------------------|
| FOURNISSEURS    | Vidéo sur les profils avancés           |
| CANAL    | Vidéo sur le profil principal               |
| SR    | Vidéo sur les profils simples             |
| "MP@LL" | Profil principal, vidéo de niveau moyen |
| NIV    | Profil audio, <= 160 Kbits/s    |



 

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[API de transcodage](transcode-api.md)
</dt> <dt>

[**IMFTranscodeProfile::GetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getaudioattributes)
</dt> <dt>

[**IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes)
</dt> <dt>

[**IMFTranscodeProfile::SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getvideoattributes)
</dt> <dt>

[**IMFTranscodeProfile::GetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 

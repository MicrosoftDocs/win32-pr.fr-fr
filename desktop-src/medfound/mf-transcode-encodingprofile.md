---
description: Spécifie le profil de conformité de périphérique pour l’encodage des fichiers ASF.
ms.assetid: 9a6b6402-ff53-4399-8616-06b7768a8737
title: Attribut MF_TRANSCODE_ENCODINGPROFILE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 020344cb2c2f6fc4a539c7cdbc8df0dc69d80d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527406"
---
# <a name="mf_transcode_encodingprofile-attribute"></a>\_Attribut ENCODINGPROFILE de transcodage MF \_

Spécifie le profil de conformité de périphérique pour l’encodage des fichiers ASF.

## <a name="data-type"></a>Type de données

**LPWSTR**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetAllocatedString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedstring).

Pour définir cet attribut, appelez [**IMFAttributes :: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Notes

Utilisez cet attribut lors du transcodage sur un appareil qui prend en charge Windows Media. Si cet attribut est défini, l’encodeur utilise le profil de conformité de périphérique, ou modèle, pour les codecs Windows Media. Définissez l’attribut sur le profil de transcodage avant de générer la topologie de transcodage.

La valeur de cet attribut peut être l’une des chaînes de modèle de conformité énumérées dans les rubriques suivantes :

-   [Modèles de conformité des périphériques audio](../wmformat/audio-device-conformance-templates.md)
-   [Modèles de conformité des périphériques vidéo](../wmformat/video-device-conformance-templates.md)

Pour l’encodage Windows Media Video, le générateur de topologies utilise cet attribut pour définir la propriété [**MFPKEY \_ DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) sur l’encodeur. L’encodeur tente d’utiliser le modèle spécifié pour encoder le contenu. Pour obtenir le modèle réel, parcourez les nœuds de la topologie de transcodage pour obtenir un pointeur vers le nœud de l’encodeur. Ensuite, récupérez la valeur de la propriété [**MFPKEY \_ DECODERCOMPLEXITYPROFILE**](mfpkey-decodercomplexityprofileproperty.md) à partir de l’encodeur.

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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                            |
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

 

 

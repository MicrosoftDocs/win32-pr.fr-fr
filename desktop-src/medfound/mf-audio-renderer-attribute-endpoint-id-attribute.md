---
description: Spécifie l’identificateur pour l’appareil de point de terminaison audio.
ms.assetid: f145fb80-c136-421c-9a65-e69c52109348
title: Attribut MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1dd99a42442342e25c748e12f8af84a03f2322b8c3dd24bb915b50b57952d65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941129"
---
# <a name="mf_audio_renderer_attribute_endpoint_id-attribute"></a>\_Attribut d' \_ ID de \_ \_ point de terminaison d’attribut de convertisseur audio MF \_

Spécifie l’identificateur pour l’appareil de point de terminaison audio.

## <a name="data-type"></a>Type de données

Chaîne de caractères larges

## <a name="remarks"></a>Remarques

Vous pouvez utiliser cet attribut pour configurer le convertisseur audio. L’utilisation dépend de la fonction que vous appelez pour créer le convertisseur audio :

-   [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): définissez cet attribut à l’aide du pointeur d’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) spécifié dans le paramètre *pAudioAttributes* .
-   [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): définissez cet attribut à l’aide du pointeur d’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) récupéré dans le paramètre *ppActivate* . Définissez l’attribut avant d’appeler [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).

Un périphérique de point de terminaison audio est un périphérique matériel qui se trouve à une extrémité d’un chemin de données audio, tel qu’un casque ou un haut-parleur. Pour obtenir l’identificateur de point de terminaison audio, utilisez les API audio principales suivantes :

-   Utilisez l’interface [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) pour énumérer les appareils sur le système.
-   Appelez [**IMMDevice :: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) pour obtenir l’identificateur de l’appareil.

Pour plus d’informations, consultez la documentation de l’API [audio principale](../coreaudio/core-audio-apis-in-windows-vista.md) . Si cet attribut n’est pas défini, le convertisseur audio utilise l’appareil de point de terminaison par défaut.

Si cet attribut est défini, ne définissez pas l’attribut de [**\_ rôle de point de \_ terminaison d’attribut de convertisseur \_ \_ \_ audio MF**](mf-audio-renderer-attribute-endpoint-role-attribute.md) . Si les deux attributs sont définis, un échec se produit lors de la création du convertisseur audio.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du convertisseur audio](audio-renderer-attributes.md)
</dt> <dt>

[**IMFAttributes :: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**IMFAttributes :: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[Convertisseur audio de streaming](streaming-audio-renderer.md)
</dt> </dl>

 

 

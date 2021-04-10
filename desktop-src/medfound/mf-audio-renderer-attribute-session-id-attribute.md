---
description: Spécifie la classe de stratégie audio pour le convertisseur audio.
ms.assetid: 80b028f5-7756-4bb8-b5e3-ebc8343e168c
title: Attribut MF_AUDIO_RENDERER_ATTRIBUTE_SESSION_ID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4952a60d4438e610677b494290e9738e469770d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866806"
---
# <a name="mf_audio_renderer_attribute_session_id-attribute"></a>Attribut d’ID de session de l' \_ attribut de convertisseur audio MF \_ \_ \_ \_

Spécifie la classe de stratégie audio pour le convertisseur audio.

## <a name="data-type"></a>Type de données

**GUID**

## <a name="remarks"></a>Notes

Cet attribut associe le convertisseur audio à une classe de stratégie audio. Chaque classe de stratégie dispose de son propre contrôle de volume et de stratégie. Si cet attribut n’est pas défini, le nouveau SAR rejoint la session audio par défaut de l’application. Pour plus d’informations, consultez [**IAudioClient :: Initialize**](/windows/win32/api/audioclient/nf-audioclient-iaudioclient-initialize) dans la documentation de l’API audio principale.

Vous pouvez utiliser cet attribut pour configurer le convertisseur audio. L’utilisation dépend de la fonction que vous appelez pour créer le convertisseur audio :

-   [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): définissez cet attribut à l’aide du pointeur d’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) spécifié dans le paramètre *pAudioAttributes* .
-   [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): définissez cet attribut à l’aide du pointeur d’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) récupéré dans le paramètre *ppActivate* . Définissez l’attribut avant d’appeler [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du convertisseur audio](audio-renderer-attributes.md)
</dt> <dt>

[**IMFAttributes :: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes :: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[Convertisseur audio de streaming](streaming-audio-renderer.md)
</dt> </dl>

 

 

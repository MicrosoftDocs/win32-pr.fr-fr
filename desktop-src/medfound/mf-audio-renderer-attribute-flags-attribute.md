---
description: Contient des indicateurs pour configurer le convertisseur audio.
ms.assetid: 07433904-1bf6-4e8d-9571-8d663bf4fd13
title: Attribut MF_AUDIO_RENDERER_ATTRIBUTE_FLAGS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1146ce4e363dca63819badd96abcd9d9e91051419df3b5007c237a002bb39d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105005"
---
# <a name="mf_audio_renderer_attribute_flags-attribute"></a>\_ \_ \_ Attribut indicateurs d’attribut de convertisseur audio MF \_

Contient des indicateurs pour configurer le convertisseur audio.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

La valeur de cet attribut est **une opération or au niveau du bit** des indicateurs suivants.



| Valeur                                                   | Description                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_indicateurs d' \_ attribut de convertisseur audio MF \_ \_ \_ CROSSPROCESS** | Le convertisseur audio utilise une session audio inter-processus. Cet indicateur active les convertisseurs audio dans plusieurs processus pour partager la même session audio, ainsi que les contrôles de volume et de stratégie associés.<br/> Si cet indicateur n’est pas défini, la session audio ne peut pas être partagée par les convertisseurs audio dans d’autres processus.<br/> |
| **\_indicateurs d’attribut de convertisseur audio MF non \_ \_ \_ \_ persistance**    | l’API de session audio Windows (WASAPI) ne rend pas persistantes les propriétés de cette session audio, telles que le volume de session.<br/> Si cet indicateur n’est pas défini, WASAPI conserve les propriétés de session audio.<br/>                                                                                                       |



 

Vous pouvez utiliser cet attribut pour configurer le convertisseur audio. L’utilisation dépend de la fonction que vous appelez pour créer le convertisseur audio :

-   [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): définissez cet attribut à l’aide du pointeur d’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) spécifié dans le paramètre *pAudioAttributes* .
-   [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): définissez cet attribut à l’aide du pointeur d’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) récupéré dans le paramètre *ppActivate* . Définissez l’attribut avant d’appeler [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).

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

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Convertisseur audio de streaming](streaming-audio-renderer.md)
</dt> </dl>

 

 





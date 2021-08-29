---
description: Spécifie le rôle de point de terminaison audio pour le convertisseur audio.
ms.assetid: f0456337-5351-457e-9830-920bf346bfc4
title: Attribut MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ROLE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b56d3d3c34403693edf259a35c66fe8ee9663f0b3106e2c846508d999852651a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941119"
---
# <a name="mf_audio_renderer_attribute_endpoint_role-attribute"></a>\_Attribut de \_ rôle de \_ \_ point de terminaison d’attribut de convertisseur audio MF \_

Spécifie le rôle de point de terminaison audio pour le convertisseur audio.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

Vous pouvez utiliser cet attribut pour configurer le convertisseur audio. L’utilisation dépend de la fonction que vous appelez pour créer le convertisseur audio :

-   [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): définissez cet attribut à l’aide du pointeur d’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) spécifié dans le paramètre *pAudioAttributes* .
-   [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): définissez cet attribut à l’aide du pointeur d’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) récupéré dans le paramètre *ppActivate* . Définissez l’attribut avant d’appeler [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).

Un périphérique de point de terminaison audio est un périphérique matériel qui se trouve à une extrémité d’un chemin de données audio, tel qu’un casque ou un haut-parleur.

Si cet attribut est défini, le convertisseur audio utilise le périphérique audio par défaut pour le rôle spécifié. La valeur de cet attribut est un membre de l’énumération **ERole** , qui est définie dans le fichier d’en-tête MMDeviceAPI. h. Pour plus d’informations, consultez la documentation de l’API audio principale. Si cet attribut n’est pas défini, le convertisseur audio utilise l’appareil de point de terminaison par défaut.

Si cet attribut est défini, ne définissez pas l’attribut ID de point de terminaison de l' [**\_ \_ attribut de convertisseur \_ \_ \_ audio MF**](mf-audio-renderer-attribute-endpoint-id-attribute.md) . Si les deux attributs sont définis, un échec se produit lors de la création du convertisseur audio.

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

 

 





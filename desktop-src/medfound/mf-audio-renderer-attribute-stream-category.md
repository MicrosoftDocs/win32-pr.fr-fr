---
description: Spécifie la catégorie de flux audio pour le convertisseur audio de streaming (SAR).
ms.assetid: 88E79DE6-2062-4471-A939-D1D4DD2EC42D
title: Attribut MF_AUDIO_RENDERER_ATTRIBUTE_STREAM_CATEGORY (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4acb6bd0f40d3c6fb3caa6b4dce8801f8fa60d31222265d5dca6ff5a132444e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714879"
---
# <a name="mf_audio_renderer_attribute_stream_category-attribute"></a>\_Attribut de \_ catégorie de \_ flux d’attribut de convertisseur audio \_ MF \_

Spécifie la catégorie de flux audio pour le [convertisseur audio de streaming](streaming-audio-renderer.md) (SAR).

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

Vous pouvez utiliser cet attribut pour configurer le convertisseur audio. L’utilisation dépend de la fonction que vous appelez pour créer le convertisseur audio.



| Fonction                                                               | Définition de l’attribut                                                                                                                                                                       |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)                 | Utilisez le pointeur [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) spécifié dans le paramètre *pAudioAttributes* .                                                                                          |
| [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) | Utilisez le pointeur [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) retourné dans le paramètre *ppActivate* . Définissez l’attribut avant d’appeler [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject). |



 

La valeur de l’attribut est un membre de l’énumération de [**\_ \_ catégorie de flux audio**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) . Le service audio utilise la catégorie Stream pour déterminer les stratégies audio lorsque plusieurs applications lisent l’audio en même temps.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 

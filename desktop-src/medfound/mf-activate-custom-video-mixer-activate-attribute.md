---
description: Spécifie un objet d’activation qui crée un mélangeur vidéo personnalisé pour le récepteur multimédia EVR (Enhanced Video Renderer).
ms.assetid: 60484f87-7588-4b52-93aa-ef8fad66d971
title: Attribut MF_ACTIVATE_CUSTOM_VIDEO_MIXER_ACTIVATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6268f3630b013235f3d365e0b8ab0578c9dd3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114611"
---
# <a name="mf_activate_custom_video_mixer_activate-attribute"></a>Activer \_ l' \_ \_ attribut d' \_ activation du MÉLANGEur vidéo personnalisé \_ MF

Spécifie un objet d’activation qui crée un mélangeur vidéo personnalisé pour le récepteur multimédia EVR (Enhanced Video Renderer).

## <a name="data-type"></a>Type de données

**IUnknown \** _

## <a name="remarks"></a>Notes

Si vous créez le EVR via un objet d’activation, vous pouvez utiliser cet attribut pour définir une console de mixage vidéo personnalisée sur EVR. Utilisez cet attribut comme suit :

1.  Appelez la fonction [_ *MFCreateVideoRendererActivate* *](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) pour créer un objet d’activation pour EVR. La fonction retourne un pointeur vers l’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .
2.  Définissez cet attribut sur le pointeur [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) en appelant [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown). La valeur de l’attribut est un pointeur vers un objet d’activation implémenté par l’appelant. L’objet d’activation de l’appelant doit exposer l’interface **IMFActivate** .

Si vous définissez cet attribut, EVR appelle [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) pour créer le mélangeur vidéo personnalisé. Le mixer vidéo doit exposer l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .

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

[Attributs de convertisseur vidéo améliorés](enhanced-video-renderer-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**IMFAttributes :: Setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[Objets d’activation](activation-objects.md)
</dt> </dl>

 

 





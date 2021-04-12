---
description: CLSID d’un mélangeur vidéo personnalisé pour le récepteur multimédia EVR (Enhanced Video Renderer).
ms.assetid: a3586e6f-a2a2-4932-8b43-a076f64c5958
title: Attribut MF_ACTIVATE_CUSTOM_VIDEO_MIXER_CLSID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc1049fb3bc77b65fb48fe9a4c10a059b2a4651
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318554"
---
# <a name="mf_activate_custom_video_mixer_clsid-attribute"></a>\_ \_ \_ \_ Attribut CLSID du mélangeur vidéo personnalisé MF activé \_

CLSID d’un mélangeur vidéo personnalisé pour le récepteur multimédia EVR (Enhanced Video Renderer).

## <a name="data-type"></a>Type de données

**GUID**

## <a name="remarks"></a>Notes

Si vous créez le EVR via un objet d’activation, vous pouvez utiliser cet attribut pour définir une console de mixage vidéo personnalisée sur EVR. Utilisez cet attribut comme suit :

1.  Appelez la fonction [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) pour créer un objet d’activation pour EVR. La fonction retourne un pointeur vers l’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .

2.  Définissez ce du sur le pointeur [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) en appelant [**IMFAttributes :: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid). La valeur de l’attribut est le CLSID du mélangeur vidéo personnalisé de l’application.

Si cet attribut est défini, EVR appelle **CoCreateInstance** avec le CLSID spécifié pour créer le mélangeur vidéo personnalisé. Le mixer vidéo doit exposer l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) . Le mélangeur est créé en tant que serveur COM in-process.

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

[**IMFAttributes :: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes :: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[Objets d’activation](activation-objects.md)
</dt> </dl>

 

 





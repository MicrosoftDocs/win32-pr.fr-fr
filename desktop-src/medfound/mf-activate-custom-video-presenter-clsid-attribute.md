---
description: CLSID d’un présentateur vidéo personnalisé pour le récepteur multimédia EVR (Enhanced Video Renderer).
ms.assetid: f035ee56-7582-45d3-bafe-dd9c821b6326
title: Attribut MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5afd39cf31cd0efaff4dc4d32756e1e27433d87fac643e4058897babd0f4f50f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877252"
---
# <a name="mf_activate_custom_video_presenter_clsid-attribute"></a>\_ \_ \_ \_ Attribut CLSID du présentateur vidéo personnalisé MF activé \_

CLSID d’un présentateur vidéo personnalisé pour le récepteur multimédia EVR (Enhanced Video Renderer).

## <a name="data-type"></a>Type de données

**GUID**

## <a name="remarks"></a>Remarques

Si vous créez le EVR via un objet d’activation, vous pouvez utiliser cet attribut pour définir un présentateur vidéo personnalisé sur EVR. Utilisez cet attribut comme suit :

1.  Appelez la fonction [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) pour créer un objet d’activation pour EVR. La fonction retourne un pointeur vers l’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .

2.  Définissez ce du sur le pointeur [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) en appelant [**IMFAttributes :: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid). La valeur de l’attribut est le CLSID du présentateur vidéo personnalisé de l’application.

Si cet attribut est défini, EVR appelle **CoCreateInstance** avec le CLSID spécifié pour créer le présentateur vidéo personnalisé. Le présentateur vidéo doit exposer l’interface [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) . Le présentateur est créé en tant que serveur COM in-process.

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

[Attributs de convertisseur vidéo améliorés](enhanced-video-renderer-attributes.md)
</dt> <dt>

[**IMFAttributes :: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes :: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[Objets d’activation](activation-objects.md)
</dt> <dt>

[Comment écrire un présentateur EVR](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 





---
description: Handle vers la fenêtre de découpage vidéo.
ms.assetid: 883bc7cf-f52f-4cb5-a942-b42b429b17a9
title: Attribut MF_ACTIVATE_VIDEO_WINDOW (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5249d98f7a3850d68e83be43cb851c4089253ba7fc782724631a2983285c9ce0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826929"
---
# <a name="mf_activate_video_window-attribute"></a>\_Attribut de \_ fenêtre vidéo d’activation MF \_

Handle vers la fenêtre de découpage vidéo.

## <a name="data-type"></a>Type de données

**UINT64**

Traiter en tant que **\_ pointeur DWORD** (**HWND**).

## <a name="remarks"></a>Remarques

Cet attribut s’applique à l’objet d’activation pour le convertisseur vidéo amélioré (EVR). La valeur est définie automatiquement quand vous appelez [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) pour créer l’objet d’activation EVR.

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

[**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[Objets d’activation](activation-objects.md)
</dt> </dl>

 

 





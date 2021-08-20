---
title: Message WM_CAP_SET_VIDEOFORMAT (VFW. h)
description: Le \_ message WM Cap \_ Set \_ VIDEOFORMAT définit le format des données de la vidéo capturée. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capSetVideoFormat.
ms.assetid: 4f9cf90d-7ccb-4fc7-aad5-3d7e082526be
keywords:
- message WM_CAP_SET_VIDEOFORMAT Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c543f613fedf54518579829d6825bd20dc4738ae03cb77f0996f8a58a123cb76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135013"
---
# <a name="wm_cap_set_videoformat-message"></a>\_Message VIDEOFORMAT de l’ensemble de connexions WM \_ \_

Le message **WM \_ Cap \_ Set \_ VIDEOFORMAT** définit le format des données de la vidéo capturée. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capSetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) .


```C++
WM_CAP_SET_VIDEOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (psVideoFormat); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Taille, en octets, de la structure référencée par **s**.

</dd> <dt>

<span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*
</dt> <dd>

Pointeur vers une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Étant donné que les formats vidéo sont spécifiques à l’appareil, les applications doivent vérifier la valeur de retour de cette fonction pour déterminer si le format est accepté par le pilote.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Capture vidéo](video-capture.md)
</dt> <dt>

[Messages de capture vidéo](video-capture-messages.md)
</dt> </dl>

 


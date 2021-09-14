---
title: Message WM_CAP_GET_VIDEOFORMAT (VFW. h)
description: Le \_ message WM \_ Cap \_ VIDEOFORMAT récupère une copie du format vidéo utilisé ou la taille requise pour le format vidéo. Vous pouvez envoyer ce message explicitement ou à l’aide des macros capGetVideoFormat et capGetVideoFormatSize.
ms.assetid: ac72dfdb-fe1a-4007-bdce-41e5e67d076a
keywords:
- message WM_CAP_GET_VIDEOFORMAT Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GET_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072d71366efee550b037d4a20388817954937854
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119445"
---
# <a name="wm_cap_get_videoformat-message"></a>Message WM d' \_ \_ extraction de \_ VIDEOFORMAT

Le **message \_ WM \_ Cap \_ VIDEOFORMAT** récupère une copie du format vidéo utilisé ou la taille requise pour le format vidéo. Vous pouvez envoyer ce message explicitement ou à l’aide des macros [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) et [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) .


```C++
WM_CAP_GET_VIDEOFORMAT 
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

Pointeur vers une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) . Vous pouvez également spécifier la **valeur null** pour récupérer le nombre d’octets nécessaires.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la taille, en octets, du format vidéo ou zéro si la fenêtre de capture n’est pas connectée à un pilote de capture. Pour les formats vidéo qui nécessitent une palette, la palette active est également retournée.

## <a name="remarks"></a>Notes

Étant donné que les formats vidéo compressés varient en fonction de la taille requise, les applications doivent d’abord récupérer la taille, puis allouer de la mémoire et enfin demander les données au format vidéo.

## <a name="requirements"></a>Spécifications



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

 


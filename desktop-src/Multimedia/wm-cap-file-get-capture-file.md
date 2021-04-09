---
title: Message WM_CAP_FILE_GET_CAPTURE_FILE (VFW. h)
description: Le \_ message WM Cap \_ file \_ obtenir \_ \_ un fichier de capture renvoie le nom du fichier de capture actuel. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capFileGetCaptureFile.
ms.assetid: 86ce2904-834d-449f-9ef8-5a158c55bbaa
keywords:
- Message WM_CAP_FILE_GET_CAPTURE_FILE Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_FILE_GET_CAPTURE_FILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7008e0b217f29ad9602afbdc41cc97f9cb7ecaa3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843186"
---
# <a name="wm_cap_file_get_capture_file-message"></a>Message de capture de fichier de la \_ \_ file d' \_ \_ \_ attente WM

Le message **WM \_ Cap \_ file obtenir un \_ \_ \_ fichier de capture** renvoie le nom du fichier de capture actuel. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capFileGetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) .


```C++
WM_CAP_FILE_GET_CAPTURE_FILE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Taille, en octets, de la mémoire tampon définie par l’application référencée par **szName**.

</dd> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Pointeur vers une mémoire tampon définie par l’application utilisée pour retourner le nom du fichier de capture sous la forme d’une chaîne terminée par le caractère null.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Le nom de fichier de capture par défaut est C : \\CAPTURE.AVI.

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

 

 






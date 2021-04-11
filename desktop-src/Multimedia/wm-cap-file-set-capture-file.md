---
title: Message WM_CAP_FILE_SET_CAPTURE_FILE (VFW. h)
description: Le message du fichier \_ \_ \_ de capture du jeu de fichiers WM Cap \_ \_ désigne le fichier utilisé pour la capture vidéo. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capFileSetCaptureFile.
ms.assetid: d96e498b-6322-4d48-a5d7-156e95f23740
keywords:
- Message WM_CAP_FILE_SET_CAPTURE_FILE Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SET_CAPTURE_FILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b3f59edfc9bf01f6bd2af3b9028f8e3315e2de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941646"
---
# <a name="wm_cap_file_set_capture_file-message"></a>\_Message du \_ \_ fichier de capture du jeu de fichiers de \_ l’embout WM \_

Le message du fichier de **\_ capture du jeu de \_ fichiers \_ \_ \_ WM Cap** désigne le fichier utilisé pour la capture vidéo. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) .


```C++
WM_CAP_FILE_SET_CAPTURE_FILE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Pointeur vers la chaîne terminée par le caractère null qui contient le nom du fichier de capture à utiliser.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** si le nom de fichier n’est pas valide, ou si la diffusion en continu ou la capture de frame unique est en cours.

## <a name="remarks"></a>Notes

Ce message stocke le nom de fichier dans une structure interne. Il ne crée pas, n’alloue pas ou n’ouvre pas le fichier spécifié. Le nom de fichier de capture par défaut est C : \\CAPTURE.AVI.

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

 

 






---
title: Message WM_CAP_FILE_SAVEDIB (VFW. h)
description: Le \_ message WM Cap \_ file \_ SAVEDIB copie le frame en cours dans un fichier DIB. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capFileSaveDIB.
ms.assetid: bf6d343b-9236-4e68-bbda-2ed6e197a5cb
keywords:
- Message WM_CAP_FILE_SAVEDIB Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SAVEDIB
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2155febfdac1b3f24133df47ce206c8e5ec33d3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466870"
---
# <a name="wm_cap_file_savedib-message"></a>\_ \_ Message SAVEDIB de fichier de la file d' \_ attente WM

Le message **WM \_ Cap \_ file \_ SAVEDIB** copie le frame en cours dans un fichier DIB. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capFileSaveDIB**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) .


```C++
WM_CAP_FILE_SAVEDIB 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Pointeur vers la chaîne terminée par le caractère null qui contient le nom du fichier DIB de destination.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

Si une erreur se produit et qu’une fonction de rappel d’erreur est définie à l’aide du message d' [**\_ erreur WM Cap \_ Set \_ callback \_**](wm-cap-set-callback-error.md) , la fonction de rappel d’erreur est appelée.

## <a name="remarks"></a>Notes

Si le pilote de capture fournit des frames dans un format compressé, cet appel tente de décompresser le frame avant d’écrire le fichier.

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

 

 






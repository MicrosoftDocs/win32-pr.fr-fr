---
title: Message WM_CAP_FILE_SAVEDIB (VFW. h)
description: Le \_ message WM Cap \_ file \_ SAVEDIB copie le frame en cours dans un fichier DIB. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capFileSaveDIB.
ms.assetid: bf6d343b-9236-4e68-bbda-2ed6e197a5cb
keywords:
- message WM_CAP_FILE_SAVEDIB Windows Multimedia
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
ms.openlocfilehash: 66d6dd9b8675e1fb8625349afc4b3f86347d71d605407d5c99fbca291ade744d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803809"
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

## <a name="remarks"></a>Remarques

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

 

 






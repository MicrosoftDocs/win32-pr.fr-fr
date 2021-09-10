---
title: Message WM_CAP_FILE_ALLOCATE (VFW. h)
description: Le \_ message WM \_ Cap \_ allocate crée (Préalloue) un fichier de capture d’une taille spécifiée. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capFileAlloc.
ms.assetid: 31ebe824-4a30-4212-9479-a5cbd8fc1e1d
keywords:
- message WM_CAP_FILE_ALLOCATE Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_FILE_ALLOCATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d36cec54e5775641118679b24b0d4b3b1767693
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124367900"
---
# <a name="wm_cap_file_allocate-message"></a>\_Message d' \_ allocation du fichier WM Cap \_

Le **message \_ WM \_ Cap \_ allocate** crée (Préalloue) un fichier de capture d’une taille spécifiée. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) .


```C++
WM_CAP_FILE_ALLOCATE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (DWORD) (dwSize); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>*dwSize nul*
</dt> <dd>

Taille, en octets, pour créer le fichier de capture.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

Si une erreur se produit et qu’une fonction de rappel d’erreur est définie à l’aide du message d' [**\_ erreur WM Cap \_ Set \_ callback \_**](wm-cap-set-callback-error.md) , la fonction de rappel d’erreur est appelée.

## <a name="remarks"></a>Remarques

Vous pouvez améliorer considérablement les performances de capture de streaming en préallouant un fichier de capture suffisamment grand pour stocker un clip vidéo entier et en défragmentant le fichier de capture avant de capturer le clip.

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

 

 






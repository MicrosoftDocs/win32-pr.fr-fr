---
title: Message WM_CAP_PAL_SAVE (VFW. h)
description: Le \_ message WM Cap \_ PAL \_ Save enregistre la palette actuelle dans un fichier palette. Les fichiers de palette utilisent généralement l’extension de nom de fichier. Adaptation. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capPaletteSave.
ms.assetid: b1fa3978-9147-403f-aa08-db1a803aa5ac
keywords:
- message WM_CAP_PAL_SAVE Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_PAL_SAVE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ff8703eafcc3c612fbde5bac7d15433758aa3d6ee44ab47697ffb25f9324dfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891879"
---
# <a name="wm_cap_pal_save-message"></a>\_Message d’enregistrement WM Cap \_ PAL \_

Le message **WM \_ Cap \_ PAL \_ Save** enregistre la palette actuelle dans un fichier palette. Les fichiers de palette utilisent généralement l’extension de nom de fichier. Adaptation. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capPaletteSave**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) .


```C++
WM_CAP_PAL_SAVE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Pointeur vers une chaîne se terminant par null et contenant le nom de fichier de palette.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

Si une erreur se produit et qu’une fonction de rappel d’erreur est définie à l’aide du message d' [**\_ erreur WM Cap \_ Set \_ callback \_**](wm-cap-set-callback-error.md) , la fonction de rappel d’erreur est appelée.

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

 

 






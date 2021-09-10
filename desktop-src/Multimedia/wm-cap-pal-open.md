---
title: Message WM_CAP_PAL_OPEN (VFW. h)
description: Le \_ message WM Cap \_ PAL \_ Open charge une nouvelle palette à partir d’un fichier de palette et la transmet à un pilote de capture.
ms.assetid: e77b518e-ff03-4622-978f-d9ebaa49c6a4
keywords:
- message WM_CAP_PAL_OPEN Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_PAL_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e949bab50294251543c50d72c8d8b169cfc5514
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124367972"
---
# <a name="wm_cap_pal_open-message"></a>Message d’ouverture de WM \_ Cap \_ PAL \_

Le message **WM \_ Cap \_ PAL \_ Open** charge une nouvelle palette à partir d’un fichier de palette et la transmet à un pilote de capture. Les fichiers de palette utilisent généralement l’extension de nom de fichier. Adaptation. Un pilote de capture utilise une palette lorsqu’il est requis par le format d’image numérisé spécifié. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capPaletteOpen**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) .


```C++
WM_CAP_PAL_OPEN 
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

 

 






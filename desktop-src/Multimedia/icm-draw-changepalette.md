---
title: Message ICM_DRAW_CHANGEPALETTE (VFW. h)
description: le ICM \_ message de dessin \_ CHANGEPALETTE avertit un pilote de rendu que la palette de films est en modification. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDrawChangePalette.
ms.assetid: 974fc0d8-d0c7-4a82-af84-68b53f753259
keywords:
- message ICM_DRAW_CHANGEPALETTE Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_CHANGEPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6364abb2c535158b2e64ff311041b00490c5958c
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364184"
---
# <a name="icm_draw_changepalette-message"></a>ICM \_ DESSINER le \_ message CHANGEPALETTE

le **ICM message de \_ dessin \_ CHANGEPALETTE** avertit un pilote de rendu que la palette de films est en modification. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDrawChangePalette**](/windows/desktop/api/Vfw/nf-vfw-icdrawchangepalette) .


```C++
ICM_DRAW_CHANGEPALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = 0; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*
</dt> <dd>

Pointeur vers une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenant le nouveau format et le tableau de couleurs facultatif.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK en cas de réussite ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Ce message doit être pris en charge par les gestionnaires de rendu installables qui dessinent des fichiers DIB avec une structure interne qui comprend une palette.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Gestionnaire de compression vidéo](video-compression-manager.md)
</dt> <dt>

[Messages de compression vidéo](video-compression-messages.md)
</dt> </dl>

 


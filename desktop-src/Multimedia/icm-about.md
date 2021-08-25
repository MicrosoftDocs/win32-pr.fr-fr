---
title: Message ICM_ABOUT (VFW. h)
description: le ICM \_ à propos du message indique à un pilote de compression vidéo d’afficher la boîte de dialogue à propos de ou interroge un pilote de compression vidéo pour déterminer s’il possède une boîte de dialogue à propos de. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICAbout.
ms.assetid: 6eca69a3-0463-48e6-befb-5003b7515e7d
keywords:
- message ICM_ABOUT Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_ABOUT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bf47ff93ef1986d805b2cb37697fdf4d86876c5552fe6aeffb00ff172673018
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785069"
---
# <a name="icm_about-message"></a>ICM \_ À propos du message

le **ICM \_ à propos** du message indique à un pilote de compression vidéo d’afficher la boîte de dialogue à propos de ou interroge un pilote de compression vidéo pour déterminer s’il possède une boîte de dialogue à propos de. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) .


```C++
ICM_ABOUT 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Handle de la fenêtre parente de la boîte de dialogue affichée. Vous pouvez également déterminer si un pilote a une boîte de dialogue à propos de en spécifiant-1 dans ce paramètre, comme dans la macro [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) . Le pilote retourne ICERR \_ OK s’il possède une boîte de dialogue à propos de ou ICERR \_ non prise en charge dans le cas contraire.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK si le pilote prend en charge ce message ou ICERR \_ non pris en charge dans le cas contraire.

## <a name="requirements"></a>Configuration requise



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

 

 






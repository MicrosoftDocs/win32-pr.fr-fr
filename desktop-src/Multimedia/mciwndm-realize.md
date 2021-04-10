---
title: Message MCIWNDM_REALIZE (VFW. h)
description: Le \_ message MCIWNDM de réalisation réalise la palette actuellement utilisée par le périphérique MCI dans une fenêtre MCIWnd. Cette macro est définie avec le \_ message MCIWNDM. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndRealize.
ms.assetid: fe8803b5-3500-44b4-97f7-784bedf0b362
keywords:
- Message MCIWNDM_REALIZE Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_REALIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef3a803791a4f8dfe94d128d42ea06a7b28e739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941733"
---
# <a name="mciwndm_realize-message"></a>MCIWNDM \_ réaliser le message

Le **message \_ MCIWNDM** de réalisation réalise la palette actuellement utilisée par le périphérique MCI dans une fenêtre MCIWnd. Cette macro est définie avec le **message \_ MCIWNDM** . Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) .


```C++
MCIWNDM_REALIZE 
wParam = (WPARAM) (BOOL) fBkgnd; 
lParam = 0; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="fBkgnd"></span><span id="fbkgnd"></span><span id="FBKGND"></span>*fBkgnd*
</dt> <dd>

Indicateur d’arrière-plan. Spécifiez **true** pour ce paramètre si la fenêtre est une application en arrière-plan.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Notes

**MCIWNDM \_ RÉALISEz** l’utilisation de la palette du périphérique MCI et appelle la fonction [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) . Si votre application gère explicitement les messages [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) et [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) , vous devez utiliser ce message dans votre application au lieu d’utiliser **RealizePalette**. Si le corps de l’un de ces gestionnaires de messages contient uniquement **RealizePalette**, transférez le message à la fenêtre MCIWnd, qui réalise automatiquement la palette.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize)
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**\_PALETTECHANGED WM**](/windows/desktop/gdi/wm-palettechanged)
</dt> <dt>

[**\_QUERYNEWPALETTE WM**](/windows/desktop/gdi/wm-querynewpalette)
</dt> </dl>

 


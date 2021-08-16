---
title: Message WM_GESTURENOTIFY (winuser. h)
description: Vous donne la possibilité de définir la configuration du geste.
ms.assetid: 83c23928-86ce-421d-bb84-5c41a770bf60
keywords:
- WM_GESTURENOTIFY message Windows Touch
topic_type:
- apiref
api_name:
- WM_GESTURENOTIFY
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d474f356310a0d7949cecf36e7af9cb586a76029171dfe27c1679970e481ed1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118435235"
---
# <a name="wm_gesturenotify-message"></a>\_Message WM GESTURENOTIFY

Vous donne la possibilité de définir la configuration du geste.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Inutilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers un [**GESTURENOTIFYSTRUCT**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Une valeur doit être retournée à partir de [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Remarques

Lorsque le message **WM \_ GESTURENOTIFY** est reçu, l’application peut utiliser [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) pour spécifier les gestes à recevoir. Ce message doit toujours être propagé à l’aide de la fonction [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) .

> [!Note]  
> Le fait de gérer le message **WM \_ GESTURENOTIFY** modifie la configuration du geste pour la durée de vie de la fenêtre, pas seulement pour le mouvement suivant.

 

## <a name="examples"></a>Exemples

L’exemple suivant montre comment activer tous les mouvements. Pour plus d’exemples, consultez [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig).


```C++
    switch (message)
    {
    case WM_GESTURENOTIFY:
        GESTURECONFIG gc = {0,GC_ALLGESTURES,0};
        BOOL bResult = SetGestureConfig(hWnd,0,1,&gc,sizeof(GESTURECONFIG));
            
        if(!bResult)
        {
            // an error
        }
        return DefWindowProc(hWnd, WM_GESTURENOTIFY, wParam, lParam);
    }
      
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                                  |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Notifications](notifications.md)
</dt> <dt>

[Windows Guide de programmation des gestes tactiles](guide-multi-touch-gestures.md)
</dt> <dt>

[**GESTURENOTIFYSTRUCT**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct)
</dt> <dt>

[**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig)
</dt> </dl>

 


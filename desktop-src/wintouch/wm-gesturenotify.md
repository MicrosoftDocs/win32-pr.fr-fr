---
title: Message WM_GESTURENOTIFY (winuser. h)
description: Vous donne la possibilité de définir la configuration du geste.
ms.assetid: 83c23928-86ce-421d-bb84-5c41a770bf60
keywords:
- WM_GESTURENOTIFY message Windows tactile
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
ms.openlocfilehash: 5e900e4b607760df16938080a49f97a3ab0cf2ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104530"
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

## <a name="remarks"></a>Notes

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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                               |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                                  |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Notifications](notifications.md)
</dt> <dt>

[Guide de programmation des gestes tactiles Windows](guide-multi-touch-gestures.md)
</dt> <dt>

[**GESTURENOTIFYSTRUCT**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct)
</dt> <dt>

[**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig)
</dt> </dl>

 


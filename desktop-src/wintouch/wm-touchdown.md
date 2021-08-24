---
title: Message WM_TOUCH (winuser. h)
description: Notifie la fenêtre lorsqu’un ou plusieurs points tactiles, tels qu’un doigt ou un stylet, touche une surface de digitaliseur tactile.
ms.assetid: 5dee8bab-34fa-4dd9-a65b-35883757ec80
keywords:
- WM_TOUCH message Windows TOUCH
topic_type:
- apiref
api_name:
- WM_TOUCH
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1034a229dbb1f3895726fcb3c1551e2dd0f390be0fd7bc2eb81d8331e582eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810099"
---
# <a name="wm_touch-message"></a>\_Message WM Touch

Notifie la fenêtre lorsqu’un ou plusieurs points tactiles, tels qu’un doigt ou un stylet, touche une surface de digitaliseur tactile.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Le mot de poids faible contient le nombre de points tactiles associés à ce message. Le mot de poids fort est réservé à une utilisation ultérieure.

</dd> <dt>

*lParam* 
</dt> <dd>

Contient une poignée d’entrée tactile qui peut être utilisée dans un appel à [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) pour récupérer des informations détaillées sur les points tactiles associés à ce message.

Ce handle est valide uniquement dans le processus actuel et ne doit pas être passé entre processus, sauf en tant que **lParam** dans un appel **SendMessage** ou **PostMessage** .

Lorsque l’application n’a plus besoin de ce handle, l’application doit appeler **CloseTouchInputHandle** pour libérer la mémoire de processus associée à ce descripteur. Si ce n’est pas le cas, cela peut entraîner une fuite de mémoire d’application.

Notez que le handle d’entrée tactile dans ce paramètre n’est plus valide une fois que le message a été passé à [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) va fermer et invalider ce handle.

Notez également que le handle d’entrée tactile dans ce paramètre n’est plus valide une fois que le message a été transféré à l’aide de [**PostMessage**](sendmessage--postmessage--and-related-functions.md), **SendMessage** ou de l’une de ses variantes. Ces fonctions vont fermer et invalider ce handle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la valeur zéro.

Si l’application ne traite pas le message, elle doit appeler [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). Si ce n’est pas le cas, l’application subit une fuite de mémoire, car le handle d’entrée tactile n’est pas fermé et la mémoire de processus associée n’est pas libérée.

## <a name="remarks"></a>Remarques

**WM \_ Les messages TACTILEs** ne respectent pas les régions **HTTRANSPARENT** des fenêtres. Si une fenêtre retourne **HTTRANSPARENT** en réponse à un message **WM \_ NCHITTEST** , les messages de la souris sont dirigés vers le parent et les messages **WM \_ Touch** sont directement dirigés vers la fenêtre.

## <a name="examples"></a>Exemples

Le code suivant est un exemple qui montre comment obtenir des informations détaillées sur les entrées tactiles associées à ce message.


```C++
UINT cInputs = LOWORD(wParam);
PTOUCHINPUT pInputs = new TOUCHINPUT[cInputs];
if (NULL != pInputs)
{
    if (GetTouchInputInfo((HTOUCHINPUT)lParam,
                          cInputs,
                          pInputs,
                          sizeof(TOUCHINPUT)))
    {
        // process pInputs
        if (!CloseTouchInputHandle((HTOUCHINPUT)lParam))
        {
            // error handling
        }
    }
    else
    {
        // GetLastError() and error handling
    }
    delete [] pInputs;
}
else
{
    // error handling, presumably out of memory
}
return DefWindowProc(hWnd, message, wParam, lParam);
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                                  |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Messages](messages.md)
</dt> <dt>

[Guide de programmation des manipulations et de l’inertie](manipulation-and-inertia.md)
</dt> <dt>

[Windows Guide de programmation de l’entrée tactile](guide-multi-touch-input.md)
</dt> </dl>

 


---
Description: Le \_ message WM Paint est envoyé lorsque le système ou une autre application effectue une requête pour peindre une partie de la fenêtre d’une application.
ms.assetid: afebaa07-cf00-47db-a919-46436f164881
title: Message WM_PAINT (winuser. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: b13e1779fb54a3db7905cb8fc738ef45558400f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982954"
---
# <a name="wm_paint-message"></a>\_Message de peinture WM

Le message **WM \_ Paint** est envoyé lorsque le système ou une autre application effectue une requête pour peindre une partie de la fenêtre d’une application. Le message est envoyé lorsque la fonction [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) ou [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) est appelée, ou par la [**fonction DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) lorsque l’application obtient un message **de \_ peinture WM** à l’aide de la fonction [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) .

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Une application retourne la valeur zéro si elle traite ce message.

## <a name="example"></a>Exemple

```c
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_DESTROY:
        PostQuitMessage(0);
        return 0;

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            HDC hdc = BeginPaint(hwnd, &ps);

            // All painting occurs here, between BeginPaint and EndPaint.
            FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
            EndPaint(hwnd, &ps);
        }
        return 0;
    }

    return DefWindowProc(hwnd, uMsg, wParam, lParam);
}

```

Exemple tiré d' [exemples classiques Windows](https://github.com/microsoft/Windows-classic-samples/blob/18cbd05ee44455cd7552804dcf2c9d6db619b412/Samples/Win7Samples/begin/LearnWin32/HelloWorld/cpp/main.cpp) sur GitHub.

## <a name="remarks"></a>Notes

Le message **WM \_ Paint** est généré par le système et ne doit pas être envoyé par une application. Pour forcer une fenêtre à dessiner dans un contexte de périphérique spécifique, utilisez le message WM [**\_ Print**](wm-print.md) ou [**WM \_ PRINTCLIENT**](wm-printclient.md) . Notez que cela nécessite que la fenêtre cible prenne en charge le message **WM \_ PRINTCLIENT** . La plupart des contrôles courants prennent en charge le message **WM \_ PRINTCLIENT** .

La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  valide la région de mise à jour. La fonction peut également envoyer le message [**WM \_ NCPAINT**](wm-ncpaint.md) à la procédure de fenêtre si le frame de fenêtre doit être peint et envoyer le message [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) si l’arrière-plan de la fenêtre doit être effacé.

Le système envoie ce message lorsqu’il n’y a pas d’autres messages dans la file d’attente des messages de l’application. [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) détermine où envoyer le message. [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) détermine le message à distribuer. **GetMessage** retourne le message de **\_ peinture WM** lorsqu’il n’y a pas d’autres messages dans la file d’attente de messages de l’application, et **DispatchMessage** envoie le message à la procédure de fenêtre appropriée.

Une fenêtre peut recevoir des messages de peinture internes suite à l’appel de [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) avec l' \_ indicateur RDW INTERNALPAINT défini. Dans ce cas, la fenêtre peut ne pas avoir de zone de mise à jour. Une application peut appeler la fonction [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) pour déterminer si la fenêtre a une région de mise à jour. Si **GetUpdateRect** retourne la valeur zéro, l’application n’a pas besoin d’appeler les fonctions [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) et [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) .

Une application doit vérifier s’il existe des peintures internes nécessaires en examinant ses structures de données internes pour chaque message **WM \_ Paint** , car un message **\_ WM** peut avoir été provoqué par une région de mise à jour non null et un appel à [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) avec l' \_ indicateur RDW INTERNALPAINT défini.

Le système envoie un message **de \_ peinture WM** interne une seule fois. Après qu’un message de **\_ peinture WM** interne a été retourné à partir de [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) ou qu’il est envoyé à une fenêtre par [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow), le système ne publie pas ou n’envoie pas d’autres messages de **\_ peinture WM** tant que la fenêtre n’est pas invalidée ou jusqu’à ce que [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) soit rappelé avec l' \_ indicateur RDW INTERNALPAINT défini.

Pour certains contrôles courants, le traitement du message de **\_ peinture WM** par défaut vérifie le paramètre *wParam* . Si *wParam* est non null, le contrôle suppose que la valeur est un HDC et peint à l’aide de ce contexte de périphérique.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble de la peinture et du dessin](painting-and-drawing.md)
</dt> <dt>

[Peinture et dessin de messages](painting-and-drawing-messages.md)
</dt> <dt>

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)
</dt> <dt>

[**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint)
</dt> <dt>

[**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect)
</dt> <dt>

[**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)
</dt> <dt>

[**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow)
</dt> <dt>

[**\_ERASEBKGND WM**](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[**\_NCPAINT WM**](wm-ncpaint.md)
</dt> <dt>

[**\_impression WM**](wm-print.md)
</dt> <dt>

[**\_PRINTCLIENT WM**](wm-printclient.md)
</dt> </dl>

 

 

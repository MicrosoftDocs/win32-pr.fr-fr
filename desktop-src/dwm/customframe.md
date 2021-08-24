---
title: Frame de fenêtre personnalisé à l’aide de DWM
description: Cette rubrique montre comment utiliser les API Gestionnaire de fenêtrage (DWM) pour créer des frames de fenêtre personnalisés pour votre application.
ms.assetid: 7f7dc902-40d3-44e9-adc2-05a39c634eb3
keywords:
- Gestionnaire de fenêtrage (DWM), frames de fenêtre personnalisés
- DWM (Gestionnaire de fenêtrage), frames de fenêtre personnalisés
- frames de fenêtre personnalisés
- suppression des frames standard
- extension des frames client
- Gestionnaire de fenêtrage (DWM), extension des frames client
- DWM (Gestionnaire de fenêtrage), étendre des frames client
- Gestionnaire de fenêtrage (DWM), suppression des frames standard
- DWM (Gestionnaire de fenêtrage), suppression des frames standard
- Gestionnaire de fenêtrage (DWM), dessin dans des frames étendus
- DWM (Gestionnaire de fenêtrage), dessin dans des frames étendus
- dessiner dans des frames étendus
- test des accès
- Gestionnaire de fenêtrage (DWM), test de positionnement
- DWM (Gestionnaire de fenêtrage), test de positionnement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b440f475dfacc610354ce151ab0be42dbbe3069390b1efa211195252f7a3914
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741455"
---
# <a name="custom-window-frame-using-dwm"></a>Frame de fenêtre personnalisé à l’aide de DWM

Cette rubrique montre comment utiliser les API Gestionnaire de fenêtrage (DWM) pour créer des frames de fenêtre personnalisés pour votre application.

-   [Introduction](#introduction)
-   [Extension du frame client](#extending-the-client-frame)
-   [Suppression du frame standard](#removing-the-standard-frame)
-   [Dessin dans la fenêtre frame étendue](#drawing-in-the-extended-frame-window)
-   [Activation du test de positionnement pour le frame personnalisé](#enabling-hit-testing-for-the-custom-frame)
-   [Annexe A : exemple de procédure de fenêtre](#appendix-a-sample-window-procedure)
-   [Annexe B : peinture du titre de la légende](#appendix-b-painting-the-caption-title)
-   [Annexe C : fonction HitTestNCA](#appendix-c-hittestnca-function)
-   [Rubriques connexes](#related-topics)

## <a name="introduction"></a>Introduction

dans Windows Vista et versions ultérieures, l’apparence des zones non clientes des fenêtres d’application (la barre de titre, l’icône, la bordure de la fenêtre et les boutons de légende) est contrôlée par le DWM. À l’aide des API DWM, vous pouvez modifier la façon dont le DWM restitue le frame d’une fenêtre.

L’une des fonctionnalités des API DWM est la possibilité d’étendre le frame d’application dans la zone cliente. Cela vous permet d’intégrer un élément d’interface utilisateur client, tel qu’une barre d’outils, dans le frame, en donnant à l’interface utilisateur des contrôles un emplacement plus important dans l’interface utilisateur de l’application. par exemple, Windows Internet Explorer 7 sur Windows Vista intègre la barre de navigation dans le cadre de la fenêtre en étendant le haut du cadre comme indiqué dans la capture d’écran suivante.

![barre de navigation intégrée dans le frame de fenêtre.](images/ie7-extendedborder-boxed.png)

La possibilité d’étendre le frame de la fenêtre vous permet également de créer des frames personnalisés tout en conservant l’apparence de la fenêtre. par exemple, Microsoft Office Word 2007 dessine le bouton Office et la barre d’outils accès rapide dans le cadre personnalisé tout en fournissant les boutons standard réduire, agrandir et fermer la légende, comme illustré dans la capture d’écran suivante.

![bouton Office et barre d’outils accès rapide dans Word 2007](images/word2007-customborder-boxed.png)

## <a name="extending-the-client-frame"></a>Extension du frame client

La fonctionnalité d’extension du frame dans la zone cliente est exposée par la fonction [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) . Pour étendre le frame, transmettez le descripteur de la fenêtre cible avec les valeurs de marge intérieure à **DwmExtendFrameIntoClientArea**. Les valeurs d’incrustation de marge déterminent la distance d’extension du cadre sur les quatre côtés de la fenêtre.

Le code suivant illustre l’utilisation de [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) pour étendre le frame.


```
// Handle the window activation.
if (message == WM_ACTIVATE)
{
    // Extend the frame into the client area.
    MARGINS margins;

    margins.cxLeftWidth = LEFTEXTENDWIDTH;      // 8
    margins.cxRightWidth = RIGHTEXTENDWIDTH;    // 8
    margins.cyBottomHeight = BOTTOMEXTENDWIDTH; // 20
    margins.cyTopHeight = TOPEXTENDWIDTH;       // 27

    hr = DwmExtendFrameIntoClientArea(hWnd, &margins);

    if (!SUCCEEDED(hr))
    {
        // Handle the error.
    }

    fCallDWP = true;
    lRet = 0;
}
```



Notez que l’extension de cadre est effectuée dans le message [**WM \_ Activate**](/windows/desktop/inputdev/wm-activate) et non dans le message [**WM \_ Create**](/windows/desktop/winmsg/wm-create) . Cela garantit que l’extension de frame est gérée correctement quand la fenêtre est à sa taille par défaut et quand elle est agrandie.

L’illustration suivante montre un cadre de fenêtre standard (à gauche) et le même cadre de fenêtre étendu (à droite). le frame est étendu à l’aide de l’exemple de code précédent et de l’arrière-plan Microsoft Visual Studio [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) / [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) par défaut ( \_ fenêtre couleur + 1).

![capture d’écran d’un cadre standard (gauche) et étendu (à droite) avec arrière-plan blanc](images/white-sidebyside.png)

La différence visuelle entre ces deux fenêtres est très subtile. La seule différence entre les deux est que la bordure noire fine de la région du client dans la fenêtre de gauche est absente de la fenêtre de droite. La raison de cette bordure manquante est qu’elle est incorporée dans le frame étendu, mais que le reste de la zone cliente ne l’est pas. Pour que les frames étendus soient visibles, les régions sous-jacentes de chaque côté du cadre étendu doivent avoir des données de pixels avec une valeur alpha de 0. La bordure noire autour de la région du client contient des données de pixels dans lesquelles toutes les valeurs de couleur (rouge, vert, bleu et alpha) sont définies sur 0. Le reste de l’arrière-plan n’a pas la valeur alpha définie sur 0, donc le reste du frame étendu n’est pas visible.

Le moyen le plus simple de s’assurer que les frames étendus sont visibles consiste à peindre l’ensemble de la région cliente en noir. Pour ce faire, initialisez le membre *hbrBackground* de votre structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) ou [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) sur le handle du pinceau noir de stock \_ . L’illustration suivante montre le même frame standard (à gauche) et le même cadre étendu (à droite). Cette fois, cependant, *hbrBackground* est défini sur la \_ poignée du pinceau noir obtenue à partir de la fonction [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) .

![capture d’écran d’un bloc standard (à gauche) et étendu (à droite) avec arrière-plan noir](images/standard-extended-sidebyside.png)

## <a name="removing-the-standard-frame"></a>Suppression du frame standard

Une fois que vous avez étendu le frame de votre application et que vous l’avez rendu visible, vous pouvez supprimer le cadre standard. La suppression du frame standard vous permet de contrôler la largeur de chaque côté du cadre plutôt que d’étendre simplement le cadre standard.

Pour supprimer le frame de fenêtre standard, vous devez gérer le message [**WM \_ NCCALCSIZE**](/windows/desktop/winmsg/wm-nccalcsize) , en particulier lorsque sa valeur *wParam* est **true** et que la valeur de retour est 0. En procédant ainsi, votre application utilise la zone de fenêtre entière comme zone cliente, en supprimant le frame standard.

Les résultats de la gestion du message [**WM \_ NCCALCSIZE**](/windows/desktop/winmsg/wm-nccalcsize) ne sont pas visibles tant que la région du client n’a pas besoin d’être redimensionnée. Jusqu’à ce moment-là, la vue initiale de la fenêtre apparaît avec le frame standard et les bordures étendues. Pour remédier à cela, vous devez redimensionner votre fenêtre ou exécuter une action qui initie un message **WM \_ NCCALCSIZE** au moment de la création de la fenêtre. Pour ce faire, vous pouvez utiliser la fonction [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) pour déplacer votre fenêtre et la redimensionner. Le code suivant illustre un appel à **SetWindowPos** qui force l’envoi d’un message **WM \_ NCCALCSIZE** à l’aide des attributs du rectangle de la fenêtre active et de l' \_ indicateur de FRAMECHANGED SWP.


```
// Handle window creation.
if (message == WM_CREATE)
{
    RECT rcClient;
    GetWindowRect(hWnd, &rcClient);

    // Inform the application of the frame change.
    SetWindowPos(hWnd, 
                 NULL, 
                 rcClient.left, rcClient.top,
                 RECTWIDTH(rcClient), RECTHEIGHT(rcClient),
                 SWP_FRAMECHANGED);

    fCallDWP = true;
    lRet = 0;
}
```



L’illustration suivante montre le cadre standard (à gauche) et le cadre nouvellement étendu sans le cadre standard (à droite).

![capture d’écran d’un cadre standard (à gauche) et d’un cadre personnalisé (à droite)](images/standard-custom-sidebyside.png)

## <a name="drawing-in-the-extended-frame-window"></a>Dessin dans la fenêtre frame étendue

En supprimant le cadre standard, vous perdez le dessin automatique de l’icône et du titre de l’application. Pour rajouter ces éléments à votre application, vous devez les dessiner vous-même. Pour ce faire, examinez d’abord les modifications qui se sont produites dans votre zone cliente.

Avec la suppression du frame standard, votre zone cliente se compose désormais de la totalité de la fenêtre, y compris le cadre étendu. Cela comprend la région dans laquelle les boutons de légende sont dessinés. Dans la comparaison côte à côte suivante, la zone cliente pour le frame standard et le frame étendu personnalisé est mise en surbrillance en rouge. La zone cliente de la fenêtre frame standard (à gauche) est la région noire. Dans la fenêtre frame étendue (à droite), la zone cliente est la fenêtre entière.

![capture d’écran des zones clientes en rouge en surbrillance dans le frame standard et personnalisé](images/clientarea-sidebyside.png)

Étant donné que la totalité de la fenêtre est votre zone cliente, vous pouvez simplement dessiner ce que vous souhaitez dans le frame étendu. Pour ajouter un titre à votre application, il vous suffit de dessiner du texte dans la région appropriée. L’illustration suivante montre le texte à thème dessiné sur le cadre de légende personnalisé. Le titre est dessiné à l’aide de la fonction [**DrawThemeTextEx**](/windows/win32/api/uxtheme/nf-uxtheme-drawthemetextex) . Pour afficher le code qui peint le titre, consultez l' [annexe B : peinture du titre de la légende](#appendix-b-painting-the-caption-title).

![capture d’écran d’un cadre personnalisé avec titre](images/custom-caption-title.png)

> [!Note]  
> Quand vous dessinez dans votre Frame personnalisé, soyez prudent lorsque vous placez des contrôles d’interface utilisateur. Étant donné que la totalité de la fenêtre est votre région cliente, vous devez ajuster le placement de votre contrôle d’interface utilisateur pour chaque largeur d’image si vous ne souhaitez pas qu’elles apparaissent sur ou dans le frame étendu.

 

## <a name="enabling-hit-testing-for-the-custom-frame"></a>Activation du test de positionnement pour le frame personnalisé

L’un des effets secondaires de la suppression du frame standard est la perte du comportement de redimensionnement et de déplacement par défaut. Pour que votre application puisse émuler correctement le comportement de fenêtre standard, vous devez implémenter une logique pour gérer le test de positionnement de bouton de légende et le redimensionnement/déplacement de frame.

Pour le test de positionnement des boutons de légende, DWM fournit la fonction [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) . Pour tester correctement les boutons de légende dans les scénarios de frame personnalisé, les messages doivent d’abord être transmis à **DwmDefWindowProc** pour être géré. **DwmDefWindowProc** retourne la **valeur true** si un message est géré et **false** si ce n’est pas le cas. Si le message n’est pas géré par **DwmDefWindowProc**, votre application doit gérer le message lui-même ou passer le message sur [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

Pour le redimensionnement et le déplacement de frame, votre application doit fournir la logique de test de positionnement et gérer les messages de test de positionnement de frame. Les messages de test de positionnement de frame sont envoyés via le message [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) , même si votre application crée un frame personnalisé sans le frame standard. Le code suivant illustre la gestion du message **WM \_ NCHITTEST** lorsque [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) ne le gère pas. Pour afficher le code de la `HitTestNCA` fonction appelée, consultez l' [annexe C : fonction HitTestNCA](#appendix-c-hittestnca-function).


```
// Handle hit testing in the NCA if not handled by DwmDefWindowProc.
if ((message == WM_NCHITTEST) && (lRet == 0))
{
    lRet = HitTestNCA(hWnd, wParam, lParam);

    if (lRet != HTNOWHERE)
    {
        fCallDWP = false;
    }
}
```



## <a name="appendix-a-sample-window-procedure"></a>Annexe A : exemple de procédure de fenêtre

L’exemple de code suivant illustre une procédure de fenêtre et ses fonctions de travail de prise en charge utilisées pour créer une application Frame personnalisée.


```
//
//  Main WinProc.
//
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    bool fCallDWP = true;
    BOOL fDwmEnabled = FALSE;
    LRESULT lRet = 0;
    HRESULT hr = S_OK;

    // Winproc worker for custom frame issues.
    hr = DwmIsCompositionEnabled(&fDwmEnabled);
    if (SUCCEEDED(hr))
    {
        lRet = CustomCaptionProc(hWnd, message, wParam, lParam, &fCallDWP);
    }

    // Winproc worker for the rest of the application.
    if (fCallDWP)
    {
        lRet = AppWinProc(hWnd, message, wParam, lParam);
    }
    return lRet;
}

//
// Message handler for handling the custom caption messages.
//
LRESULT CustomCaptionProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam, bool* pfCallDWP)
{
    LRESULT lRet = 0;
    HRESULT hr = S_OK;
    bool fCallDWP = true; // Pass on to DefWindowProc?

    fCallDWP = !DwmDefWindowProc(hWnd, message, wParam, lParam, &lRet);

    // Handle window creation.
    if (message == WM_CREATE)
    {
        RECT rcClient;
        GetWindowRect(hWnd, &rcClient);

        // Inform application of the frame change.
        SetWindowPos(hWnd, 
                     NULL, 
                     rcClient.left, rcClient.top,
                     RECTWIDTH(rcClient), RECTHEIGHT(rcClient),
                     SWP_FRAMECHANGED);

        fCallDWP = true;
        lRet = 0;
    }

    // Handle window activation.
    if (message == WM_ACTIVATE)
    {
        // Extend the frame into the client area.
        MARGINS margins;

        margins.cxLeftWidth = LEFTEXTENDWIDTH;      // 8
        margins.cxRightWidth = RIGHTEXTENDWIDTH;    // 8
        margins.cyBottomHeight = BOTTOMEXTENDWIDTH; // 20
        margins.cyTopHeight = TOPEXTENDWIDTH;       // 27

        hr = DwmExtendFrameIntoClientArea(hWnd, &margins);

        if (!SUCCEEDED(hr))
        {
            // Handle error.
        }

        fCallDWP = true;
        lRet = 0;
    }

    if (message == WM_PAINT)
    {
        HDC hdc;
        {
            PAINTSTRUCT ps;
            hdc = BeginPaint(hWnd, &ps);
            PaintCustomCaption(hWnd, hdc);
            EndPaint(hWnd, &ps);
        }

        fCallDWP = true;
        lRet = 0;
    }

    // Handle the non-client size message.
    if ((message == WM_NCCALCSIZE) && (wParam == TRUE))
    {
        // Calculate new NCCALCSIZE_PARAMS based on custom NCA inset.
        NCCALCSIZE_PARAMS *pncsp = reinterpret_cast<NCCALCSIZE_PARAMS*>(lParam);

        pncsp->rgrc[0].left   = pncsp->rgrc[0].left   + 0;
        pncsp->rgrc[0].top    = pncsp->rgrc[0].top    + 0;
        pncsp->rgrc[0].right  = pncsp->rgrc[0].right  - 0;
        pncsp->rgrc[0].bottom = pncsp->rgrc[0].bottom - 0;

        lRet = 0;
        
        // No need to pass the message on to the DefWindowProc.
        fCallDWP = false;
    }

    // Handle hit testing in the NCA if not handled by DwmDefWindowProc.
    if ((message == WM_NCHITTEST) && (lRet == 0))
    {
        lRet = HitTestNCA(hWnd, wParam, lParam);

        if (lRet != HTNOWHERE)
        {
            fCallDWP = false;
        }
    }

    *pfCallDWP = fCallDWP;

    return lRet;
}

//
// Message handler for the application.
//
LRESULT AppWinProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;
    HRESULT hr; 
    LRESULT result = 0;

    switch (message)
    {
        case WM_CREATE:
            {}
            break;
        case WM_COMMAND:
            wmId    = LOWORD(wParam);
            wmEvent = HIWORD(wParam);

            // Parse the menu selections:
            switch (wmId)
            {
                default:
                    return DefWindowProc(hWnd, message, wParam, lParam);
            }
            break;
        case WM_PAINT:
            {
                hdc = BeginPaint(hWnd, &ps);
                PaintCustomCaption(hWnd, hdc);
                
                // Add any drawing code here...
    
                EndPaint(hWnd, &ps);
            }
            break;
        case WM_DESTROY:
            PostQuitMessage(0);
            break;
        default:
            return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



## <a name="appendix-b-painting-the-caption-title"></a>Annexe B : peinture du titre de la légende

Le code suivant montre comment peindre un titre de légende sur le frame étendu. Cette fonction doit être appelée à partir des appels [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) et [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) .


```
// Paint the title on the custom frame.
void PaintCustomCaption(HWND hWnd, HDC hdc)
{
    RECT rcClient;
    GetClientRect(hWnd, &rcClient);

    HTHEME hTheme = OpenThemeData(NULL, L"CompositedWindow::Window");
    if (hTheme)
    {
        HDC hdcPaint = CreateCompatibleDC(hdc);
        if (hdcPaint)
        {
            int cx = RECTWIDTH(rcClient);
            int cy = RECTHEIGHT(rcClient);

            // Define the BITMAPINFO structure used to draw text.
            // Note that biHeight is negative. This is done because
            // DrawThemeTextEx() needs the bitmap to be in top-to-bottom
            // order.
            BITMAPINFO dib = { 0 };
            dib.bmiHeader.biSize            = sizeof(BITMAPINFOHEADER);
            dib.bmiHeader.biWidth           = cx;
            dib.bmiHeader.biHeight          = -cy;
            dib.bmiHeader.biPlanes          = 1;
            dib.bmiHeader.biBitCount        = BIT_COUNT;
            dib.bmiHeader.biCompression     = BI_RGB;

            HBITMAP hbm = CreateDIBSection(hdc, &dib, DIB_RGB_COLORS, NULL, NULL, 0);
            if (hbm)
            {
                HBITMAP hbmOld = (HBITMAP)SelectObject(hdcPaint, hbm);

                // Setup the theme drawing options.
                DTTOPTS DttOpts = {sizeof(DTTOPTS)};
                DttOpts.dwFlags = DTT_COMPOSITED | DTT_GLOWSIZE;
                DttOpts.iGlowSize = 15;

                // Select a font.
                LOGFONT lgFont;
                HFONT hFontOld = NULL;
                if (SUCCEEDED(GetThemeSysFont(hTheme, TMT_CAPTIONFONT, &lgFont)))
                {
                    HFONT hFont = CreateFontIndirect(&lgFont);
                    hFontOld = (HFONT) SelectObject(hdcPaint, hFont);
                }

                // Draw the title.
                RECT rcPaint = rcClient;
                rcPaint.top += 8;
                rcPaint.right -= 125;
                rcPaint.left += 8;
                rcPaint.bottom = 50;
                DrawThemeTextEx(hTheme, 
                                hdcPaint, 
                                0, 0, 
                                szTitle, 
                                -1, 
                                DT_LEFT | DT_WORD_ELLIPSIS, 
                                &rcPaint, 
                                &DttOpts);

                // Blit text to the frame.
                BitBlt(hdc, 0, 0, cx, cy, hdcPaint, 0, 0, SRCCOPY);

                SelectObject(hdcPaint, hbmOld);
                if (hFontOld)
                {
                    SelectObject(hdcPaint, hFontOld);
                }
                DeleteObject(hbm);
            }
            DeleteDC(hdcPaint);
        }
        CloseThemeData(hTheme);
    }
}
```



## <a name="appendix-c-hittestnca-function"></a>Annexe C : fonction HitTestNCA

Le code suivant illustre la `HitTestNCA` fonction utilisée [pour activer le test de positionnement pour le frame personnalisé](#enabling-hit-testing-for-the-custom-frame). Cette fonction gère la logique de test de positionnement pour le [**\_ NCHITTEST WM**](/windows/desktop/inputdev/wm-nchittest) lorsque [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) ne gère pas le message.


```
// Hit test the frame for resizing and moving.
LRESULT HitTestNCA(HWND hWnd, WPARAM wParam, LPARAM lParam)
{
    // Get the point coordinates for the hit test.
    POINT ptMouse = { GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam)};

    // Get the window rectangle.
    RECT rcWindow;
    GetWindowRect(hWnd, &rcWindow);

    // Get the frame rectangle, adjusted for the style without a caption.
    RECT rcFrame = { 0 };
    AdjustWindowRectEx(&rcFrame, WS_OVERLAPPEDWINDOW & ~WS_CAPTION, FALSE, NULL);

    // Determine if the hit test is for resizing. Default middle (1,1).
    USHORT uRow = 1;
    USHORT uCol = 1;
    bool fOnResizeBorder = false;

    // Determine if the point is at the top or bottom of the window.
    if (ptMouse.y >= rcWindow.top && ptMouse.y < rcWindow.top + TOPEXTENDWIDTH)
    {
        fOnResizeBorder = (ptMouse.y < (rcWindow.top - rcFrame.top));
        uRow = 0;
    }
    else if (ptMouse.y < rcWindow.bottom && ptMouse.y >= rcWindow.bottom - BOTTOMEXTENDWIDTH)
    {
        uRow = 2;
    }

    // Determine if the point is at the left or right of the window.
    if (ptMouse.x >= rcWindow.left && ptMouse.x < rcWindow.left + LEFTEXTENDWIDTH)
    {
        uCol = 0; // left side
    }
    else if (ptMouse.x < rcWindow.right && ptMouse.x >= rcWindow.right - RIGHTEXTENDWIDTH)
    {
        uCol = 2; // right side
    }

    // Hit test (HTTOPLEFT, ... HTBOTTOMRIGHT)
    LRESULT hitTests[3][3] = 
    {
        { HTTOPLEFT,    fOnResizeBorder ? HTTOP : HTCAPTION,    HTTOPRIGHT },
        { HTLEFT,       HTNOWHERE,     HTRIGHT },
        { HTBOTTOMLEFT, HTBOTTOM, HTBOTTOMRIGHT },
    };

    return hitTests[uRow][uCol];
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble du Gestionnaire de fenêtres du Bureau](dwm-overview.md)
</dt> </dl>

 

 
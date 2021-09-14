---
title: Utilisation de styles visuels avec des contrôles personnalisés et Owner-Drawn
description: Cette rubrique explique comment utiliser l’API des styles visuels pour appliquer des styles visuels à des contrôles personnalisés ou à des contrôles owner-drawn.
ms.assetid: 8b06f9ce-702c-48f8-8cf3-2718a09b8d77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7025bdf7c589649ac62bed7a4ea4f55c418940
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115225"
---
# <a name="using-visual-styles-with-custom-and-owner-drawn-controls"></a>Utilisation de styles visuels avec des contrôles personnalisés et Owner-Drawn

Cette rubrique explique comment utiliser l’API des styles visuels pour appliquer des styles visuels à des contrôles personnalisés ou à des contrôles owner-drawn.

-   [Dessiner des contrôles avec des styles visuels](#drawing-controls-with-visual-styles)
-   [Réponse aux modifications de thème](#responding-to-theme-changes)
-   [Rubriques connexes](#related-topics)

## <a name="drawing-controls-with-visual-styles"></a>Dessiner des contrôles avec des styles visuels

Les styles visuels sont pris en charge par ComCtrl32.dll version 6 et versions ultérieures. Si votre application est configurée pour utiliser ComCtrl32.dll version 6 et ultérieure, et si cette version est disponible sur le système, les styles visuels actuels sont automatiquement appliqués à tous les contrôles communs de votre application. Toutefois, les styles visuels actuels ne sont pas appliqués automatiquement aux contrôles personnalisés ou aux contrôles owner-drawn. Votre application doit inclure du code qui vérifie si les styles visuels sont disponibles et, le cas échéant, utilise l’API des styles visuels pour appliquer les styles visuels actuellement sélectionnés à vos contrôles personnalisés et owner-drawn.

Pour vérifier si les styles visuels sont disponibles, appelez la fonction [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) . Si les styles visuels ne sont pas disponibles, utilisez le code de secours pour dessiner le contrôle.

Si les styles visuels sont disponibles, vous pouvez utiliser des fonctions de style visuel, telles que [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) , pour restituer votre contrôle. Notez que [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) vous permet de personnaliser l’apparence du texte, en conservant certaines propriétés de la police du thème tout en modifiant d’autres.

**Pour dessiner un contrôle dans le style visuel actuel**

1.  Appelez [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata), en passant le *HWND* du contrôle auquel vous souhaitez appliquer des styles visuels et une liste de classes qui décrit le type du contrôle. Les classes sont définies dans Vssym32. h. **OpenThemeData** retourne un handle htheme, mais si le gestionnaire de styles visuels est désactivé ou si le style visuel actuel ne fournit pas d’informations spécifiques pour un contrôle donné, la fonction retourne la **valeur null**. Si la valeur de retour est **null**, utilisez des fonctions de dessin de styles non visuels.
2.  Pour dessiner l’arrière-plan du contrôle, appelez [**DrawThemeBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackground) ou [**DrawThemeBackgroundEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackgroundex).
3.  Pour déterminer l’emplacement du rectangle de contenu, appelez [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect).
4.  Pour restituer le texte, utilisez [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) ou [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex), en basant les coordonnées sur le rectangle retourné par [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect). Ces fonctions peuvent restituer du texte dans la police du thème pour une partie de contrôle et un état spécifiés, ou dans la police actuellement sélectionnée dans le contexte de périphérique (DC).
5.  Lorsque votre contrôle reçoit un message [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) , appelez [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) pour libérer le handle de thème qui a été retourné lorsque vous avez appelé [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata).

L’exemple de code suivant montre une façon de dessiner un contrôle bouton dans le style visuel actuel.


```C++
HTHEME hTheme = NULL;

hTheme = OpenThemeData(hwndButton, L"Button");
// ...
DrawMyControl(hDC, hwndButton, hTheme, iState);
// ...
if (hTheme)
{
    CloseThemeData(hTheme);
}


void DrawMyControl(HDC hDC, HWND hwndButton, HTHEME hTheme, int iState)
{
    RECT rc, rcContent;
    TCHAR szButtonText[255];
    HRESULT hr;
    size_t cch;

    GetWindowRect(hwndButton, &rc);
    GetWindowText(hwndButton, szButtonText,
                  (sizeof(szButtonText) / sizeof(szButtonText[0])+1));
    hr = StringCchLength(szButtonText,
         (sizeof(szButtonText) / sizeof(szButtonText[0])), &cch);
    if (hTheme)
    {
        hr = DrawThemeBackground(hTheme, hDC, BP_PUSHBUTTON, iState, &rc, 0);
        if (SUCCEEDED(hr))
        {
            hr = GetThemeBackgroundContentRect(hTheme, hDC, BP_PUSHBUTTON, 
                    iState, &rc, &rcContent);
        }

        if (SUCCEEDED(hr))
        {
            hr = DrawThemeText(hTheme, hDC, BP_PUSHBUTTON, iState, 
                    szButtonText, cch,
                    DT_CENTER | DT_VCENTER | DT_SINGLELINE,
                    0, &rcContent);
        }

    }
    else
    {
        // Draw the control without using visual styles.
    }
}
```





L’exemple de code suivant se trouve dans le gestionnaire de messages de [**\_ peinture WM**](/windows/desktop/gdi/wm-paint) pour un contrôle de bouton sous-classé. Le texte du contrôle est dessiné dans la police des styles visuels, mais la couleur est définie par l’application en fonction de l’état du contrôle.


```C++
// textColor is a COLORREF whose value has been set according to whether the button is "hot".
// paint is the PAINTSTRUCT whose members are filled in by BeginPaint.
HTHEME theme = OpenThemeData(hWnd, L"button");
if (theme)
{
    DTTOPTS opts = { 0 };
    opts.dwSize = sizeof(opts);
    opts.crText = textColor;
    opts.dwFlags |= DTT_TEXTCOLOR;
    WCHAR caption[255];
    size_t cch;
    GetWindowText(hWnd, caption, 255);
    StringCchLength(caption, 255, &cch);
    DrawThemeTextEx(theme, paint.hdc, BP_PUSHBUTTON, CBS_UNCHECKEDNORMAL, 
        caption, cch, DT_CENTER | DT_VCENTER | DT_SINGLELINE, 
        &paint.rcPaint, &opts);
    CloseThemeData(theme);
}
else
{
    // Draw the control without using visual styles.
}
```



Vous pouvez utiliser des parties d’autres contrôles et restituer chaque partie séparément. Par exemple, pour un contrôle de calendrier qui se compose d’une grille, vous pouvez traiter chaque carré formé par la grille comme un bouton de barre d’outils, en obtenant la poignée de thème comme suit :


```C++
OpenThemeData(hwnd, L"Toolbar");
```



Vous pouvez mélanger et faire correspondre des parties de contrôle en appelant plusieurs fois [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) pour un contrôle donné et en utilisant la poignée de thème appropriée pour dessiner différentes parties. Dans certains styles visuels, toutefois, certaines parties peuvent ne pas être compatibles avec d’autres parties.

Une autre approche du rendu des contrôles dans le style visuel actif consiste à utiliser les couleurs système. Par exemple, vous pouvez utiliser les couleurs système pour définir la couleur du texte lors de l’appel de la fonction [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) . La plupart des couleurs système sont définies lorsqu’un fichier de style visuel est appliqué.

## <a name="responding-to-theme-changes"></a>Réponse aux modifications de thème

Lorsque votre contrôle reçoit un message [**WM \_ THEMECHANGED**](/windows/desktop/winmsg/wm-themechanged) et qu’il détient un handle global vers le thème, il doit effectuer les opérations suivantes :

-   Appelez [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) pour fermer le handle de thème existant.
-   Appelez [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) pour faire passer le pointeur du thème au style visuel qui vient d’être chargé.

L’exemple suivant illustre les deux appels.


```C++
case WM_THEMECHANGED:
     CloseThemeData (g_hTheme);
     g_hTheme = OpenThemeData (hwnd, L"MyClassName");
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Activation des styles visuels](cookbook-overview.md)
</dt> <dt>

[Styles visuels](themes-overview.md)
</dt> </dl>

 

 
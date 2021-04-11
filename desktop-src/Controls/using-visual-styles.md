---
title: Utilisation de styles visuels avec des contrôles personnalisés et Owner-Drawn
description: Cette rubrique explique comment utiliser l’API des styles visuels pour appliquer des styles visuels à des contrôles personnalisés ou à des contrôles owner-drawn.
ms.assetid: 8b06f9ce-702c-48f8-8cf3-2718a09b8d77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7025bdf7c589649ac62bed7a4ea4f55c418940
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102436"
---
# <a name="using-visual-styles-with-custom-and-owner-drawn-controls"></a><span data-ttu-id="babd0-103">Utilisation de styles visuels avec des contrôles personnalisés et Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="babd0-103">Using Visual Styles with Custom and Owner-Drawn Controls</span></span>

<span data-ttu-id="babd0-104">Cette rubrique explique comment utiliser l’API des styles visuels pour appliquer des styles visuels à des contrôles personnalisés ou à des contrôles owner-drawn.</span><span class="sxs-lookup"><span data-stu-id="babd0-104">This topic describes how to use the visual styles API to apply visual styles to custom controls or owner-drawn controls.</span></span>

-   [<span data-ttu-id="babd0-105">Dessiner des contrôles avec des styles visuels</span><span class="sxs-lookup"><span data-stu-id="babd0-105">Drawing Controls with Visual Styles</span></span>](#drawing-controls-with-visual-styles)
-   [<span data-ttu-id="babd0-106">Réponse aux modifications de thème</span><span class="sxs-lookup"><span data-stu-id="babd0-106">Responding to Theme Changes</span></span>](#responding-to-theme-changes)
-   [<span data-ttu-id="babd0-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="babd0-107">Related topics</span></span>](#related-topics)

## <a name="drawing-controls-with-visual-styles"></a><span data-ttu-id="babd0-108">Dessiner des contrôles avec des styles visuels</span><span class="sxs-lookup"><span data-stu-id="babd0-108">Drawing Controls with Visual Styles</span></span>

<span data-ttu-id="babd0-109">Les styles visuels sont pris en charge par ComCtrl32.dll version 6 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="babd0-109">Visual styles are supported by ComCtrl32.dll version 6 and later.</span></span> <span data-ttu-id="babd0-110">Si votre application est configurée pour utiliser ComCtrl32.dll version 6 et ultérieure, et si cette version est disponible sur le système, les styles visuels actuels sont automatiquement appliqués à tous les contrôles communs de votre application.</span><span class="sxs-lookup"><span data-stu-id="babd0-110">If your application is configured to use ComCtrl32.dll version 6 and later, and if that version is available on the system, the current visual styles are automatically applied to all common controls in your application.</span></span> <span data-ttu-id="babd0-111">Toutefois, les styles visuels actuels ne sont pas appliqués automatiquement aux contrôles personnalisés ou aux contrôles owner-drawn.</span><span class="sxs-lookup"><span data-stu-id="babd0-111">However, the current visual styles are not automatically applied to custom controls or owner-drawn controls.</span></span> <span data-ttu-id="babd0-112">Votre application doit inclure du code qui vérifie si les styles visuels sont disponibles et, le cas échéant, utilise l’API des styles visuels pour appliquer les styles visuels actuellement sélectionnés à vos contrôles personnalisés et owner-drawn.</span><span class="sxs-lookup"><span data-stu-id="babd0-112">Your application must include code that checks whether visual styles are available and, if so, uses the visual styles API to apply the currently selected visual styles to your custom and owner-drawn controls.</span></span>

<span data-ttu-id="babd0-113">Pour vérifier si les styles visuels sont disponibles, appelez la fonction [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) .</span><span class="sxs-lookup"><span data-stu-id="babd0-113">To check whether visual styles are available, call the [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) function.</span></span> <span data-ttu-id="babd0-114">Si les styles visuels ne sont pas disponibles, utilisez le code de secours pour dessiner le contrôle.</span><span class="sxs-lookup"><span data-stu-id="babd0-114">If visual styles are not available, use fallback code to draw the control.</span></span>

<span data-ttu-id="babd0-115">Si les styles visuels sont disponibles, vous pouvez utiliser des fonctions de style visuel, telles que [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) , pour restituer votre contrôle.</span><span class="sxs-lookup"><span data-stu-id="babd0-115">If visual styles are available, you can use visual-styles functions such as [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) to render your control.</span></span> <span data-ttu-id="babd0-116">Notez que [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) vous permet de personnaliser l’apparence du texte, en conservant certaines propriétés de la police du thème tout en modifiant d’autres.</span><span class="sxs-lookup"><span data-stu-id="babd0-116">Note that [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) enables you to customize the appearance of text, retaining some properties of the theme font while modifying others.</span></span>

<span data-ttu-id="babd0-117">**Pour dessiner un contrôle dans le style visuel actuel**</span><span class="sxs-lookup"><span data-stu-id="babd0-117">**To draw a control in the current visual style**</span></span>

1.  <span data-ttu-id="babd0-118">Appelez [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata), en passant le *HWND* du contrôle auquel vous souhaitez appliquer des styles visuels et une liste de classes qui décrit le type du contrôle.</span><span class="sxs-lookup"><span data-stu-id="babd0-118">Call [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata), passing the *hwnd* of the control you want to apply visual styles to and a class list that describes the control's type.</span></span> <span data-ttu-id="babd0-119">Les classes sont définies dans Vssym32. h.</span><span class="sxs-lookup"><span data-stu-id="babd0-119">The classes are defined in Vssym32.h.</span></span> <span data-ttu-id="babd0-120">**OpenThemeData** retourne un handle htheme, mais si le gestionnaire de styles visuels est désactivé ou si le style visuel actuel ne fournit pas d’informations spécifiques pour un contrôle donné, la fonction retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="babd0-120">**OpenThemeData** returns an HTHEME handle, but if the visual styles manager is disabled or the current visual style does not supply specific information for a given control, the function returns **NULL**.</span></span> <span data-ttu-id="babd0-121">Si la valeur de retour est **null**, utilisez des fonctions de dessin de styles non visuels.</span><span class="sxs-lookup"><span data-stu-id="babd0-121">If the return value is **NULL**, use non-visual-styles drawing functions.</span></span>
2.  <span data-ttu-id="babd0-122">Pour dessiner l’arrière-plan du contrôle, appelez [**DrawThemeBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackground) ou [**DrawThemeBackgroundEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackgroundex).</span><span class="sxs-lookup"><span data-stu-id="babd0-122">To draw the control background, call [**DrawThemeBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackground) or [**DrawThemeBackgroundEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackgroundex).</span></span>
3.  <span data-ttu-id="babd0-123">Pour déterminer l’emplacement du rectangle de contenu, appelez [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect).</span><span class="sxs-lookup"><span data-stu-id="babd0-123">To determine the location of the content rectangle, call [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect).</span></span>
4.  <span data-ttu-id="babd0-124">Pour restituer le texte, utilisez [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) ou [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex), en basant les coordonnées sur le rectangle retourné par [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect).</span><span class="sxs-lookup"><span data-stu-id="babd0-124">To render text, use either [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) or [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex), basing the coordinates on the rectangle returned by [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect).</span></span> <span data-ttu-id="babd0-125">Ces fonctions peuvent restituer du texte dans la police du thème pour une partie de contrôle et un état spécifiés, ou dans la police actuellement sélectionnée dans le contexte de périphérique (DC).</span><span class="sxs-lookup"><span data-stu-id="babd0-125">These functions can render text either in the theme's font for a specified control part and state, or in the font currently selected into the device context (DC).</span></span>
5.  <span data-ttu-id="babd0-126">Lorsque votre contrôle reçoit un message [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) , appelez [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) pour libérer le handle de thème qui a été retourné lorsque vous avez appelé [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata).</span><span class="sxs-lookup"><span data-stu-id="babd0-126">When your control receives a [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message, call [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) to release the theme handle that was returned when you called [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata).</span></span>

<span data-ttu-id="babd0-127">L’exemple de code suivant montre une façon de dessiner un contrôle bouton dans le style visuel actuel.</span><span class="sxs-lookup"><span data-stu-id="babd0-127">The following example code demonstrates one way to draw a button control in the current visual style.</span></span>


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





<span data-ttu-id="babd0-128">L’exemple de code suivant se trouve dans le gestionnaire de messages de [**\_ peinture WM**](/windows/desktop/gdi/wm-paint) pour un contrôle de bouton sous-classé.</span><span class="sxs-lookup"><span data-stu-id="babd0-128">The following example code is in the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message handler for a subclassed button control.</span></span> <span data-ttu-id="babd0-129">Le texte du contrôle est dessiné dans la police des styles visuels, mais la couleur est définie par l’application en fonction de l’état du contrôle.</span><span class="sxs-lookup"><span data-stu-id="babd0-129">The text for the control is drawn in the visual styles font, but the color is application-defined depending on the state of the control.</span></span>


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



<span data-ttu-id="babd0-130">Vous pouvez utiliser des parties d’autres contrôles et restituer chaque partie séparément.</span><span class="sxs-lookup"><span data-stu-id="babd0-130">You can use parts from other controls and render each part separately.</span></span> <span data-ttu-id="babd0-131">Par exemple, pour un contrôle de calendrier qui se compose d’une grille, vous pouvez traiter chaque carré formé par la grille comme un bouton de barre d’outils, en obtenant la poignée de thème comme suit :</span><span class="sxs-lookup"><span data-stu-id="babd0-131">For example, for a calendar control that consists of a grid, you can treat each square formed by the grid as a toolbar button, by obtaining the theme handle as follows:</span></span>


```C++
OpenThemeData(hwnd, L"Toolbar");
```



<span data-ttu-id="babd0-132">Vous pouvez mélanger et faire correspondre des parties de contrôle en appelant plusieurs fois [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) pour un contrôle donné et en utilisant la poignée de thème appropriée pour dessiner différentes parties.</span><span class="sxs-lookup"><span data-stu-id="babd0-132">You can mix and match control parts by calling [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) multiple times for a given control and using the appropriate theme handle to draw different parts.</span></span> <span data-ttu-id="babd0-133">Dans certains styles visuels, toutefois, certaines parties peuvent ne pas être compatibles avec d’autres parties.</span><span class="sxs-lookup"><span data-stu-id="babd0-133">In some visual styles, however, certain parts might not be compatible with other parts.</span></span>

<span data-ttu-id="babd0-134">Une autre approche du rendu des contrôles dans le style visuel actif consiste à utiliser les couleurs système.</span><span class="sxs-lookup"><span data-stu-id="babd0-134">Another approach to rendering controls in the active visual style is to use the system colors.</span></span> <span data-ttu-id="babd0-135">Par exemple, vous pouvez utiliser les couleurs système pour définir la couleur du texte lors de l’appel de la fonction [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) .</span><span class="sxs-lookup"><span data-stu-id="babd0-135">For example, you can use system colors to set the text color when calling the [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) function.</span></span> <span data-ttu-id="babd0-136">La plupart des couleurs système sont définies lorsqu’un fichier de style visuel est appliqué.</span><span class="sxs-lookup"><span data-stu-id="babd0-136">Most system colors are set when a visual style file is applied.</span></span>

## <a name="responding-to-theme-changes"></a><span data-ttu-id="babd0-137">Réponse aux modifications de thème</span><span class="sxs-lookup"><span data-stu-id="babd0-137">Responding to Theme Changes</span></span>

<span data-ttu-id="babd0-138">Lorsque votre contrôle reçoit un message [**WM \_ THEMECHANGED**](/windows/desktop/winmsg/wm-themechanged) et qu’il détient un handle global vers le thème, il doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="babd0-138">When your control receives a [**WM\_THEMECHANGED**](/windows/desktop/winmsg/wm-themechanged) message and is holding a global handle to the theme, it should do the following:</span></span>

-   <span data-ttu-id="babd0-139">Appelez [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) pour fermer le handle de thème existant.</span><span class="sxs-lookup"><span data-stu-id="babd0-139">Call [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) to close the existing theme handle.</span></span>
-   <span data-ttu-id="babd0-140">Appelez [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) pour faire passer le pointeur du thème au style visuel qui vient d’être chargé.</span><span class="sxs-lookup"><span data-stu-id="babd0-140">Call [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) to get the theme handle to the newly loaded visual style.</span></span>

<span data-ttu-id="babd0-141">L’exemple suivant illustre les deux appels.</span><span class="sxs-lookup"><span data-stu-id="babd0-141">The following example illustrates the two calls.</span></span>


```C++
case WM_THEMECHANGED:
     CloseThemeData (g_hTheme);
     g_hTheme = OpenThemeData (hwnd, L"MyClassName");
```



## <a name="related-topics"></a><span data-ttu-id="babd0-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="babd0-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="babd0-143">Activation des styles visuels</span><span class="sxs-lookup"><span data-stu-id="babd0-143">Enabling Visual Styles</span></span>](cookbook-overview.md)
</dt> <dt>

[<span data-ttu-id="babd0-144">Styles visuels</span><span class="sxs-lookup"><span data-stu-id="babd0-144">Visual Styles</span></span>](themes-overview.md)
</dt> </dl>

 

 
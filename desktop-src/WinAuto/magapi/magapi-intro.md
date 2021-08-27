---
title: Vue d’ensemble de l’API zoom
description: Cette rubrique décrit l’API d’agrandissement et explique comment l’utiliser dans une application.
ms.assetid: 8dcecb73-db73-4043-b922-0b92f299eb1d
keywords:
- Agrandissement
- applications d’agrandissement d’écran
- Agrandissement
- traitement des images personnalisées
- Magnification.dll
- création de contrôles de loupe
- agrandissement sélectif
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb908623d6d6419925801119369f4f660110e680dd2499a1d61caa4c0c05de4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052590"
---
# <a name="magnification-api-overview"></a>Vue d’ensemble de l’API zoom

L’API d’agrandissement permet aux fournisseurs de technologies d’assistance de développer des applications d’agrandissement d’écran qui s’exécutent sur Microsoft Windows. Cette rubrique décrit l’API d’agrandissement et explique comment l’utiliser dans une application. Il contient les sections suivantes :

- [Prise en main](#getting-started)
- [Concepts de base](#basic-concepts)
  - [Types de loupes](#types-of-magnifiers)
  - [Facteur d’agrandissement](#magnification-factor)
  - [Effets de couleur](#color-effects)
  - [Rectangle source](#source-rectangle)
  - [Liste de filtres](#filter-list)
  - [Transformation d’entrée](#input-transform)
  - [Curseur système](#system-cursor)
- [Initialisation de la bibliothèque Runtime de la loupe](#initializing-the-magnifier-run-time-library)
- [Utilisation de la loupe Full-Screen](#using-the-full-screen-magnifier)
- [Utilisation du contrôle magnifier](#using-the-magnifier-control)
  - [Création du contrôle magnifier](#creating-the-magnifier-control)
  - [Initialisation du contrôle](#initializing-the-control)
  - [Définition du rectangle source](#setting-the-source-rectangle)
  - [Application d’effets de couleur](#applying-color-effects)
  - [Agrandissement sélectif](#selective-magnification)
- [Rubriques connexes](#related-topics)

## <a name="getting-started"></a>Mise en route

la version d’origine de l’API d’agrandissement est prise en charge sur les systèmes d’exploitation Windows Vista et versions ultérieures. sur Windows 8 et versions ultérieures, l’API prend en charge des fonctionnalités supplémentaires, notamment l’agrandissement plein écran et la définition de la visibilité du curseur système agrandi.

La prise en charge de l’API d’agrandissement est fournie par Magnification.dll. Pour compiler votre application, incluez grossissement. h et un lien vers grossissement. lib.

> [!Note]  
> L’API d’agrandissement n’est pas prise en charge sous WOW64 ; autrement dit, une application de loupe 32 bits ne s’exécute pas correctement sur le Windows 64 bits.

## <a name="basic-concepts"></a>Concepts de base

Cette section décrit les concepts fondamentaux sur lesquels l’API d’agrandissement est basée. Il contient les éléments suivants :

- [Types de loupes](#types-of-magnifiers)
- [Facteur d’agrandissement](#magnification-factor)
- [Effets de couleur](#color-effects)
- [Rectangle source](#source-rectangle)
- [Liste de filtres](#filter-list)
- [Transformation d’entrée](#input-transform)
- [Curseur système](#system-cursor)

### <a name="types-of-magnifiers"></a>Types de loupes

L’API prend en charge deux types d’agrandisseurs : la *loupe plein écran* et le *contrôle magnifier*. La loupe plein écran agrandit le contenu de l’écran tout entier, tandis que le contrôle magnifier agrandit le contenu d’une zone particulière de l’écran et affiche le contenu dans une fenêtre. Pour les deux loupes, les images et le texte sont agrandis, et tous deux vous permettent de contrôler la quantité d’agrandissement. Vous pouvez également appliquer des effets de couleur au contenu de l’écran agrandi, ce qui vous permet de voir plus facilement les personnes qui ont des défauts de couleurs ou des couleurs qui ont un contraste plus ou moins élevé.

> [!Important]  
> l’api de contrôle magnifier est disponible sur Windows Vista et les systèmes d’exploitation ultérieurs, tandis que l’api magnifier plein écran est disponible uniquement sur les systèmes d’exploitation Windows 8 et ultérieurs.

### <a name="magnification-factor"></a>Facteur d’agrandissement

La loupe plein écran et le contrôle magnifier appliquent une transformation d’échelle pour agrandir le contenu de l’écran. La quantité de grossissement appliquée par la transformation d’échelle est appelée *facteur d’agrandissement*. Elle est exprimée sous la forme d’une valeur à virgule flottante où 1,0 correspond à aucun grossissement, tandis que les valeurs supérieures produisent une quantité d’agrandissement correspondante. Par exemple, la valeur 1,5 rend le contenu de l’écran de 50% plus grand. Un facteur d’agrandissement inférieur à 1,0 n’est pas valide.

### <a name="color-effects"></a>Effets de couleur

Les effets de couleur sont obtenus en appliquant une matrice de transformation de couleur 5 par 5 aux couleurs du contenu de l’écran agrandi. La matrice détermine les intensités des composants rouge, bleu, vert et alpha du contenu. pour plus d’informations, consultez [utilisation d’une matrice de couleurs pour transformer une couleur unique](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) dans la documentation Windows GDI+.

### <a name="source-rectangle"></a>Rectangle source

La loupe plein écran applique la transformation de mise à l’échelle et la transformation de couleur à l’écran entier. En revanche, le contrôle magnifier copie une zone de l’écran, appelée *rectangle source*, vers une image bitmap hors écran. Ensuite, le contrôle applique la transformation d’échelle et la transformation de couleur, le cas échéant, à la bitmap hors écran. Enfin, le contrôle affiche le bitmap mis à l’échelle et transformé en couleurs dans la fenêtre de contrôle de la loupe.

### <a name="filter-list"></a>Liste de filtres

Par défaut, le contrôle magnifier agrandit toutes les fenêtres du rectangle source spécifié. Toutefois, en fournissant une *liste de filtres* de handles de fenêtre, vous pouvez contrôler les fenêtres qui sont incluses dans le contenu agrandi et celles qui ne le sont pas. Pour plus d’informations, consultez [grossissement sélectif](#selective-magnification).

La loupe plein écran ne prend pas en charge une liste de filtres ; elle agrandit toujours toutes les fenêtres à l’écran.

### <a name="input-transform"></a>Transformation d’entrée

Normalement, le contenu de l’écran agrandi est « invisible » au stylet ou à l’entrée tactile de l’utilisateur. Par exemple, si l’utilisateur appuie sur l’image agrandie d’un contrôle, le système ne passe pas nécessairement l’entrée au contrôle. Au lieu de cela, le système passe l’entrée à n’importe quel élément (le cas échéant) sur les coordonnées d’écran taraudé sur le Bureau non agrandi. La fonction [**MagSetInputTransform**](/windows/win32/api/Magnification/nf-magnification-magsetinputtransform) vous permet de spécifier une *transformation d’entrée* qui mappe l’espace de coordonnées du contenu de l’écran agrandi à l’espace de coordonnées d’écran réel (non agrandi). Cela permet au système de passer une entrée de stylet ou de toucher entrée dans le contenu d’écran agrandi, à l’élément d’interface utilisateur approprié à l’écran.

> [!Note]  
> Le processus appelant doit disposer de privilèges UIAccess pour définir la transformation d’entrée. Pour plus d’informations, consultez Considérations sur la [sécurité d’UI Automation](../uiauto-securityoverview.md) et [/MANIFESTUAC (incorpore les informations de contrôle de compte d’utilisateur dans le manifeste)](/cpp/build/reference/manifestuac-embeds-uac-information-in-manifest).

### <a name="system-cursor"></a>Curseur système

La fonction [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) vous permet d’afficher ou de masquer le curseur système. Si vous affichez le curseur système lorsque la loupe plein écran est active, le curseur système est toujours agrandi avec le reste du contenu de l’écran. Si vous masquez le curseur système lorsque la loupe plein écran est active, le curseur système n’est pas visible du tout.

Avec le contrôle Magnifier, la fonction [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) affiche ou masque le curseur système non agrandi, mais n’a aucun effet sur le curseur système agrandi. La visibilité du curseur système agrandi varie selon que le contrôle magnifier a le style [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) . S’il a ce style, le contrôle magnifier affiche le curseur système agrandi, ainsi que le contenu de l’écran agrandi, chaque fois que le curseur système entre dans le rectangle source.

## <a name="initializing-the-magnifier-run-time-library"></a>Initialisation de la bibliothèque Runtime de la loupe

Avant de pouvoir appeler d’autres fonctions de l’API loupe, vous devez créer et initialiser les objets d’exécution de la loupe en appelant la fonction [**MagInitialize**](/windows/win32/api/Magnification/nf-magnification-maginitialize) . De même, une fois que vous avez fini d’utiliser l’API Magnifier, appelez la fonction [**MagUninitialize**](/windows/win32/api/Magnification/nf-magnification-maguninitialize) pour détruire les objets d’exécution de la loupe et libérer les ressources système associées.

## <a name="using-the-full-screen-magnifier"></a>Utilisation de la loupe Full-Screen

Pour utiliser la loupe plein écran, appelez la fonction [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) . Le paramètre *magLevel* spécifie le facteur d’agrandissement. Les paramètres *xoffset* et *yOffset* spécifient la façon dont le contenu de l’écran agrandi est positionné par rapport à l’écran.

Lorsque le contenu de l’écran est agrandi, il devient plus grand que l’écran lui-même. Une partie du contenu s’étend au-delà des bords de l’écran et devient invisible pour l’utilisateur. Les paramètres *xoffset* et *yOffset* de la fonction [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) déterminent la partie du contenu de l’écran agrandie qui s’affiche à l’écran. Ensemble, les paramètres spécifient les coordonnées d’un point dans le contenu de l’écran qui n’est pas agrandi. Lorsque le contenu est agrandi, il est positionné avec le point spécifié dans l’angle supérieur gauche de l’écran.

L’exemple suivant définit le facteur d’agrandissement de la loupe plein écran et place le centre du contenu de l’écran agrandi au centre de l’écran.

```C++
BOOL SetZoom(float magnificationFactor)
{
    // A magnification factor less than 1.0 is not valid.
    if (magnificationFactor < 1.0)
    {
        return FALSE;
    }

    // Calculate offsets such that the center of the magnified screen content 
    // is at the center of the screen. The offsets are relative to the 
    // unmagnified screen content.
    int xDlg = (int)((float)GetSystemMetrics(
            SM_CXSCREEN) * (1.0 - (1.0 / magnificationFactor)) / 2.0);
    int yDlg = (int)((float)GetSystemMetrics(
            SM_CYSCREEN) * (1.0 - (1.0 / magnificationFactor)) / 2.0);

    return MagSetFullscreenTransform(magnificationFactor, xDlg, yDlg);
}
```

Utilisez la fonction [**MagSetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreencoloreffect) pour appliquer des effets de couleur au contenu plein écran en définissant une matrice de transformation des couleurs définie par l’application. Par exemple, l’exemple suivant définit une matrice de transformation des couleurs qui convertit les couleurs en nuances de gris.

```C++
// Initialize color transformation matrices used to apply grayscale and to 
// restore the original screen color.
MAGCOLOREFFECT g_MagEffectGrayscale = {0.3f,  0.3f,  0.3f,  0.0f,  0.0f,
                                       0.6f,  0.6f,  0.6f,  0.0f,  0.0f,
                                       0.1f,  0.1f,  0.1f,  0.0f,  0.0f,
                                       0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
                                       0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

MAGCOLOREFFECT g_MagEffectIdentity = {1.0f,  0.0f,  0.0f,  0.0f,  0.0f,
                                      0.0f,  1.0f,  0.0f,  0.0f,  0.0f,
                                      0.0f,  0.0f,  1.0f,  0.0f,  0.0f,
                                      0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
                                      0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

BOOL SetColorGrayscale(__in BOOL fGrayscaleOn)
{
    // Apply the color matrix required to either apply grayscale to the screen 
    // colors or to show the regular colors.
    PMAGCOLOREFFECT pEffect = 
                (fGrayscaleOn ? &amp;g_MagEffectGrayscale : &amp;g_MagEffectIdentity);

    return MagSetFullscreenColorEffect(pEffect);
}
```

Vous pouvez récupérer le facteur d’agrandissement et les valeurs de décalage actuels en appelant la fonction [**MagGetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreentransform) . Vous pouvez récupérer la matrice de transformation de couleur actuelle en appelant la fonction [**MagGetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreencoloreffect) .

## <a name="using-the-magnifier-control"></a>Utilisation du contrôle magnifier

Le contrôle magnifier agrandit le contenu d’une zone particulière de l’écran et affiche le contenu dans une fenêtre. Cette section décrit comment utiliser le contrôle magnifier. Il contient les éléments suivants :

- [Création du contrôle magnifier](#creating-the-magnifier-control)
- [Initialisation du contrôle](#initializing-the-control)
- [Définition du rectangle source](#setting-the-source-rectangle)
- [Application d’effets de couleur](#applying-color-effects)
- [Agrandissement sélectif](#selective-magnification)

### <a name="creating-the-magnifier-control"></a>Création du contrôle magnifier

Le contrôle magnifier doit être hébergé dans une fenêtre créée avec le style étendu [**WS_EX_LAYERED**](../../winmsg/extended-window-styles.md) . Après avoir créé la fenêtre hôte, appelez [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) pour définir l’opacité de la fenêtre hôte. La fenêtre hôte est généralement définie sur l’opacité totale pour empêcher le contenu de l’écran sous-jacent de s’affiche. L’exemple suivant montre comment définir l’opacité complète de la fenêtre hôte :

```C++
SetLayeredWindowAttributes(hwndHost, NULL, 255, LWA_ALPHA);
```

Si vous appliquez le style de [**WS_EX_TRANSPARENT**](../../winmsg/extended-window-styles.md) à la fenêtre hôte, les clics de souris sont passés à l’objet situé derrière la fenêtre hôte à l’emplacement du curseur de la souris. Sachez que, étant donné que la fenêtre hôte ne traite pas les clics de souris, l’utilisateur ne peut pas déplacer ou redimensionner la fenêtre d’agrandissement à l’aide de la souris.

La classe de fenêtre de la fenêtre de contrôle loupe doit être **WC_MAGNIFIER**. Si vous appliquez le style de [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) , le contrôle loupe comprend le curseur système dans le contenu de l’écran agrandi et le curseur est agrandi avec le contenu de l’écran.

Après avoir créé le contrôle Magnifier, conservez le handle de fenêtre pour pouvoir le passer à d’autres fonctions.

L’exemple suivant montre comment créer le contrôle magnifier.

```C++
// Description: 
//   Registers the host window class, creates the host window, sets the layered
//   window attributes, and creates the magnifier control. 
// Parameters:
//   hInstance - Instance handle of the application.
// Variables:
//   HostWndProc - Window procedure of the host window.
//   WindowClassName - Name of the window class.
//   WindowTitle - Title of the host window.
// Constants and global variables:
//   hwndHost - Handle of the host window.
//   hwndMag - Handle of the magnifier window.
//   LENS_WIDTH - Width of the magnifier window.
//   LENS_HEIGHT - Height of the magnifier window.
// 
BOOL CreateMagnifier(HINSTANCE hInstance)
{
   // Register the host window class.
    WNDCLASSEX wcex = {};
    wcex.cbSize = sizeof(WNDCLASSEX); 
    wcex.style          = 0;
    wcex.lpfnWndProc    = HostWndProc;
    wcex.hInstance      = hInstance;
    wcex.hCursor        = LoadCursor(NULL, IDC_ARROW);
    wcex.hbrBackground  = (HBRUSH)(1 + COLOR_BTNFACE);
    wcex.lpszClassName  = WindowClassName;
    
    if (RegisterClassEx(&amp;wcex) == 0)
        return FALSE;

    // Create the host window. 
    hwndHost = CreateWindowEx(WS_EX_TOPMOST | WS_EX_LAYERED | WS_EX_TRANSPARENT, 
        WindowClassName, WindowTitle, 
        WS_CLIPCHILDREN,
        0, 0, 0, 0,
        NULL, NULL, hInstance, NULL);
    if (!hwndHost)
    {
        return FALSE;
    }

    // Make the window opaque.
    SetLayeredWindowAttributes(hwndHost, 0, 255, LWA_ALPHA);

    // Create a magnifier control that fills the client area.
    hwndMag = CreateWindow(WC_MAGNIFIER, TEXT("MagnifierWindow"), 
        WS_CHILD | MS_SHOWMAGNIFIEDCURSOR | WS_VISIBLE,
        0, 0, 
        LENS_WIDTH, 
        LENS_HEIGHT, 
        hwndHost, NULL, hInstance, NULL );
    if (!hwndMag)
    {
        return FALSE;
    }

    return TRUE;
}
```

### <a name="initializing-the-control"></a>Initialisation du contrôle

Après avoir créé le contrôle Magnifier, vous devez appeler la fonction [**MagSetWindowTransform**](/windows/win32/api/Magnification/nf-magnification-magsetwindowtransform) pour spécifier le facteur d’agrandissement. Il suffit de spécifier une matrice de

(*n*, 0,0, 0,0)

(0,0, *n*, 0,0)

(0,0, 0,0, 1,0)

où *n* est le facteur d’agrandissement.

L’exemple suivant montre comment définir le facteur d’agrandissement du contrôle magnifier.

```C++
// Description:
//   Sets the magnification factor for a magnifier control.
// Parameters:
//   hwndMag - Handle of the magnifier control.
//   magFactor - New magnification factor.
//
BOOL SetMagnificationFactor(HWND hwndMag, float magFactor)
{
    MAGTRANSFORM matrix;
    memset(&amp;matrix, 0, sizeof(matrix));
    matrix.v[0][0] = magFactor;
    matrix.v[1][1] = magFactor;
    matrix.v[2][2] = 1.0f;

    return MagSetWindowTransform(hwndMag, &amp;matrix);  
}
```

### <a name="setting-the-source-rectangle"></a>Définition du rectangle source

Lorsque l’utilisateur déplace le curseur de la souris autour de l’écran, votre application appelle la fonction [**MagSetWindowSource**](/windows/win32/api/Magnification/nf-magnification-magsetwindowsource) pour spécifier la partie de l’écran sous-jacent qui doit être agrandie.

L’exemple de fonction suivant calcule la position et les dimensions du rectangle source (en fonction de la position de la souris et des dimensions de la fenêtre de la loupe divisée par le facteur d’agrandissement) et définit le rectangle source en conséquence. La fonction Centre également la zone cliente de la fenêtre hôte à la position de la souris. Cette fonction est appelée à des intervalles pour mettre à jour la fenêtre d’agrandissement.

```C++
// Description: 
//   Called by a timer to update the contents of the magnifier window and to set
//   the position of the host window. 
// Constants and global variables:
//   hwndHost - Handle of the host window.
//   hwndMag - Handle of the magnifier window.
//   LENS_WIDTH - Width of the magnifier window.
//   LENS_HEIGHT - Height of the magnifier window.
//   MAGFACTOR - The magnification factor.
//
void CALLBACK UpdateMagWindow(HWND /*hwnd*/, UINT /*uMsg*/, 
        UINT_PTR /*idEvent*/, DWORD /*dwTime*/)
{
    // Get the mouse coordinates.
    POINT mousePoint;
    GetCursorPos(&amp;mousePoint);

    // Calculate a source rectangle that is centered at the mouse coordinates. 
    // Size the rectangle so that it fits into the magnifier window (the lens).
    RECT sourceRect;
    int borderWidth = GetSystemMetrics(SM_CXFIXEDFRAME);
    int captionHeight = GetSystemMetrics(SM_CYCAPTION);
    sourceRect.left = (mousePoint.x - (int)((LENS_WIDTH / 2) / MAGFACTOR)) + 
             (int)(borderWidth / MAGFACTOR);
    sourceRect.top = (mousePoint.y - (int)((LENS_HEIGHT / 2) / MAGFACTOR)) + 
             (int)(captionHeight / MAGFACTOR) + (int)(borderWidth / MAGFACTOR); 
    sourceRect.right = LENS_WIDTH;
    sourceRect.bottom = LENS_HEIGHT;

    // Pass the source rectangle to the magnifier control.
    MagSetWindowSource(hwndMag, sourceRect);

    // Move the host window so that the origin of the client area lines up
    // with the origin of the magnified source rectangle.
    MoveWindow(hwndHost, 
        (mousePoint.x - LENS_WIDTH / 2), 
        (mousePoint.y - LENS_HEIGHT / 2), 
        LENS_WIDTH, 
        LENS_HEIGHT,
        FALSE);

    // Force the magnifier control to redraw itself.
    InvalidateRect(hwndMag, NULL, TRUE);

    return;
}
```

### <a name="applying-color-effects"></a>Application d’effets de couleur

Un contrôle magnifier qui a le style [**MS_INVERTCOLORS**](magapi-magnifier-styles.md) applique une matrice de transformation de couleur intégrée qui inverse les couleurs du contenu de l’écran agrandi. L’illustration suivante montre le contenu de l’écran dans un contrôle magnifier qui a le style **MS_INVERTCOLORS** .

![capture d’écran du contenu agrandi avec les couleurs inversées](images/color-inversion.png)

La fonction [**MagSetColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetcoloreffect) vous permet d’appliquer d’autres effets de couleur en définissant une matrice de transformation des couleurs définie par l’application. Par exemple, la fonction suivante définit une matrice de transformation des couleurs qui convertit les couleurs en nuances de gris.


```C++
// Description:
//   Converts the colors displayed in the magnifier window to grayscale, or
//   returns the colors to normal.
// Parameters:
//   hwndMag - Handle of the magnifier control.
//   fInvert - TRUE to convert to grayscale, or FALSE for normal colors.
//
BOOL ConvertToGrayscale(HWND hwndMag, BOOL fConvert)
{
    // Convert the screen colors in the magnifier window.
    if (fConvert)
    {
        MAGCOLOREFFECT magEffectGrayscale = 
            {{ // MagEffectGrayscale
                {  0.3f,  0.3f,  0.3f,  0.0f,  0.0f },
                {  0.6f,  0.6f,  0.6f,  0.0f,  0.0f },
                {  0.1f,  0.1f,  0.1f,  0.0f,  0.0f },
                {  0.0f,  0.0f,  0.0f,  1.0f,  0.0f },
                {  0.0f,  0.0f,  0.0f,  0.0f,  1.0f } 
            }};

        return MagSetColorEffect(hwndMag, &amp;magEffectGrayscale);
    }

    // Return the colors to normal.
    else
    {
        return MagSetColorEffect(hwndMag, NULL);
    }
}
```

pour plus d’informations sur le fonctionnement des transformations de couleurs, consultez [utilisation d’une matrice de couleurs pour transformer une couleur unique](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) dans la documentation de GDI+.

### <a name="selective-magnification"></a>Agrandissement sélectif

Par défaut, l’agrandissement est appliqué à toutes les fenêtres autres que la fenêtre d’agrandissement elle-même. Pour spécifier les fenêtres à agrandir, appelez la fonction [**MagSetWindowFilterList**](/windows/win32/api/Magnification/nf-magnification-magsetwindowfilterlist) . Cette méthode prend une liste de fenêtres à agrandir ou une liste de fenêtres à exclure de l’agrandissement.

## <a name="related-topics"></a>Rubriques connexes

[API de grossissement](entry-magapi-sdk.md)
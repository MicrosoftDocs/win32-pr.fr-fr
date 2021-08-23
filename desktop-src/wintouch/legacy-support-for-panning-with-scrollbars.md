---
title: Prise en charge héritée du panorama avec les barres de défilement
description: cette section décrit la prise en charge du panoramique à l’aide des barres de défilement dans les applications basées sur Windows.
ms.assetid: a8906b48-b804-4f3a-bb9b-dc94b632e2f7
keywords:
- Windows Toucher, prise en charge héritée
- panoramique avec barres de défilement
- Windows Toucher, panoramique avec barres de défilement
- Windows Toucher, barres de défilement
- barres de défilement, panoramique
- barres de défilement, prise en charge héritée
- Windows Toucher, mouvements
- mouvements, panoramique avec barres de défilement
- Windows Toucher, raccourcis
- raccourcis, panoramique avec barres de défilement
- raccourcis, désactivation
- Windows Messages tactiles, roulette de la souris
- messages de roulette de la souris
- Windows Toucher, personnaliser la panoramisation
- panoramique, barres de défilement
- panoramique, prise en charge héritée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97190d637cae5cc6936ecd78dca31e1e6c0f9ef1037b292b6080f973fc4e8701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086305"
---
# <a name="legacy-support-for-panning-with-scroll-bars"></a>Prise en charge héritée du panorama avec les barres de défilement

cette section décrit la prise en charge du panoramique à l’aide des barres de défilement dans les applications basées sur Windows.

dans Windows 7, les gestes panoramiques génèrent \_ \* des messages de défilement WM pour activer la prise en charge héritée pour le panoramique. Étant donné que vos applications peuvent ne pas prendre en charge tous les \_ \* messages de défilement WM, le panoramique peut ne pas fonctionner correctement. Cette rubrique décrit les étapes que vous devez suivre pour vous assurer que l’expérience de panoramique héritée dans les applications fonctionne comme prévu par les utilisateurs.

## <a name="overview"></a>Vue d’ensemble

Les sections suivantes expliquent comment activer l’expérience de panoramique héritée :

-   Créer une application avec des barres de défilement.
-   Désactiver les raccourcis.
-   Personnaliser l’expérience de panoramique.

## <a name="create-an-application-with-scroll-bars"></a>Créer une application avec des barres de défilement

démarrez un nouveau projet Win32 à l’aide de l’assistant Microsoft Visual Studio. assurez-vous que le type d’application est défini sur l’application Windows. Vous n’avez pas besoin d’activer la prise en charge des Active Template Library (ATL). L’illustration suivante montre à quoi ressemblera votre projet une fois que vous l’avez démarré.

![capture d’écran montrant une fenêtre sans barres de défilement](images/gpd-1.png)

Activez ensuite les barres de défilement sur l’image. Modifiez le code de création de fenêtre dans **InitInstance** afin que l’appel de fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) crée une fenêtre avec des barres de défilement. Le code suivant montre comment procéder.


```C++
   hWnd = CreateWindow(
      szWindowClass, 
      szTitle, 
      WS_OVERLAPPEDWINDOW | WS_VSCROLL,  // style
      200,                               // x
      200,                               // y
      550,                               // width
      300,                               // height
      NULL,
      NULL,
      hInstance,
      NULL
    );  
```



Une fois que vous avez modifié le code de création de la fenêtre, votre application dispose d’une barre de défilement. L’illustration suivante montre comment l’application peut examiner ce point.

![capture d’écran montrant une fenêtre avec une barre de défilement verticale mais sans texte](images/gpd-2.png)

Après avoir modifié le code de création de la fenêtre, ajoutez un objet de barre de défilement à votre application et du texte à faire défiler. Placez le code suivant en haut de la méthode **WndProc** .


```C++
    TEXTMETRIC tm;     
    SCROLLINFO si; 
     
    // These variables are required to display text. 
    static int xClient;     // width of client area 
    static int yClient;     // height of client area 
    static int xClientMax;  // maximum width of client area 
     
    static int xChar;       // horizontal scrolling unit 
    static int yChar;       // vertical scrolling unit 
    static int xUpper;      // average width of uppercase letters 
     
    static int xPos;        // current horizontal scrolling position 
    static int yPos;        // current vertical scrolling position 
     
    int i;                  // loop counter 
    int x, y;               // horizontal and vertical coordinates
     
    int FirstLine;          // first line in the invalidated area 
    int LastLine;           // last line in the invalidated area 
    HRESULT hr;
    int abcLength = 0;  // length of an abc[] item

    int lines = 0;

    // Create an array of lines to display. 
    static const int LINES=28;
    static LPCWSTR abc[] = { 
       L"anteater",  L"bear",      L"cougar", 
       L"dingo",     L"elephant",  L"falcon", 
       L"gazelle",   L"hyena",     L"iguana", 
       L"jackal",    L"kangaroo",  L"llama", 
       L"moose",     L"newt",      L"octopus", 
       L"penguin",   L"quail",     L"rat", 
       L"squid",     L"tortoise",  L"urus", 
       L"vole",      L"walrus",    L"xylophone", 
       L"yak",       L"zebra",
       L"This line contains words, but no character. Go figure.",
       L""
     };        
```



Ensuite, implémentez la logique d’application pour configurer les calculs de texte pour les métriques de texte. Le code suivant doit remplacer le cas **\_ Create WM** existant dans la fonction **WndProc** .


```C++
    case WM_CREATE : 
        // Get the handle to the client area's device context. 
        hdc = GetDC (hWnd); 
 
        // Extract font dimensions from the text metrics. 
        GetTextMetrics (hdc, &tm); 
        xChar = tm.tmAveCharWidth; 
        xUpper = (tm.tmPitchAndFamily & 1 ? 3 : 2) * xChar/2; 
        yChar = tm.tmHeight + tm.tmExternalLeading; 
 
        // Free the device context. 
        ReleaseDC (hWnd, hdc); 
 
        // Set an arbitrary maximum width for client area. 
        // (xClientMax is the sum of the widths of 48 average 
        // lowercase letters and 12 uppercase letters.) 
        xClientMax = 48 * xChar + 12 * xUpper; 
 
        return 0;
```



Ensuite, implémentez la logique d’application pour recalculer le bloc de texte lorsque la fenêtre est redimensionnée. Le code suivant doit être placé dans le commutateur de message dans **WndProc**.


```C++
    case WM_SIZE: 
 
        // Retrieve the dimensions of the client area. 
        yClient = HIWORD (lParam); 
        xClient = LOWORD (lParam); 
 
        // Set the vertical scrolling range and page size
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = LINES - 1; 
        si.nPage  = yClient / yChar; 
        SetScrollInfo(hWnd, SB_VERT, &si, TRUE); 
 
        // Set the horizontal scrolling range and page size. 
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = 2 + xClientMax / xChar; 
        si.nPage  = xClient / xChar; 
        SetScrollInfo(hWnd, SB_HORZ, &si, TRUE);            
        return 0;
```



Ensuite, implémentez la logique d’application pour les messages de défilement vertical. Le code suivant doit être placé dans le commutateur de message dans **WndProc**.


```C++
        case WM_VSCROLL:
         // Get all the vertical scroll bar information
         si.cbSize = sizeof (si);
         si.fMask  = SIF_ALL;
         GetScrollInfo (hWnd, SB_VERT, &si);
         // Save the position for comparison later on
         yPos = si.nPos;
         switch (LOWORD (wParam))
         {
         // user clicked the HOME keyboard key
         case SB_TOP:
             si.nPos = si.nMin;
             break;
              
         // user clicked the END keyboard key
         case SB_BOTTOM:
             si.nPos = si.nMax;
             break;
              
         // user clicked the top arrow
         case SB_LINEUP:
             si.nPos -= 1;
             break;
              
         // user clicked the bottom arrow
         case SB_LINEDOWN:
             si.nPos += 1;
             break;
              
         // user clicked the scroll bar shaft above the scroll box
         case SB_PAGEUP:
             si.nPos -= si.nPage;
             break;
              
         // user clicked the scroll bar shaft below the scroll box
         case SB_PAGEDOWN:
             si.nPos += si.nPage;
             break;
              
         // user dragged the scroll box
         case SB_THUMBTRACK:
             si.nPos = si.nTrackPos;
             break;

         // user positioned the scroll box
         // This message is the one used by Windows Touch
         case SB_THUMBPOSITION:
             si.nPos = HIWORD(wParam);
             break;
                            
         default:
              break; 
         }
         // Set the position and then retrieve it.  Due to adjustments
         //   by Windows it may not be the same as the value set.
         si.fMask = SIF_POS;
         SetScrollInfo (hWnd, SB_VERT, &si, TRUE);
         GetScrollInfo (hWnd, SB_VERT, &si);
         // If the position has changed, scroll window and update it
         if (si.nPos != yPos)
         {                    
          ScrollWindow(hWnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
          UpdateWindow (hWnd);
         }
         break;
```



Ensuite, mettez à jour le code pour redessiner la fenêtre. Le code suivant doit remplacer le cas **de \_ peinture WM** par défaut dans **WndProc**.


```C++
    case WM_PAINT:
         // Prepare the window for painting
         hdc = BeginPaint (hWnd, &ps);
         // Get vertical scroll bar position
         si.cbSize = sizeof (si);
         si.fMask  = SIF_POS;
         GetScrollInfo (hWnd, SB_VERT, &si);
         yPos = si.nPos;
         // Get horizontal scroll bar position
         GetScrollInfo (hWnd, SB_HORZ, &si);
         xPos = si.nPos;
         // Find painting limits
         FirstLine = max (0, yPos + ps.rcPaint.top / yChar);
         LastLine = min (LINES - 1, yPos + ps.rcPaint.bottom / yChar);
         
         
         
         for (i = FirstLine; i <= LastLine; i++)         
         {
              x = xChar * (1 - xPos);
              y = yChar * (i - yPos);
              
              // Note that "55" in the following depends on the 
              // maximum size of an abc[] item.
              //
              abcLength = wcslen(abc[i]);
              hr = S_OK;
              if ((FAILED(hr)))
              {
                 MessageBox(hWnd, L"err", L"err", NULL);
              }else{
                  TextOut(hdc, x, y, abc[i], abcLength);
              }
              
         }
         // Indicate that painting is finished
         EndPaint (hWnd, &ps);
         return 0;
```



Désormais, lorsque vous générez et exécutez votre application, elle doit contenir le texte réutilisable et une barre de défilement verticale. L’illustration suivante montre l’apparence de votre application.

![capture d’écran montrant une fenêtre avec une barre de défilement et un texte verticaux](images/gpd-3.png)

## <a name="disable-flicks"></a>Désactiver les raccourcis

Pour améliorer l’expérience de panorama dans votre application, vous devez désactiver les raccourcis. Pour ce faire, définissez les propriétés de la fenêtre sur la valeur *HWND* lorsqu’elle est initialisée. Les valeurs utilisées pour les raccourcis sont stockées dans l’en-tête tpcshrd. h, qui doit également être inclus. Le code suivant doit être placé dans vos directives include et dans la fonction **InitInstance** après avoir créé votre *HWND*.

> [!Note]  
> Cela est utile pour les applications qui requièrent un retour immédiat sur une pression tactile ou un événement de stylet au lieu de tester un seuil d’heure ou de distance.

 


```C++
#include <tpcshrd.h>
```




```C++
[...]
BOOL InitInstance(HINSTANCE hInstance, int nCmdShow){
[...]
  
```




```C++
   const DWORD_PTR dwHwndTabletProperty = 
    TABLET_DISABLE_PRESSANDHOLD | // disables press and hold (right-click) gesture
    TABLET_DISABLE_PENTAPFEEDBACK | // disables UI feedback on pen up (waves)
    TABLET_DISABLE_PENBARRELFEEDBACK | // disables UI feedback on pen button down (circle)
    TABLET_DISABLE_FLICKS; // disables pen flicks (back, forward, drag down, drag up)
   
   SetProp(hWnd, MICROSOFT_TABLETPENSERVICE_PROPERTY, reinterpret_cast<HANDLE>(dwHwndTabletProperty));
```



## <a name="customize-the-panning-experience"></a>Personnaliser l’expérience de panoramique

par défaut, vous souhaiterez peut-être utiliser une expérience de panoramique différente de celle offerte par Windows 7. Pour améliorer l’expérience de panoramique, vous devez ajouter le gestionnaire pour le message de [**\_ mouvement WM**](wm-gesture.md) . Pour plus d’informations, consultez [amélioration de l’expérience de panoramique Single-Finger](improving-the-single-finger-panning-experience.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Gestes tactiles](guide-multi-touch-gestures.md)
</dt> </dl>

 

 
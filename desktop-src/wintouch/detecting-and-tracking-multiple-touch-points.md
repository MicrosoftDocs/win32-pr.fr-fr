---
title: Détection et suivi de plusieurs points tactiles
description: Détection et suivi de plusieurs points tactiles
ms.assetid: 7a5c7595-f341-4e11-805f-ed0b9c63cbff
keywords:
- Tactile Windows, points tactiles multiples
- détection de plusieurs points tactiles
- suivi de plusieurs points tactiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13b9eaf665b850eea8925bd531ffd1e9ec3fcf40
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463475"
---
# <a name="detecting-and-tracking-multiple-touch-points"></a>Détection et suivi de plusieurs points tactiles

Les étapes suivantes expliquent comment suivre plusieurs points tactiles à l’aide de Windows Touch.

1.  Créez une application et activez la fonction tactile Windows.
2.  Ajoutez un gestionnaire pour [**WM \_ Touch**](wm-touchdown.md) et les points de suivi.
3.  Dessinez les points.

Une fois que votre application est en cours d’exécution, elle affiche des cercles sous chaque pression tactile. La capture d’écran suivante montre comment votre application peut s’afficher en cours d’exécution.

![capture d’écran montrant une application qui restitue des points tactiles en tant que cercles verts et jaunes](images/multitouchpoints.png)

## <a name="create-an-application-and-enable-windows-touch"></a>Créer une application et activer Windows Touch

Démarrez avec une application Microsoft Win32 à l’aide de l’Assistant Microsoft Visual Studio. Une fois l’Assistant terminé, ajoutez la prise en charge des messages tactiles Windows en définissant la version de Windows dans targetver. h et en incluant Windows. h et windowsx. h dans votre application. Le code suivant montre comment définir la version de Windows dans targetver. h.


```C++
#ifndef WINVER                  // Specifies that the minimum required platform is Windows 7.
#define WINVER 0x0601           // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT            // Specifies that the minimum required platform is Windows 7.
#define _WIN32_WINNT 0x0601     // Change this to the appropriate value to target other versions of Windows.
#endif     

#ifndef _WIN32_WINDOWS          // Specifies that the minimum required platform is Windows 98.
#define _WIN32_WINDOWS 0x0410 // Change this to the appropriate value to target Windows Me or later.
#endif

#ifndef _WIN32_IE                       // Specifies that the minimum required platform is Internet Explorer 7.0.
#define _WIN32_IE 0x0700        // Change this to the appropriate value to target other versions of IE.
#endif
```



Le code suivant illustre l’ajout de vos directives include. En outre, vous pouvez créer des variables globales qui seront utilisées ultérieurement.


```C++
#include <windows.h>    // included for Windows Touch
#include <windowsx.h>   // included for point conversion

#define MAXPOINTS 10

// You will use this array to track touch points
int points[MAXPOINTS][2];

// You will use this array to switch the color / track ids
int idLookup[MAXPOINTS];


// You can make the touch points larger
// by changing this radius value
static int radius      = 50;

// There should be at least as many colors
// as there can be touch points so that you
// can have different colors for each point
COLORREF colors[] = { RGB(153,255,51), 
                      RGB(153,0,0), 
                      RGB(0,153,0), 
                      RGB(255,255,0), 
                      RGB(255,51,204), 
                      RGB(0,0,0),
                      RGB(0,153,0), 
                      RGB(153, 255, 255), 
                      RGB(153,153,255), 
                      RGB(0,51,153)
                    };

```



## <a name="add-handler-for-wm_touch-and-track-points"></a>Ajouter un gestionnaire pour WM \_ touch et les points de suivi

Tout d’abord, déclarez des variables qui sont utilisées par le gestionnaire [**WM \_ Touch**](wm-touchdown.md) dans [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)).


```C++
int wmId, wmEvent, i, x, y;

UINT cInputs;
PTOUCHINPUT pInputs;
POINT ptInput;   
```



À présent, initialisez les variables utilisées pour stocker les points tactiles et inscrivez la fenêtre pour l’entrée tactile à partir de la méthode **InitInstance** .


```C++
BOOL InitInstance(HINSTANCE hInstance, int nCmdShow)
{
   HWND hWnd;

   hInst = hInstance; // Store instance handle in our global variable

   hWnd = CreateWindow(szWindowClass, szTitle, WS_OVERLAPPEDWINDOW,
      CW_USEDEFAULT, 0, CW_USEDEFAULT, 0, NULL, NULL, hInstance, NULL);

   if (!hWnd) {
      return FALSE;
   }

   // register the window for touch instead of gestures
   RegisterTouchWindow(hWnd, 0);  

   // the following code initializes the points
   for (int i=0; i< MAXPOINTS; i++){
     points[i][0] = -1;
     points[i][1] = -1;
     idLookup[i]  = -1;
   }  

   ShowWindow(hWnd, nCmdShow);
   UpdateWindow(hWnd);

   return TRUE;
}
```



Ensuite, gérez le message [**WM \_ Touch**](wm-touchdown.md) à partir de la méthode [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Le code suivant illustre une implémentation du gestionnaire pour **WM \_ Touch**.


```C++
case WM_TOUCH:        
  cInputs = LOWORD(wParam);
  pInputs = new TOUCHINPUT[cInputs];
  if (pInputs){
    if (GetTouchInputInfo((HTOUCHINPUT)lParam, cInputs, pInputs, sizeof(TOUCHINPUT))){
      for (int i=0; i < static_cast<INT>(cInputs); i++){
        TOUCHINPUT ti = pInputs[i];
        index = GetContactIndex(ti.dwID);
        if (ti.dwID != 0 && index < MAXPOINTS){                            
          // Do something with your touch input handle
          ptInput.x = TOUCH_COORD_TO_PIXEL(ti.x);
          ptInput.y = TOUCH_COORD_TO_PIXEL(ti.y);
          ScreenToClient(hWnd, &ptInput);
          
          if (ti.dwFlags & TOUCHEVENTF_UP){                      
            points[index][0] = -1;
            points[index][1] = -1;                
          }else{
            points[index][0] = ptInput.x;
            points[index][1] = ptInput.y;                
          }
        }
      }
    }
    // If you handled the message and don't want anything else done with it, you can close it
    CloseTouchInputHandle((HTOUCHINPUT)lParam);
    delete [] pInputs;
  }else{
    // Handle the error here 
  }  
```



> [!Note]  
> Pour pouvoir utiliser la fonction [**ScreenToClient**](/windows/desktop/api/winuser/nf-winuser-screentoclient) , vous devez disposer d’une prise en charge des résolutions élevées dans votre application. Pour plus d’informations sur la prise en charge de la haute résolution, consultez la section [haute résolution]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) de MSDN.

 

Désormais, lorsqu’un utilisateur touche l’écran, les positions qu’il touche seront stockées dans le tableau points. Le membre **dwId** de la structure [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) stocke un identificateur qui dépend du matériel.

Pour résoudre le problème lié au fait que le membre dwID dépend du matériel, le gestionnaire de cas [**\_ tactile WM**](wm-touchdown.md) utilise une fonction, **GetContactIndex**, qui mappe le membre **dwId** de la structure [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) à un point dessiné à l’écran. Le code suivant illustre une implémentation de cette fonction.


```C++
// This function is used to return an index given an ID
int GetContactIndex(int dwID){
  for (int i=0; i < MAXPOINTS; i++){
    if (idLookup[i] == -1){
      idLookup[i] = dwID;
      return i;
    }else{
      if (idLookup[i] == dwID){
        return i;
      }
    }
  }
  // Out of contacts
  return -1;
}
```



## <a name="draw-the-points"></a>Dessiner les points

Déclarez les variables suivantes pour la routine de dessin.


```C++
    // For double buffering
    static HDC memDC       = 0;
    static HBITMAP hMemBmp = 0;
    HBITMAP hOldBmp        = 0;
   
    // For drawing / fills
    PAINTSTRUCT ps;
    HDC hdc;
    
    // For tracking dwId to points
    int index;
```



Le contexte d’affichage de la mémoire *memDC* est utilisé pour stocker un contexte graphique temporaire qui est échangé avec le contexte d’affichage rendu, *HDC*, afin d’éliminer le scintillement. Implémentez la routine de dessin, qui prend les points que vous avez stockés et dessine un cercle aux points. Le code suivant montre comment vous pouvez implémenter le gestionnaire de [**\_ peinture WM**](/windows/desktop/gdi/wm-paint) .


```C++
  case WM_PAINT:
    hdc = BeginPaint(hWnd, &ps);    
    RECT client;
    GetClientRect(hWnd, &client);        
  
    // start double buffering
    if (!memDC){
      memDC = CreateCompatibleDC(hdc);
    }
    hMemBmp = CreateCompatibleBitmap(hdc, client.right, client.bottom);
    hOldBmp = (HBITMAP)SelectObject(memDC, hMemBmp);          
  
    FillRect(memDC, &client, CreateSolidBrush(RGB(255,255,255)));
     
    //Draw Touched Points                
    for (i=0; i < MAXPOINTS; i++){        
      SelectObject( memDC, CreateSolidBrush(colors[i]));           
      x = points[i][0];
      y = points[i][1];
      if  (x >0 && y>0){              
        Ellipse(memDC, x - radius, y - radius, x+ radius, y + radius);
      }
    }
  
    BitBlt(hdc, 0,0, client.right, client.bottom, memDC, 0,0, SRCCOPY);      

    EndPaint(hWnd, &ps);
    break;
```



Quand vous exécutez votre application, elle doit maintenant ressembler à l’illustration au début de cette section.

Pour vous amuser, vous pouvez dessiner des lignes supplémentaires autour des points tactiles. La capture d’écran suivante montre comment l’application peut se présenter avec quelques lignes supplémentaires dessinées autour des cercles.

![capture d’écran montrant une application qui affiche des points tactiles sous forme de cercles avec des lignes à travers les centres et en croisant les bords des points tactiles](images/multitouchpointsfun.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Entrée tactile Windows](guide-multi-touch-input.md)
</dt> </dl>

 

 
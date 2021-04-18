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
# <a name="detecting-and-tracking-multiple-touch-points"></a><span data-ttu-id="bc38f-106">Détection et suivi de plusieurs points tactiles</span><span class="sxs-lookup"><span data-stu-id="bc38f-106">Detecting and Tracking Multiple Touch Points</span></span>

<span data-ttu-id="bc38f-107">Les étapes suivantes expliquent comment suivre plusieurs points tactiles à l’aide de Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="bc38f-107">The following steps explain how to track multiple touch points using Windows Touch.</span></span>

1.  <span data-ttu-id="bc38f-108">Créez une application et activez la fonction tactile Windows.</span><span class="sxs-lookup"><span data-stu-id="bc38f-108">Create an application and enable Windows Touch.</span></span>
2.  <span data-ttu-id="bc38f-109">Ajoutez un gestionnaire pour [**WM \_ Touch**](wm-touchdown.md) et les points de suivi.</span><span class="sxs-lookup"><span data-stu-id="bc38f-109">Add a handler for [**WM\_TOUCH**](wm-touchdown.md) and track points.</span></span>
3.  <span data-ttu-id="bc38f-110">Dessinez les points.</span><span class="sxs-lookup"><span data-stu-id="bc38f-110">Draw the points.</span></span>

<span data-ttu-id="bc38f-111">Une fois que votre application est en cours d’exécution, elle affiche des cercles sous chaque pression tactile.</span><span class="sxs-lookup"><span data-stu-id="bc38f-111">After you have your application running, it will render circles under each touch.</span></span> <span data-ttu-id="bc38f-112">La capture d’écran suivante montre comment votre application peut s’afficher en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="bc38f-112">The following screen shot shows how your application might look while running.</span></span>

![capture d’écran montrant une application qui restitue des points tactiles en tant que cercles verts et jaunes](images/multitouchpoints.png)

## <a name="create-an-application-and-enable-windows-touch"></a><span data-ttu-id="bc38f-114">Créer une application et activer Windows Touch</span><span class="sxs-lookup"><span data-stu-id="bc38f-114">Create an Application and Enable Windows Touch</span></span>

<span data-ttu-id="bc38f-115">Démarrez avec une application Microsoft Win32 à l’aide de l’Assistant Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="bc38f-115">Start with a Microsoft Win32 application using the Microsoft Visual Studio wizard.</span></span> <span data-ttu-id="bc38f-116">Une fois l’Assistant terminé, ajoutez la prise en charge des messages tactiles Windows en définissant la version de Windows dans targetver. h et en incluant Windows. h et windowsx. h dans votre application.</span><span class="sxs-lookup"><span data-stu-id="bc38f-116">After you have completed the wizard, add support for Windows Touch messages by setting the Windows version in targetver.h and including windows.h and windowsx.h in your application.</span></span> <span data-ttu-id="bc38f-117">Le code suivant montre comment définir la version de Windows dans targetver. h.</span><span class="sxs-lookup"><span data-stu-id="bc38f-117">The following code shows how to set the Windows version in targetver.h.</span></span>


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



<span data-ttu-id="bc38f-118">Le code suivant illustre l’ajout de vos directives include.</span><span class="sxs-lookup"><span data-stu-id="bc38f-118">The following code shows how your include directives should be added.</span></span> <span data-ttu-id="bc38f-119">En outre, vous pouvez créer des variables globales qui seront utilisées ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="bc38f-119">Also, you can create some global variables that will be used later.</span></span>


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



## <a name="add-handler-for-wm_touch-and-track-points"></a><span data-ttu-id="bc38f-120">Ajouter un gestionnaire pour WM \_ touch et les points de suivi</span><span class="sxs-lookup"><span data-stu-id="bc38f-120">Add Handler for WM\_TOUCH and Track Points</span></span>

<span data-ttu-id="bc38f-121">Tout d’abord, déclarez des variables qui sont utilisées par le gestionnaire [**WM \_ Touch**](wm-touchdown.md) dans [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bc38f-121">First, declare some variables that are used by the [**WM\_TOUCH**](wm-touchdown.md) handler in [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)).</span></span>


```C++
int wmId, wmEvent, i, x, y;

UINT cInputs;
PTOUCHINPUT pInputs;
POINT ptInput;   
```



<span data-ttu-id="bc38f-122">À présent, initialisez les variables utilisées pour stocker les points tactiles et inscrivez la fenêtre pour l’entrée tactile à partir de la méthode **InitInstance** .</span><span class="sxs-lookup"><span data-stu-id="bc38f-122">Now, initialize the variables used for storing touch points and register the window for touch input from the **InitInstance** method.</span></span>


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



<span data-ttu-id="bc38f-123">Ensuite, gérez le message [**WM \_ Touch**](wm-touchdown.md) à partir de la méthode [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="bc38f-123">Next, handle the [**WM\_TOUCH**](wm-touchdown.md) message from the [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) method.</span></span> <span data-ttu-id="bc38f-124">Le code suivant illustre une implémentation du gestionnaire pour **WM \_ Touch**.</span><span class="sxs-lookup"><span data-stu-id="bc38f-124">The following code shows an implementation of the handler for **WM\_TOUCH**.</span></span>


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
> <span data-ttu-id="bc38f-125">Pour pouvoir utiliser la fonction [**ScreenToClient**](/windows/desktop/api/winuser/nf-winuser-screentoclient) , vous devez disposer d’une prise en charge des résolutions élevées dans votre application.</span><span class="sxs-lookup"><span data-stu-id="bc38f-125">In order to use the [**ScreenToClient**](/windows/desktop/api/winuser/nf-winuser-screentoclient) function, you must have high DPI support in your application.</span></span> <span data-ttu-id="bc38f-126">Pour plus d’informations sur la prise en charge de la haute résolution, consultez la section [haute résolution]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) de MSDN.</span><span class="sxs-lookup"><span data-stu-id="bc38f-126">For more information on supporting high DPI, see the [High DPI]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) section of MSDN.</span></span>

 

<span data-ttu-id="bc38f-127">Désormais, lorsqu’un utilisateur touche l’écran, les positions qu’il touche seront stockées dans le tableau points.</span><span class="sxs-lookup"><span data-stu-id="bc38f-127">Now when a user touches the screen, the positions that he or she is touching will be stored in the points array.</span></span> <span data-ttu-id="bc38f-128">Le membre **dwId** de la structure [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) stocke un identificateur qui dépend du matériel.</span><span class="sxs-lookup"><span data-stu-id="bc38f-128">The **dwID** member of the [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) structure stores an identifier that will be hardware dependent.</span></span>

<span data-ttu-id="bc38f-129">Pour résoudre le problème lié au fait que le membre dwID dépend du matériel, le gestionnaire de cas [**\_ tactile WM**](wm-touchdown.md) utilise une fonction, **GetContactIndex**, qui mappe le membre **dwId** de la structure [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) à un point dessiné à l’écran.</span><span class="sxs-lookup"><span data-stu-id="bc38f-129">To address the issue of the dwID member being dependent on hardware, the [**WM\_TOUCH**](wm-touchdown.md) case handler uses a function, **GetContactIndex**, that maps the **dwID** member of the [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) structure to a point that is drawn on the screen.</span></span> <span data-ttu-id="bc38f-130">Le code suivant illustre une implémentation de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="bc38f-130">The following code shows an implementation of this function.</span></span>


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



## <a name="draw-the-points"></a><span data-ttu-id="bc38f-131">Dessiner les points</span><span class="sxs-lookup"><span data-stu-id="bc38f-131">Draw the Points</span></span>

<span data-ttu-id="bc38f-132">Déclarez les variables suivantes pour la routine de dessin.</span><span class="sxs-lookup"><span data-stu-id="bc38f-132">Declare the following variables for the drawing routine.</span></span>


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



<span data-ttu-id="bc38f-133">Le contexte d’affichage de la mémoire *memDC* est utilisé pour stocker un contexte graphique temporaire qui est échangé avec le contexte d’affichage rendu, *HDC*, afin d’éliminer le scintillement.</span><span class="sxs-lookup"><span data-stu-id="bc38f-133">The memory display context *memDC* is used for storing a temporary graphics context that is swapped with the rendered display context, *hdc*, to eliminate flickering.</span></span> <span data-ttu-id="bc38f-134">Implémentez la routine de dessin, qui prend les points que vous avez stockés et dessine un cercle aux points.</span><span class="sxs-lookup"><span data-stu-id="bc38f-134">Implement the drawing routine, which takes the points you have stored and draws a circle at the points.</span></span> <span data-ttu-id="bc38f-135">Le code suivant montre comment vous pouvez implémenter le gestionnaire de [**\_ peinture WM**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="bc38f-135">The following code shows how you could implement the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) handler.</span></span>


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



<span data-ttu-id="bc38f-136">Quand vous exécutez votre application, elle doit maintenant ressembler à l’illustration au début de cette section.</span><span class="sxs-lookup"><span data-stu-id="bc38f-136">When you run your application, it now should look something like the illustration at the beginning of this section.</span></span>

<span data-ttu-id="bc38f-137">Pour vous amuser, vous pouvez dessiner des lignes supplémentaires autour des points tactiles.</span><span class="sxs-lookup"><span data-stu-id="bc38f-137">For fun, you can draw some extra lines around the touch points.</span></span> <span data-ttu-id="bc38f-138">La capture d’écran suivante montre comment l’application peut se présenter avec quelques lignes supplémentaires dessinées autour des cercles.</span><span class="sxs-lookup"><span data-stu-id="bc38f-138">The following screen shot shows how the application could look with a few extra lines drawn around the circles.</span></span>

![capture d’écran montrant une application qui affiche des points tactiles sous forme de cercles avec des lignes à travers les centres et en croisant les bords des points tactiles](images/multitouchpointsfun.png)

## <a name="related-topics"></a><span data-ttu-id="bc38f-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bc38f-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc38f-141">Entrée tactile Windows</span><span class="sxs-lookup"><span data-stu-id="bc38f-141">Windows Touch Input</span></span>](guide-multi-touch-input.md)
</dt> </dl>

 

 
---
title: Prise en charge héritée du panorama avec les barres de défilement
description: Cette section décrit la prise en charge du panoramique à l’aide des barres de défilement dans les applications Windows.
ms.assetid: a8906b48-b804-4f3a-bb9b-dc94b632e2f7
keywords:
- Tactile Windows, support hérité
- panoramique avec barres de défilement
- Tactile Windows, panoramique avec barres de défilement
- Tactile Windows, barres de défilement
- barres de défilement, panoramique
- barres de défilement, prise en charge héritée
- Tactile Windows, gestes
- mouvements, panoramique avec barres de défilement
- Tactile Windows, raccourcis
- raccourcis, panoramique avec barres de défilement
- raccourcis, désactivation
- Touches tactiles Windows, messages de roulette de la souris
- messages de roulette de la souris
- Tactile Windows, personnalisation de la panoramisation
- panoramique, barres de défilement
- panoramique, prise en charge héritée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57f6b9dd47821205a6aa5b6f07e5053e31597358
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104561822"
---
# <a name="legacy-support-for-panning-with-scroll-bars"></a><span data-ttu-id="d6b55-119">Prise en charge héritée du panorama avec les barres de défilement</span><span class="sxs-lookup"><span data-stu-id="d6b55-119">Legacy Support for Panning with Scroll Bars</span></span>

<span data-ttu-id="d6b55-120">Cette section décrit la prise en charge du panoramique à l’aide des barres de défilement dans les applications Windows.</span><span class="sxs-lookup"><span data-stu-id="d6b55-120">This section describes support for panning using scroll bars in Windows-based applications.</span></span>

<span data-ttu-id="d6b55-121">Dans Windows 7, les gestes panoramiques génèrent \_ \* des messages de défilement WM pour activer la prise en charge héritée pour le panoramique.</span><span class="sxs-lookup"><span data-stu-id="d6b55-121">In Windows 7, panning gestures generate WM\_\*SCROLL messages to enable legacy support for panning.</span></span> <span data-ttu-id="d6b55-122">Étant donné que vos applications peuvent ne pas prendre en charge tous les \_ \* messages de défilement WM, le panoramique peut ne pas fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="d6b55-122">Because your applications may not support all of the WM\_\*SCROLL messages, panning may not work correctly.</span></span> <span data-ttu-id="d6b55-123">Cette rubrique décrit les étapes que vous devez suivre pour vous assurer que l’expérience de panoramique héritée dans les applications fonctionne comme prévu par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d6b55-123">This topic describes the steps you must take to ensure that the legacy panning experience in applications functions as users expect.</span></span>

## <a name="overview"></a><span data-ttu-id="d6b55-124">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="d6b55-124">Overview</span></span>

<span data-ttu-id="d6b55-125">Les sections suivantes expliquent comment activer l’expérience de panoramique héritée :</span><span class="sxs-lookup"><span data-stu-id="d6b55-125">The following sections explain how to enable the legacy panning experience:</span></span>

-   <span data-ttu-id="d6b55-126">Créer une application avec des barres de défilement.</span><span class="sxs-lookup"><span data-stu-id="d6b55-126">Create an application with scroll bars.</span></span>
-   <span data-ttu-id="d6b55-127">Désactiver les raccourcis.</span><span class="sxs-lookup"><span data-stu-id="d6b55-127">Disable flicks.</span></span>
-   <span data-ttu-id="d6b55-128">Personnaliser l’expérience de panoramique.</span><span class="sxs-lookup"><span data-stu-id="d6b55-128">Customize the panning experience.</span></span>

## <a name="create-an-application-with-scroll-bars"></a><span data-ttu-id="d6b55-129">Créer une application avec des barres de défilement</span><span class="sxs-lookup"><span data-stu-id="d6b55-129">Create an Application with Scroll Bars</span></span>

<span data-ttu-id="d6b55-130">Démarrez un nouveau projet Win32 à l’aide de l’Assistant Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d6b55-130">Start a new Win32 project using the Microsoft Visual Studio wizard.</span></span> <span data-ttu-id="d6b55-131">Assurez-vous que le type d’application est défini sur l’application Windows.</span><span class="sxs-lookup"><span data-stu-id="d6b55-131">Make sure the application type is set to the Windows application.</span></span> <span data-ttu-id="d6b55-132">Vous n’avez pas besoin d’activer la prise en charge des Active Template Library (ATL).</span><span class="sxs-lookup"><span data-stu-id="d6b55-132">You don't need to enable support for the Active Template Library (ATL).</span></span> <span data-ttu-id="d6b55-133">L’illustration suivante montre à quoi ressemblera votre projet une fois que vous l’avez démarré.</span><span class="sxs-lookup"><span data-stu-id="d6b55-133">The following image shows what your project will look like after you have started it.</span></span>

![capture d’écran montrant une fenêtre sans barres de défilement](images/gpd-1.png)

<span data-ttu-id="d6b55-135">Activez ensuite les barres de défilement sur l’image.</span><span class="sxs-lookup"><span data-stu-id="d6b55-135">Next, enable scroll bars on the image.</span></span> <span data-ttu-id="d6b55-136">Modifiez le code de création de fenêtre dans **InitInstance** afin que l’appel de fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) crée une fenêtre avec des barres de défilement.</span><span class="sxs-lookup"><span data-stu-id="d6b55-136">Change the window creation code in **InitInstance** so that the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) function call creates a window with scroll bars.</span></span> <span data-ttu-id="d6b55-137">Le code suivant montre comment procéder.</span><span class="sxs-lookup"><span data-stu-id="d6b55-137">The following code shows how to do this.</span></span>


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



<span data-ttu-id="d6b55-138">Une fois que vous avez modifié le code de création de la fenêtre, votre application dispose d’une barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="d6b55-138">After you have changed the window creation code, your application will have a scroll bar.</span></span> <span data-ttu-id="d6b55-139">L’illustration suivante montre comment l’application peut examiner ce point.</span><span class="sxs-lookup"><span data-stu-id="d6b55-139">The following image shows how the application might look at this point.</span></span>

![capture d’écran montrant une fenêtre avec une barre de défilement verticale mais sans texte](images/gpd-2.png)

<span data-ttu-id="d6b55-141">Après avoir modifié le code de création de la fenêtre, ajoutez un objet de barre de défilement à votre application et du texte à faire défiler.</span><span class="sxs-lookup"><span data-stu-id="d6b55-141">After you have changed the window creation code, add a scroll bar object to your application and some text to scroll.</span></span> <span data-ttu-id="d6b55-142">Placez le code suivant en haut de la méthode **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="d6b55-142">Place the following code into the top of the **WndProc** method.</span></span>


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



<span data-ttu-id="d6b55-143">Ensuite, implémentez la logique d’application pour configurer les calculs de texte pour les métriques de texte.</span><span class="sxs-lookup"><span data-stu-id="d6b55-143">Next, implement the application logic for configuring the text calculations for text metrics.</span></span> <span data-ttu-id="d6b55-144">Le code suivant doit remplacer le cas **\_ Create WM** existant dans la fonction **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="d6b55-144">The following code should replace the existing **WM\_CREATE** case in the **WndProc** function.</span></span>


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



<span data-ttu-id="d6b55-145">Ensuite, implémentez la logique d’application pour recalculer le bloc de texte lorsque la fenêtre est redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="d6b55-145">Next, implement the application logic for recalculation of the text block when the window is resized.</span></span> <span data-ttu-id="d6b55-146">Le code suivant doit être placé dans le commutateur de message dans **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="d6b55-146">The following code should be placed into the message switch in **WndProc**.</span></span>


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



<span data-ttu-id="d6b55-147">Ensuite, implémentez la logique d’application pour les messages de défilement vertical.</span><span class="sxs-lookup"><span data-stu-id="d6b55-147">Next, implement the application logic for vertical scroll messages.</span></span> <span data-ttu-id="d6b55-148">Le code suivant doit être placé dans le commutateur de message dans **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="d6b55-148">The following code should be placed into the message switch in **WndProc**.</span></span>


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



<span data-ttu-id="d6b55-149">Ensuite, mettez à jour le code pour redessiner la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d6b55-149">Next, update the code to redraw the window.</span></span> <span data-ttu-id="d6b55-150">Le code suivant doit remplacer le cas **de \_ peinture WM** par défaut dans **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="d6b55-150">The following code should replace the default **WM\_PAINT** case in **WndProc**.</span></span>


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



<span data-ttu-id="d6b55-151">Désormais, lorsque vous générez et exécutez votre application, elle doit contenir le texte réutilisable et une barre de défilement verticale.</span><span class="sxs-lookup"><span data-stu-id="d6b55-151">Now when you build and run your application, it should have the boilerplate text and a vertical scroll bar.</span></span> <span data-ttu-id="d6b55-152">L’illustration suivante montre l’apparence de votre application.</span><span class="sxs-lookup"><span data-stu-id="d6b55-152">The following image shows how your application might look.</span></span>

![capture d’écran montrant une fenêtre avec une barre de défilement et un texte verticaux](images/gpd-3.png)

## <a name="disable-flicks"></a><span data-ttu-id="d6b55-154">Désactiver les raccourcis</span><span class="sxs-lookup"><span data-stu-id="d6b55-154">Disable Flicks</span></span>

<span data-ttu-id="d6b55-155">Pour améliorer l’expérience de panorama dans votre application, vous devez désactiver les raccourcis.</span><span class="sxs-lookup"><span data-stu-id="d6b55-155">To improve the panning experience in your application, you should turn off flicks.</span></span> <span data-ttu-id="d6b55-156">Pour ce faire, définissez les propriétés de la fenêtre sur la valeur *HWND* lorsqu’elle est initialisée.</span><span class="sxs-lookup"><span data-stu-id="d6b55-156">To do this, set window properties on the *hWnd* value when it is initialized.</span></span> <span data-ttu-id="d6b55-157">Les valeurs utilisées pour les raccourcis sont stockées dans l’en-tête tpcshrd. h, qui doit également être inclus.</span><span class="sxs-lookup"><span data-stu-id="d6b55-157">The values used for flicks are stored in the tpcshrd.h header, which also must be included.</span></span> <span data-ttu-id="d6b55-158">Le code suivant doit être placé dans vos directives include et dans la fonction **InitInstance** après avoir créé votre *HWND*.</span><span class="sxs-lookup"><span data-stu-id="d6b55-158">The following code should be placed in your include directives and in the **InitInstance** function after you have created your *hWnd*.</span></span>

> [!Note]  
> <span data-ttu-id="d6b55-159">Cela est utile pour les applications qui requièrent un retour immédiat sur une pression tactile ou un événement de stylet au lieu de tester un seuil d’heure ou de distance.</span><span class="sxs-lookup"><span data-stu-id="d6b55-159">This is useful for applications that require immediate feedback on a touch or pen down event instead of testing for a time or distance threshold.</span></span>

 


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



## <a name="customize-the-panning-experience"></a><span data-ttu-id="d6b55-160">Personnaliser l’expérience de panoramique</span><span class="sxs-lookup"><span data-stu-id="d6b55-160">Customize the Panning Experience</span></span>

<span data-ttu-id="d6b55-161">Vous souhaiterez peut-être disposer d’une expérience de panoramique différente de celle proposée par défaut par Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d6b55-161">You might want a different panning experience than Windows 7 offers by default.</span></span> <span data-ttu-id="d6b55-162">Pour améliorer l’expérience de panoramique, vous devez ajouter le gestionnaire pour le message de [**\_ mouvement WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="d6b55-162">To improve the panning experience, you must add the handler for the [**WM\_GESTURE**](wm-gesture.md) message.</span></span> <span data-ttu-id="d6b55-163">Pour plus d’informations, consultez [amélioration de l’expérience de panoramique Single-Finger](improving-the-single-finger-panning-experience.md).</span><span class="sxs-lookup"><span data-stu-id="d6b55-163">For more information, see [Improving the Single-Finger Panning Experience](improving-the-single-finger-panning-experience.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6b55-164">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d6b55-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6b55-165">Gestes tactiles Windows</span><span class="sxs-lookup"><span data-stu-id="d6b55-165">Windows Touch Gestures</span></span>](guide-multi-touch-gestures.md)
</dt> </dl>

 

 
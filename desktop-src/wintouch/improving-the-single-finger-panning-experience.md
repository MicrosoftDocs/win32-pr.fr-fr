---
title: Amélioration de l’expérience de panoramique Single-Finger
description: Si vous générez une application qui cible Windows Touch, elle fournit automatiquement la prise en charge de la panoramisation de base. Toutefois, vous pouvez utiliser le \_ message de mouvement WM pour fournir une prise en charge améliorée pour le panoramique à un seul doigt.
ms.assetid: eb01a6df-9969-44d1-a657-4f83fb0b67cb
keywords:
- Tactile Windows, panoramique à un seul doigt
- Tactile Windows, panoramique
- Tactile Windows, barres de défilement
- Tactile Windows, raccourcis
- Tactile Windows, messages panoramiques de geste
- Tactile Windows, commentaires sur les limites
- panoramique à un seul doigt
- panoramique, à un seul doigt
- panoramique, commentaires sur les limites
- barres de défilement, panoramique à un seul doigt
- raccourcis, panoramique à un seul doigt
- barres de défilement, désactivation
- raccourcis, désactivation
- gestes, messages panoramiques de mouvement
- panoramique, messages panoramiques de mouvement
- Commentaires sur les limites, panoramique à un seul doigt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9081903600918485f1e3241a02c01b5438c1aae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728020"
---
# <a name="improving-the-single-finger-panning-experience"></a><span data-ttu-id="f0e3c-120">Amélioration de l’expérience de panoramique Single-Finger</span><span class="sxs-lookup"><span data-stu-id="f0e3c-120">Improving the Single-Finger Panning Experience</span></span>

<span data-ttu-id="f0e3c-121">Si vous générez une application qui cible Windows Touch, elle fournit automatiquement la prise en charge de la panoramisation de base.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-121">If you build an application that targets Windows Touch, it automatically provides basic panning support.</span></span> <span data-ttu-id="f0e3c-122">Toutefois, vous pouvez utiliser le message de [**\_ mouvement WM**](wm-gesture.md) pour fournir une prise en charge améliorée pour le panoramique à un seul doigt.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-122">However, you can use the [**WM\_GESTURE**](wm-gesture.md) message to provide enhanced support for single-finger panning.</span></span>

## <a name="overview"></a><span data-ttu-id="f0e3c-123">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="f0e3c-123">Overview</span></span>

<span data-ttu-id="f0e3c-124">Pour améliorer l’expérience de panoramique à un seul doigt, suivez ces étapes, comme expliqué dans les sections suivantes de cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="f0e3c-124">To improve the single-finger panning experience, use these steps, as explained in subsequent sections of this topic:</span></span>

-   <span data-ttu-id="f0e3c-125">Créer une application avec des barres de défilement et avec des raccourcis désactivés.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-125">Create an application with scroll bars and with flicks disabled.</span></span>
-   <span data-ttu-id="f0e3c-126">Ajoutez la prise en charge des messages de panoramique des mouvements.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-126">Add support for gesture pan messages.</span></span>
-   <span data-ttu-id="f0e3c-127">Activez Bounce.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-127">Enable bounce.</span></span>

## <a name="create-an-application-with-scroll-bars-and-with-flicks-disabled"></a><span data-ttu-id="f0e3c-128">Créer une application avec des barres de défilement et avec des raccourcis désactivés</span><span class="sxs-lookup"><span data-stu-id="f0e3c-128">Create an Application with Scroll Bars and with Flicks Disabled</span></span>

<span data-ttu-id="f0e3c-129">Avant de commencer, vous devez créer une application avec des barres de défilement.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-129">Before you begin, you must create an application with scroll bars.</span></span> <span data-ttu-id="f0e3c-130">La section [prise en charge héritée du panorama avec les barres de défilement](legacy-support-for-panning-with-scrollbars.md) explique ce processus.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-130">The section [Legacy Support for Panning with Scrollbars](legacy-support-for-panning-with-scrollbars.md) explains this process.</span></span> <span data-ttu-id="f0e3c-131">Si vous souhaitez commencer par l’exemple de contenu, accédez à cette section et créez une application avec des barres de défilement, puis désactivez les raccourcis.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-131">If you want to start with the example content, go to that section and create an application with scroll bars and then disable flicks.</span></span> <span data-ttu-id="f0e3c-132">Si vous disposez déjà d’une application avec des barres de défilement fonctionnelles, désactivez les raccourcis comme décrit dans cette section.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-132">If you already have an application with functioning scroll bars, disable flicks as described in that section.</span></span>

## <a name="add-custom-panning-support-for-gesture-pan-messages"></a><span data-ttu-id="f0e3c-133">Ajouter une prise en charge de panoramique personnalisée pour les messages panoramiques de mouvements</span><span class="sxs-lookup"><span data-stu-id="f0e3c-133">Add Custom Panning Support for Gesture Pan Messages</span></span>

<span data-ttu-id="f0e3c-134">Pour prendre en charge les messages de panoramique de geste, vous devez les gérer dans la méthode **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="f0e3c-134">To support gesture pan messages, you must handle them in the **WndProc** method.</span></span> <span data-ttu-id="f0e3c-135">Les messages de mouvement permettent de déterminer les deltas horizontaux et verticaux pour les messages panoramiques.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-135">The gesture messages are used to determine horizontal and vertical deltas for pan messages.</span></span> <span data-ttu-id="f0e3c-136">Les deltas sont utilisés pour mettre à jour l’objet de barre de défilement, qui met à jour l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-136">The deltas are used to update the scroll bar object, which updates the user interface.</span></span>

<span data-ttu-id="f0e3c-137">Tout d’abord, mettez à jour les paramètres de version de Windows dans le fichier targetver. h pour activer Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-137">First, update the Windows version settings in the targetver.h file to enable Windows Touch.</span></span> <span data-ttu-id="f0e3c-138">Le code suivant montre les différents paramètres de la version de Windows qui doivent les remplacer dans targetver. h.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-138">The following code shows the various Windows version settings that should replace those in targetver.h.</span></span>


```C++
#ifndef WINVER                  // Specifies that the minimum required platform is Windows Vista.
#define WINVER 0x0601           // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT            // Specifies that the minimum required platform is Windows Vista.
#define _WIN32_WINNT 0x0601     // Change this to the appropriate value to target other versions of Windows.
#endif
```



<span data-ttu-id="f0e3c-139">Ensuite, ajoutez le fichier UXTheme. h à votre projet et ajoutez la bibliothèque uxtheme. lib aux dépendances supplémentaires de votre projet.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-139">Next, add the UXTheme.h file to your project and add the uxtheme.lib library to the additional dependencies of your project.</span></span>


```C++
#include <uxtheme.h>
```



<span data-ttu-id="f0e3c-140">Ensuite, ajoutez les variables suivantes en haut de la fonction **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="f0e3c-140">Next, add the following variables to the top of the **WndProc** function.</span></span> <span data-ttu-id="f0e3c-141">Ils seront utilisés dans les calculs pour le panoramique.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-141">These will be used in calculations for panning.</span></span>


```C++
// The following are used for the custom panning handler      
BOOL bResult = FALSE;

static int scale = 8;   // altering the scale value will change how fast the page scrolls
static int lastY = 0;   // used for panning calculations (initial / previous vertical position)
static int lastX = 0;   // used for panning calculations (initial / previous horizontal position)
GESTUREINFO gi;  
```



<span data-ttu-id="f0e3c-142">Ensuite, ajoutez le gestionnaire du message [**de \_ mouvement WM**](wm-gesture.md) afin que les barres de défilement soient mises à jour avec des deltas basés sur les gestes panoramiques.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-142">Next, add the handler for the [**WM\_GESTURE**](wm-gesture.md) message so that the scroll bars are updated with deltas based on panning gestures.</span></span> <span data-ttu-id="f0e3c-143">Vous bénéficiez ainsi d’un contrôle de panoramique bien plus affiné.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-143">This gives you a much finer-grained control of panning.</span></span>

<span data-ttu-id="f0e3c-144">Le code suivant obtient la structure [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) à partir du *lParam*, enregistre la dernière coordonnée y de la structure et détermine la modification de la position pour mettre à jour l’objet de barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-144">The following code gets the [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) structure from the *lParam*, saves the last y-coordinate from the structure, and determines the change in position to update the scroll bar object.</span></span> <span data-ttu-id="f0e3c-145">Le code suivant doit être placé dans votre instruction de commutateur **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="f0e3c-145">The following code should be placed in your **WndProc** switch statement.</span></span>


```C++
    case WM_GESTURE:        
        // Get all the vertial scroll bar information
        si.cbSize = sizeof (si);
        si.fMask  = SIF_ALL;
        GetScrollInfo (hWnd, SB_VERT, &si);
        yPos = si.nPos;

        ZeroMemory(&gi, sizeof(GESTUREINFO));
        gi.cbSize = sizeof(GESTUREINFO);
        bResult = GetGestureInfo((HGESTUREINFO)lParam, &gi);

        if (bResult){
            // now interpret the gesture            
            switch (gi.dwID){
                case GID_BEGIN:
                   lastY = gi.ptsLocation.y;
                   CloseGestureInfoHandle((HGESTUREINFO)lParam);
                   break;                     
                // A CUSTOM PAN HANDLER
                // COMMENT THIS CASE OUT TO ENABLE DEFAULT HANDLER BEHAVIOR
                case GID_PAN:                                                  
                    
                    si.nPos -= (gi.ptsLocation.y - lastY) / scale;

                    si.fMask = SIF_POS;
                    SetScrollInfo (hWnd, SB_VERT, &si, TRUE);
                    GetScrollInfo (hWnd, SB_VERT, &si);                                                        
                                               
                    yOverpan -= lastY - gi.ptsLocation.y;
                    lastY = gi.ptsLocation.y;
                     
                    if (gi.dwFlags & GF_BEGIN){
                        BeginPanningFeedback(hWnd);
                        yOverpan = 0;
                    } else if (gi.dwFlags & GF_END) {
                        EndPanningFeedback(hWnd, TRUE);
                        yOverpan = 0;
                    }
                           
                    if (si.nPos == si.nMin || si.nPos >= (si.nMax - si.nPage)){                    
                        // we reached the bottom / top, pan
                        UpdatePanningFeedback(hWnd, 0, yOverpan, gi.dwFlags & GF_INERTIA);
                    }
                    ScrollWindow(hWnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
                    UpdateWindow (hWnd);                    
                                        
                    return DefWindowProc(hWnd, message, lParam, wParam);
                case GID_ZOOM:
                   // Add Zoom handler 
                   return DefWindowProc(hWnd, message, lParam, wParam);
                default:
                   // You have encountered an unknown gesture
                   return DefWindowProc(hWnd, message, lParam, wParam);
             }          
        }else{
            DWORD dwErr = GetLastError();
            if (dwErr > 0){
                // something is wrong 
                // 87 indicates that you are probably using a bad
                // value for the gi.cbSize
            }
        } 
        return DefWindowProc (hWnd, message, wParam, lParam);
```



<span data-ttu-id="f0e3c-146">Désormais, quand vous effectuez le mouvement de panoramique sur votre fenêtre, vous voyez le texte défiler avec inertie.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-146">Now, when you perform the pan gesture on your window, you will see the text scroll with inertia.</span></span> <span data-ttu-id="f0e3c-147">À ce stade, vous souhaiterez peut-être modifier le texte pour qu’il comporte davantage de lignes afin que vous puissiez explorer de grandes sections de texte.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-147">At this point, you might want to change the text to have more lines so that you can explore panning large sections of text.</span></span>

## <a name="boundary-feedback-in-wndproc"></a><span data-ttu-id="f0e3c-148">Commentaires sur les limites dans WndProc</span><span class="sxs-lookup"><span data-stu-id="f0e3c-148">Boundary Feedback in WndProc</span></span>

<span data-ttu-id="f0e3c-149">Les commentaires sur les limites sont un type de retour visuel donné aux utilisateurs lorsqu’ils atteignent la fin d’une zone pannable.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-149">Boundary feedback is a type of visual feedback given to users when they reach the end of a pannable area.</span></span> <span data-ttu-id="f0e3c-150">Elle est déclenchée par l’application lorsqu’une limite est atteinte.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-150">It is triggered by the application when a boundary is reached.</span></span> <span data-ttu-id="f0e3c-151">Dans l’exemple d’implémentation précédent du message de [**\_ mouvement WM**](wm-gesture.md) , la condition `(si.nPos == si.yPos)` de fin du cas de **\_ mouvement WM** est utilisée pour vérifier que vous avez atteint la fin d’une région pannable.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-151">In the previous example implementation of the [**WM\_GESTURE**](wm-gesture.md) message, the end condition `(si.nPos == si.yPos)` from the **WM\_GESTURE** case is used to test that you have reached the end of a pannable region.</span></span> <span data-ttu-id="f0e3c-152">Les variables suivantes sont utilisées pour effectuer le suivi des valeurs et des erreurs de test.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-152">The following variables are used to track values and test errors.</span></span>


```C++
// The following are used for panning feedback (Window Bounce)
static int animCount = 0;
static DWORD dwErr   = 0;

static BOOL isOverpan  = FALSE;
static long xOverpan   = 0;
static long yOverpan   = 0;
```



<span data-ttu-id="f0e3c-153">Le cas de mouvement de panoramique est mis à jour pour déclencher un feedback de limite.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-153">The pan gesture case is updated to trigger boundary feedback.</span></span> <span data-ttu-id="f0e3c-154">Le code suivant illustre le cas **de \_ panoramique du GID** à partir du gestionnaire de messages de [**\_ mouvements WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="f0e3c-154">The following code illustrates the **GID\_PAN** case from the [**WM\_GESTURE**](wm-gesture.md) message handler.</span></span>


```C++
                case GID_PAN:                                                  
                    
                    si.nPos -= (gi.ptsLocation.y - lastY) / scale;

                    si.fMask = SIF_POS;
                    SetScrollInfo (hWnd, SB_VERT, &si, TRUE);
                    GetScrollInfo (hWnd, SB_VERT, &si);                                                        
                                               
                    yOverpan -= lastY - gi.ptsLocation.y;
                    lastY = gi.ptsLocation.y;
                     
                    if (gi.dwFlags & GF_BEGIN){
                        BeginPanningFeedback(hWnd);
                        yOverpan = 0;
                    } else if (gi.dwFlags & GF_END) {
                        EndPanningFeedback(hWnd, TRUE);
                        yOverpan = 0;
                    }
                           
                    if (si.nPos == si.nMin){                    
                        // we reached the top, pan upwards in y direction
                        UpdatePanningFeedback(hWnd, 0, yOverpan, gi.dwFlags & GF_INERTIA);
                    }else if (si.nPos >= (si.nMax - si.nPage)){
                        // we reached the bottom, pan downwards in y direction
                        UpdatePanningFeedback(hWnd, 0, yOverpan, gi.dwFlags & GF_INERTIA);
                    }
                    ScrollWindow(hWnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
                    UpdateWindow (hWnd);                    
                                        
                    return DefWindowProc(hWnd, message, lParam, wParam);
  
```



<span data-ttu-id="f0e3c-155">À présent, la fenêtre de votre application doit avoir un retour de limite lorsqu’un utilisateur effectue un panoramique au-delà du bas de la zone de la barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-155">Now your application's window should have boundary feedback when a user pans past the bottom of the scroll bar region.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0e3c-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f0e3c-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0e3c-157">Gestes tactiles Windows</span><span class="sxs-lookup"><span data-stu-id="f0e3c-157">Windows Touch Gestures</span></span>](guide-multi-touch-gestures.md)
</dt> <dt>

[<span data-ttu-id="f0e3c-158">**BeginPanningFeedback**</span><span class="sxs-lookup"><span data-stu-id="f0e3c-158">**BeginPanningFeedback**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-beginpanningfeedback)
</dt> <dt>

[<span data-ttu-id="f0e3c-159">**EndPanningFeedback**</span><span class="sxs-lookup"><span data-stu-id="f0e3c-159">**EndPanningFeedback**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-endpanningfeedback)
</dt> <dt>

[<span data-ttu-id="f0e3c-160">**UpdatePanningFeedback**</span><span class="sxs-lookup"><span data-stu-id="f0e3c-160">**UpdatePanningFeedback**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-updatepanningfeedback)
</dt> </dl>

 

 
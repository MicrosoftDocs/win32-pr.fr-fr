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
# <a name="improving-the-single-finger-panning-experience"></a>Amélioration de l’expérience de panoramique Single-Finger

Si vous générez une application qui cible Windows Touch, elle fournit automatiquement la prise en charge de la panoramisation de base. Toutefois, vous pouvez utiliser le message de [**\_ mouvement WM**](wm-gesture.md) pour fournir une prise en charge améliorée pour le panoramique à un seul doigt.

## <a name="overview"></a>Vue d’ensemble

Pour améliorer l’expérience de panoramique à un seul doigt, suivez ces étapes, comme expliqué dans les sections suivantes de cette rubrique :

-   Créer une application avec des barres de défilement et avec des raccourcis désactivés.
-   Ajoutez la prise en charge des messages de panoramique des mouvements.
-   Activez Bounce.

## <a name="create-an-application-with-scroll-bars-and-with-flicks-disabled"></a>Créer une application avec des barres de défilement et avec des raccourcis désactivés

Avant de commencer, vous devez créer une application avec des barres de défilement. La section [prise en charge héritée du panorama avec les barres de défilement](legacy-support-for-panning-with-scrollbars.md) explique ce processus. Si vous souhaitez commencer par l’exemple de contenu, accédez à cette section et créez une application avec des barres de défilement, puis désactivez les raccourcis. Si vous disposez déjà d’une application avec des barres de défilement fonctionnelles, désactivez les raccourcis comme décrit dans cette section.

## <a name="add-custom-panning-support-for-gesture-pan-messages"></a>Ajouter une prise en charge de panoramique personnalisée pour les messages panoramiques de mouvements

Pour prendre en charge les messages de panoramique de geste, vous devez les gérer dans la méthode **WndProc** . Les messages de mouvement permettent de déterminer les deltas horizontaux et verticaux pour les messages panoramiques. Les deltas sont utilisés pour mettre à jour l’objet de barre de défilement, qui met à jour l’interface utilisateur.

Tout d’abord, mettez à jour les paramètres de version de Windows dans le fichier targetver. h pour activer Windows Touch. Le code suivant montre les différents paramètres de la version de Windows qui doivent les remplacer dans targetver. h.


```C++
#ifndef WINVER                  // Specifies that the minimum required platform is Windows Vista.
#define WINVER 0x0601           // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT            // Specifies that the minimum required platform is Windows Vista.
#define _WIN32_WINNT 0x0601     // Change this to the appropriate value to target other versions of Windows.
#endif
```



Ensuite, ajoutez le fichier UXTheme. h à votre projet et ajoutez la bibliothèque uxtheme. lib aux dépendances supplémentaires de votre projet.


```C++
#include <uxtheme.h>
```



Ensuite, ajoutez les variables suivantes en haut de la fonction **WndProc** . Ils seront utilisés dans les calculs pour le panoramique.


```C++
// The following are used for the custom panning handler      
BOOL bResult = FALSE;

static int scale = 8;   // altering the scale value will change how fast the page scrolls
static int lastY = 0;   // used for panning calculations (initial / previous vertical position)
static int lastX = 0;   // used for panning calculations (initial / previous horizontal position)
GESTUREINFO gi;  
```



Ensuite, ajoutez le gestionnaire du message [**de \_ mouvement WM**](wm-gesture.md) afin que les barres de défilement soient mises à jour avec des deltas basés sur les gestes panoramiques. Vous bénéficiez ainsi d’un contrôle de panoramique bien plus affiné.

Le code suivant obtient la structure [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) à partir du *lParam*, enregistre la dernière coordonnée y de la structure et détermine la modification de la position pour mettre à jour l’objet de barre de défilement. Le code suivant doit être placé dans votre instruction de commutateur **WndProc** .


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



Désormais, quand vous effectuez le mouvement de panoramique sur votre fenêtre, vous voyez le texte défiler avec inertie. À ce stade, vous souhaiterez peut-être modifier le texte pour qu’il comporte davantage de lignes afin que vous puissiez explorer de grandes sections de texte.

## <a name="boundary-feedback-in-wndproc"></a>Commentaires sur les limites dans WndProc

Les commentaires sur les limites sont un type de retour visuel donné aux utilisateurs lorsqu’ils atteignent la fin d’une zone pannable. Elle est déclenchée par l’application lorsqu’une limite est atteinte. Dans l’exemple d’implémentation précédent du message de [**\_ mouvement WM**](wm-gesture.md) , la condition `(si.nPos == si.yPos)` de fin du cas de **\_ mouvement WM** est utilisée pour vérifier que vous avez atteint la fin d’une région pannable. Les variables suivantes sont utilisées pour effectuer le suivi des valeurs et des erreurs de test.


```C++
// The following are used for panning feedback (Window Bounce)
static int animCount = 0;
static DWORD dwErr   = 0;

static BOOL isOverpan  = FALSE;
static long xOverpan   = 0;
static long yOverpan   = 0;
```



Le cas de mouvement de panoramique est mis à jour pour déclencher un feedback de limite. Le code suivant illustre le cas **de \_ panoramique du GID** à partir du gestionnaire de messages de [**\_ mouvements WM**](wm-gesture.md) .


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



À présent, la fenêtre de votre application doit avoir un retour de limite lorsqu’un utilisateur effectue un panoramique au-delà du bas de la zone de la barre de défilement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestes tactiles Windows](guide-multi-touch-gestures.md)
</dt> <dt>

[**BeginPanningFeedback**](/windows/win32/api/uxtheme/nf-uxtheme-beginpanningfeedback)
</dt> <dt>

[**EndPanningFeedback**](/windows/win32/api/uxtheme/nf-uxtheme-endpanningfeedback)
</dt> <dt>

[**UpdatePanningFeedback**](/windows/win32/api/uxtheme/nf-uxtheme-updatepanningfeedback)
</dt> </dl>

 

 
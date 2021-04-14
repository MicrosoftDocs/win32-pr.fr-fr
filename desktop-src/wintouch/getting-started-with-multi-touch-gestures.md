---
title: Prise en main avec les gestes tactiles Windows
description: Cette section décrit les étapes de base pour l’utilisation de mouvements multipoint.
ms.assetid: 0ffe222a-a0ac-498b-a4ca-85cfb1caba93
keywords:
- Tactile Windows, gestes
- Tactile Windows, messages
- mouvements, à propos de
- mouvements, messages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506fee0667e6eb38469bda10af9ded0ea6d3439f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379645"
---
# <a name="getting-started-with-windows-touch-gestures"></a>Prise en main avec les gestes tactiles Windows

Cette section décrit les étapes de base pour l’utilisation de mouvements multipoint.

Les étapes suivantes sont généralement effectuées lors de l’utilisation de gestes tactiles Windows :

1.  Configurez une fenêtre pour la réception des mouvements.
2.  Gérer les messages de mouvement.
3.  Interpréter les messages de mouvement.

## <a name="setting-up-a-window-to-receive-gestures"></a>Configuration d’une fenêtre pour recevoir des mouvements

Par défaut, vous recevez des messages de [**\_ mouvement WM**](wm-gesture.md) .

> [!Note]  
> Si vous appelez [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), vous ne recevrez plus de messages de [**\_ mouvement WM**](wm-gesture.md) . Si vous ne recevez pas de messages de **\_ mouvement WM** , assurez-vous que vous n’avez pas appelé **RegisterTouchWindow**.

 

Le code suivant illustre une implémentation de InitInstance simple.


```C++
#include <windows.h>


BOOL InitInstance(HINSTANCE hInstance, int nCmdShow)
{
   HWND hWnd;

   hInst = hInstance; // Store instance handle in our global variable

   hWnd = CreateWindow(szWindowClass, szTitle, WS_OVERLAPPEDWINDOW,
      CW_USEDEFAULT, 0, CW_USEDEFAULT, 0, NULL, NULL, hInstance, NULL);

   if (!hWnd)
   {
      return FALSE;
   }

   ShowWindow(hWnd, nCmdShow);
   UpdateWindow(hWnd);

   return TRUE;
}
```



## <a name="handling-gesture-messages"></a>Gestion des messages de mouvement

À l’instar de la gestion des messages d’entrée tactile Windows, vous pouvez gérer les messages de mouvement de plusieurs façons. Si vous utilisez Win32, vous pouvez vérifier le message de [**\_ mouvement WM**](wm-gesture.md) dans WndProc. Si vous créez un autre type d’application, vous pouvez ajouter le message de **\_ mouvement WM** à la table des messages, puis implémenter un gestionnaire personnalisé.

Le code suivant montre comment les messages de mouvement peuvent être gérés.


```C++
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {    
    case WM_GESTURE:
            // Insert handler code here to interpret the gesture.            
            return DecodeGesture(hWnd, message, wParam, lParam);            
```



## <a name="interpreting-the-gesture-messages"></a>Interprétation des messages de mouvement

La fonction [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) est utilisée pour interpréter un message de mouvement dans une structure décrivant le mouvement. La structure, [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo), contient des informations sur le mouvement, telles que l’emplacement où le mouvement a été effectué et le type de mouvement. Le code suivant montre comment récupérer et interpréter un message de mouvement.


```C++
  LRESULT DecodeGesture(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    // Create a structure to populate and retrieve the extra message info.
    GESTUREINFO gi;  
    
    ZeroMemory(&gi, sizeof(GESTUREINFO));
    
    gi.cbSize = sizeof(GESTUREINFO);

    BOOL bResult  = GetGestureInfo((HGESTUREINFO)lParam, &gi);
    BOOL bHandled = FALSE;

    if (bResult){
        // now interpret the gesture
        switch (gi.dwID){
           case GID_ZOOM:
               // Code for zooming goes here     
               bHandled = TRUE;
               break;
           case GID_PAN:
               // Code for panning goes here
               bHandled = TRUE;
               break;
           case GID_ROTATE:
               // Code for rotation goes here
               bHandled = TRUE;
               break;
           case GID_TWOFINGERTAP:
               // Code for two-finger tap goes here
               bHandled = TRUE;
               break;
           case GID_PRESSANDTAP:
               // Code for roll over goes here
               bHandled = TRUE;
               break;
           default:
               // A gesture was not recognized
               break;
        }
    }else{
        DWORD dwErr = GetLastError();
        if (dwErr > 0){
            //MessageBoxW(hWnd, L"Error!", L"Could not retrieve a GESTUREINFO structure.", MB_OK);
        }
    }
    if (bHandled){
        return 0;
    }else{
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
  }
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestes tactiles Windows](guide-multi-touch-gestures.md)
</dt> </dl>

 

 





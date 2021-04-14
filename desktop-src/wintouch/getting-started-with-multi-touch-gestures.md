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
# <a name="getting-started-with-windows-touch-gestures"></a><span data-ttu-id="a0f72-107">Prise en main avec les gestes tactiles Windows</span><span class="sxs-lookup"><span data-stu-id="a0f72-107">Getting Started with Windows Touch Gestures</span></span>

<span data-ttu-id="a0f72-108">Cette section décrit les étapes de base pour l’utilisation de mouvements multipoint.</span><span class="sxs-lookup"><span data-stu-id="a0f72-108">This section describes the basic steps for using multitouch gestures.</span></span>

<span data-ttu-id="a0f72-109">Les étapes suivantes sont généralement effectuées lors de l’utilisation de gestes tactiles Windows :</span><span class="sxs-lookup"><span data-stu-id="a0f72-109">The following steps are typically performed when using Windows Touch gestures:</span></span>

1.  <span data-ttu-id="a0f72-110">Configurez une fenêtre pour la réception des mouvements.</span><span class="sxs-lookup"><span data-stu-id="a0f72-110">Set up a window for receiving gestures.</span></span>
2.  <span data-ttu-id="a0f72-111">Gérer les messages de mouvement.</span><span class="sxs-lookup"><span data-stu-id="a0f72-111">Handle the gesture messages.</span></span>
3.  <span data-ttu-id="a0f72-112">Interpréter les messages de mouvement.</span><span class="sxs-lookup"><span data-stu-id="a0f72-112">Interpret the gesture messages.</span></span>

## <a name="setting-up-a-window-to-receive-gestures"></a><span data-ttu-id="a0f72-113">Configuration d’une fenêtre pour recevoir des mouvements</span><span class="sxs-lookup"><span data-stu-id="a0f72-113">Setting up a Window to Receive Gestures</span></span>

<span data-ttu-id="a0f72-114">Par défaut, vous recevez des messages de [**\_ mouvement WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="a0f72-114">By default, you receive [**WM\_GESTURE**](wm-gesture.md) messages.</span></span>

> [!Note]  
> <span data-ttu-id="a0f72-115">Si vous appelez [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), vous ne recevrez plus de messages de [**\_ mouvement WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="a0f72-115">If you call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will stop receiving [**WM\_GESTURE**](wm-gesture.md) messages.</span></span> <span data-ttu-id="a0f72-116">Si vous ne recevez pas de messages de **\_ mouvement WM** , assurez-vous que vous n’avez pas appelé **RegisterTouchWindow**.</span><span class="sxs-lookup"><span data-stu-id="a0f72-116">If you are not receiving **WM\_GESTURE** messages, make sure that you haven't called **RegisterTouchWindow**.</span></span>

 

<span data-ttu-id="a0f72-117">Le code suivant illustre une implémentation de InitInstance simple.</span><span class="sxs-lookup"><span data-stu-id="a0f72-117">The following code shows a simple InitInstance implementation.</span></span>


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



## <a name="handling-gesture-messages"></a><span data-ttu-id="a0f72-118">Gestion des messages de mouvement</span><span class="sxs-lookup"><span data-stu-id="a0f72-118">Handling Gesture Messages</span></span>

<span data-ttu-id="a0f72-119">À l’instar de la gestion des messages d’entrée tactile Windows, vous pouvez gérer les messages de mouvement de plusieurs façons.</span><span class="sxs-lookup"><span data-stu-id="a0f72-119">Similar to handling Windows Touch input messages, you can handle gesture messages in many ways.</span></span> <span data-ttu-id="a0f72-120">Si vous utilisez Win32, vous pouvez vérifier le message de [**\_ mouvement WM**](wm-gesture.md) dans WndProc.</span><span class="sxs-lookup"><span data-stu-id="a0f72-120">If you are using Win32, you can check for the [**WM\_GESTURE**](wm-gesture.md) message in WndProc.</span></span> <span data-ttu-id="a0f72-121">Si vous créez un autre type d’application, vous pouvez ajouter le message de **\_ mouvement WM** à la table des messages, puis implémenter un gestionnaire personnalisé.</span><span class="sxs-lookup"><span data-stu-id="a0f72-121">If you are creating another type of application, you can add the **WM\_GESTURE** message to the message map and then implement a custom handler.</span></span>

<span data-ttu-id="a0f72-122">Le code suivant montre comment les messages de mouvement peuvent être gérés.</span><span class="sxs-lookup"><span data-stu-id="a0f72-122">The following code shows how gesture messages could be handled.</span></span>


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



## <a name="interpreting-the-gesture-messages"></a><span data-ttu-id="a0f72-123">Interprétation des messages de mouvement</span><span class="sxs-lookup"><span data-stu-id="a0f72-123">Interpreting the Gesture Messages</span></span>

<span data-ttu-id="a0f72-124">La fonction [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) est utilisée pour interpréter un message de mouvement dans une structure décrivant le mouvement.</span><span class="sxs-lookup"><span data-stu-id="a0f72-124">The [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) function is used to interpret a gesture message into a structure describing the gesture.</span></span> <span data-ttu-id="a0f72-125">La structure, [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo), contient des informations sur le mouvement, telles que l’emplacement où le mouvement a été effectué et le type de mouvement.</span><span class="sxs-lookup"><span data-stu-id="a0f72-125">The structure, [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo), has information about the gesture such as the location where the gesture was performed and the type of gesture.</span></span> <span data-ttu-id="a0f72-126">Le code suivant montre comment récupérer et interpréter un message de mouvement.</span><span class="sxs-lookup"><span data-stu-id="a0f72-126">The following code shows how you can retrieve and interpret a gesture message.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a0f72-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a0f72-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0f72-128">Gestes tactiles Windows</span><span class="sxs-lookup"><span data-stu-id="a0f72-128">Windows Touch Gestures</span></span>](guide-multi-touch-gestures.md)
</dt> </dl>

 

 





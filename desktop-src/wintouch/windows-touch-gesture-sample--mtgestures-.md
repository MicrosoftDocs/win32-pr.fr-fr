---
title: Exemple de mouvement tactile Windows (MTGestures)
description: Cette section décrit l’exemple de mouvement tactile Windows.
ms.assetid: 04166c9c-5de7-409e-9d5e-dd210a3a3f11
keywords:
- Windows Touch, exemples de code
- Tactile Windows, exemple de code
- Tactile Windows, gestes
- Tactile Windows, exemples de mouvements
- Exemples de mouvements
- gestes, exemple de code
- mouvements, exemples de code
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 0e01d97e844af37caeb5c33f3cb780601da4629d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723443"
---
# <a name="windows-touch-gesture-sample-mtgestures"></a><span data-ttu-id="aaa1e-110">Exemple de mouvement tactile Windows (MTGestures)</span><span class="sxs-lookup"><span data-stu-id="aaa1e-110">Windows Touch Gesture Sample (MTGestures)</span></span>

<span data-ttu-id="aaa1e-111">Cette section décrit l’exemple de mouvement tactile Windows.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-111">This section describes the Windows Touch Gesture sample.</span></span>

<span data-ttu-id="aaa1e-112">L’exemple de mouvement tactile Windows montre comment utiliser des messages de mouvement pour translater, faire pivoter et mettre à l’échelle une zone rendue par le Graphics Device Interface (GDI) en gérant le message [**WM_GESTURE**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="aaa1e-112">The Windows Touch Gesture sample demonstrates how to use gesture messages to translate, rotate, and scale a box rendered by the Graphics Device Interface (GDI) by handling the [**WM_GESTURE**](wm-gesture.md) message.</span></span> <span data-ttu-id="aaa1e-113">La capture d’écran suivante montre comment l’exemple apparaît lorsqu’il est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-113">The following screen shot shows how the sample looks when it is running.</span></span>

![capture d’écran montrant l’exemple de mouvement tactile Windows lorsqu’il est en cours d’exécution, avec un rectangle blanc pivoté et entouré d’un noir à l’écran](images/mtgestures.png)

<span data-ttu-id="aaa1e-115">Pour cet exemple, les messages de mouvement sont passés à un moteur de mouvement, qui appelle ensuite des méthodes sur des objets de dessin pour translater, faire pivoter et mettre à l’échelle un objet qui a des méthodes pour gérer ces commandes.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-115">For this sample, gesture messages are passed to a gesture engine, which then calls methods on drawing objects to translate, rotate, and scale an object that has methods for handling these commands.</span></span> <span data-ttu-id="aaa1e-116">Pour vous aider à voir comment fonctionne l’exemple, examinez les étapes d’utilisation de la commande TAP à deux doigts pour activer ou désactiver les lignes diagonales dans la zone rendue.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-116">To help show how the sample works, consider the steps for using the two-finger tap command to enable or disable diagonal lines in the rendered box.</span></span> <span data-ttu-id="aaa1e-117">Un utilisateur effectue le mouvement TAP à deux doigts, ce qui génère un message géré par le programme.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-117">A user performs the two-finger tap gesture, which generates a message that is handled by the program.</span></span> <span data-ttu-id="aaa1e-118">Lorsque le message est géré, il bascule une valeur booléenne pour le rendu des diagonales sur l’objet de dessin, et l’objet restitue ensuite les lignes diagonales.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-118">When the message is handled, it will toggle a Boolean for rendering diagonals on the drawing object, and the object will then render the diagonal lines.</span></span>

<span data-ttu-id="aaa1e-119">Le code suivant montre comment les messages de mouvement sont passés au moteur de mouvement à partir de la méthode WndProc.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-119">The following code shows how gesture messages are passed to the gesture engine from the WndProc method.</span></span>

```C++
    case WM_GESTURE:
        // The gesture-processing code is implemented in the CGestureEngine
        // class.
        return g_cGestureEngine.WndProc(hWnd,wParam,lParam);
        break;
```

<span data-ttu-id="aaa1e-120">Le code suivant montre comment le moteur de mouvement gère la commande TAP à deux doigts.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-120">The following code shows how the gesture engine handles the two-finger tap command.</span></span>

```C++
// Two-finger tap command
void CMyGestureEngine::ProcessTwoFingerTap(void)
{
    if(_pcRect)
    {
        _pcRect->ToggleDrawDiagonals();
    }
}
```

<span data-ttu-id="aaa1e-121">Le code suivant montre comment l’objet Drawing bascule ses diagonales.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-121">The following code shows how the drawing object toggles its diagonals.</span></span>

```C++
void ToggleDrawDiagonals(void){_bDrawDiagonals = !_bDrawDiagonals;}
```

<span data-ttu-id="aaa1e-122">Le code suivant montre comment l’objet restitue des lignes diagonales dans sa méthode Draw.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-122">The following code shows how the object renders diagonal lines in its draw method.</span></span>

```C++
    if(_bDrawDiagonals)
    {
        // draw diagonals
        MoveToEx(hdc,ptRect[0].x,ptRect[0].y,NULL);
        LineTo(hdc,ptRect[2].x,ptRect[2].y);
        MoveToEx(hdc,ptRect[1].x,ptRect[1].y,NULL);
        LineTo(hdc,ptRect[3].x,ptRect[3].y);
    }
```

## <a name="related-topics"></a><span data-ttu-id="aaa1e-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aaa1e-123">Related topics</span></span>

<span data-ttu-id="aaa1e-124">[Application de mouvements tactiles multiples (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [application de gestes multipoint (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), exemples de [fonctions tactiles Windows](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="aaa1e-124">[Multi-touch Gestures Application (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [Multi-touch Gestures Application (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>

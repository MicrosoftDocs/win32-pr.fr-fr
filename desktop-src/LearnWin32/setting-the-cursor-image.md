---
title: Définition de l’image de curseur
description: Définition de l’image de curseur
ms.assetid: FB223131-19AE-41DD-87DE-73992AE2A0CA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3bc993b7566dee1fa47bd2b53c270ad0e4f64b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463034"
---
# <a name="setting-the-cursor-image"></a><span data-ttu-id="2dcd5-103">Définition de l’image de curseur</span><span class="sxs-lookup"><span data-stu-id="2dcd5-103">Setting the Cursor Image</span></span>

<span data-ttu-id="2dcd5-104">Le *curseur* est la petite image qui indique l’emplacement de la souris ou d’un autre dispositif de pointage.</span><span class="sxs-lookup"><span data-stu-id="2dcd5-104">The *cursor* is the small image that shows the location of the mouse or other pointing device.</span></span> <span data-ttu-id="2dcd5-105">De nombreuses applications modifient l’image du curseur pour fournir des commentaires à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2dcd5-105">Many applications change the cursor image to give feedback to the user.</span></span> <span data-ttu-id="2dcd5-106">Bien qu’elle ne soit pas obligatoire, elle ajoute un peu de poli à votre application.</span><span class="sxs-lookup"><span data-stu-id="2dcd5-106">Although it is not required, it adds a nice bit of polish to your application.</span></span>

<span data-ttu-id="2dcd5-107">Windows fournit un ensemble d’images de curseurs standard, appelées *curseurs système*.</span><span class="sxs-lookup"><span data-stu-id="2dcd5-107">Windows provides a set of standard cursor images, called *system cursors*.</span></span> <span data-ttu-id="2dcd5-108">Il peut s’agir de la flèche, de la main, du pointeur en I, du sablier (qui est maintenant un cercle tournant) et d’autres.</span><span class="sxs-lookup"><span data-stu-id="2dcd5-108">These include the arrow, the hand, the I-beam, the hourglass (which is now a spinning circle), and others.</span></span> <span data-ttu-id="2dcd5-109">Cette section décrit comment utiliser les curseurs système.</span><span class="sxs-lookup"><span data-stu-id="2dcd5-109">This section describes how to use the system cursors.</span></span> <span data-ttu-id="2dcd5-110">Pour des tâches plus avancées, telles que la création de curseurs personnalisés, consultez [curseurs](/windows/desktop/menurc/cursors).</span><span class="sxs-lookup"><span data-stu-id="2dcd5-110">For more advanced tasks, such as creating custom cursors, see [Cursors](/windows/desktop/menurc/cursors).</span></span>

<span data-ttu-id="2dcd5-111">Vous pouvez associer un curseur à une classe de fenêtre en définissant le membre **hCursor** de la structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) ou [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) .</span><span class="sxs-lookup"><span data-stu-id="2dcd5-111">You can associate a cursor with a window class by setting the **hCursor** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) or [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) structure.</span></span> <span data-ttu-id="2dcd5-112">Dans le cas contraire, le curseur par défaut est la flèche.</span><span class="sxs-lookup"><span data-stu-id="2dcd5-112">Otherwise, the default cursor is the arrow.</span></span> <span data-ttu-id="2dcd5-113">Lorsque la souris passe au-dessus d’une fenêtre, la fenêtre reçoit un message [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) (sauf si une autre fenêtre a capturé la souris).</span><span class="sxs-lookup"><span data-stu-id="2dcd5-113">When the mouse moves over a window, the window receives a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message (unless another window has captured the mouse).</span></span> <span data-ttu-id="2dcd5-114">À ce stade, l’un des événements suivants se produit :</span><span class="sxs-lookup"><span data-stu-id="2dcd5-114">At this point, one of the following events occurs:</span></span>

-   <span data-ttu-id="2dcd5-115">L’application définit le curseur et la procédure de fenêtre retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="2dcd5-115">The application sets the cursor and the window procedure returns **TRUE**.</span></span>
-   <span data-ttu-id="2dcd5-116">L’application ne fait rien et transmet [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="2dcd5-116">The application does nothing and passes [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="2dcd5-117">Pour définir le curseur, un programme effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2dcd5-117">To set the cursor, a program does the following:</span></span>

1.  <span data-ttu-id="2dcd5-118">Appelle [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) pour charger le curseur en mémoire.</span><span class="sxs-lookup"><span data-stu-id="2dcd5-118">Calls [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) to load the cursor into memory.</span></span> <span data-ttu-id="2dcd5-119">Cette fonction retourne un handle au curseur.</span><span class="sxs-lookup"><span data-stu-id="2dcd5-119">This function returns a handle to the cursor.</span></span>
2.  <span data-ttu-id="2dcd5-120">Appelle [**SetCursor**](/windows/desktop/api/winuser/nf-winuser-setcursor) et passe dans le handle de curseur.</span><span class="sxs-lookup"><span data-stu-id="2dcd5-120">Calls [**SetCursor**](/windows/desktop/api/winuser/nf-winuser-setcursor) and passes in the cursor handle.</span></span>

<span data-ttu-id="2dcd5-121">Sinon, si l’application passe [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), la fonction **DefWindowProc** utilise l’algorithme suivant pour définir l’image de curseur :</span><span class="sxs-lookup"><span data-stu-id="2dcd5-121">Otherwise, if the application passes [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), the **DefWindowProc** function uses the following algorithm to set the cursor image:</span></span>

1.  <span data-ttu-id="2dcd5-122">Si la fenêtre a un parent, transférez le message [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) au parent pour le gérer.</span><span class="sxs-lookup"><span data-stu-id="2dcd5-122">If the window has a parent, forward the [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message to the parent to handle.</span></span>
2.  <span data-ttu-id="2dcd5-123">Sinon, si la fenêtre possède un curseur de classe, définissez le curseur sur la classe Cursor.</span><span class="sxs-lookup"><span data-stu-id="2dcd5-123">Otherwise, if the window has a class cursor, set the cursor to the class cursor.</span></span>
3.  <span data-ttu-id="2dcd5-124">S’il n’y a aucun curseur de classe, définissez le curseur sur le curseur en flèche.</span><span class="sxs-lookup"><span data-stu-id="2dcd5-124">If there is no class cursor, set the cursor to the arrow cursor.</span></span>

<span data-ttu-id="2dcd5-125">La fonction [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) peut charger soit un curseur personnalisé à partir d’une ressource, soit l’un des curseurs système.</span><span class="sxs-lookup"><span data-stu-id="2dcd5-125">The [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) function can load either a custom cursor from a resource, or one of the system cursors.</span></span> <span data-ttu-id="2dcd5-126">L’exemple suivant montre comment définir le curseur sur le curseur de la main du système.</span><span class="sxs-lookup"><span data-stu-id="2dcd5-126">The following example shows how to set the cursor to the system hand cursor.</span></span>


```C++
    hCursor = LoadCursor(NULL, cursor);
    SetCursor(hCursor);
```



<span data-ttu-id="2dcd5-127">Si vous modifiez le curseur, l’image de curseur se réinitialise au prochain déplacement de la souris, sauf si vous interceptez le message [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) et redéfinissez le curseur.</span><span class="sxs-lookup"><span data-stu-id="2dcd5-127">If you change the cursor, the cursor image resets on the next mouse move, unless you intercept the [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message and set the cursor again.</span></span> <span data-ttu-id="2dcd5-128">Le code suivant montre comment gérer **WM \_ SETCURSOR**.</span><span class="sxs-lookup"><span data-stu-id="2dcd5-128">The following code shows how to handle **WM\_SETCURSOR**.</span></span>


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



<span data-ttu-id="2dcd5-129">Ce code vérifie d’abord les 16 bits inférieurs de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="2dcd5-129">This code first checks the lower 16 bits of *lParam*.</span></span> <span data-ttu-id="2dcd5-130">Si est `LOWORD(lParam)` égal à **HTCLIENT**, cela signifie que le curseur se trouve sur la zone cliente de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="2dcd5-130">If `LOWORD(lParam)` equals **HTCLIENT**, it means the cursor is over the client area of the window.</span></span> <span data-ttu-id="2dcd5-131">Dans le cas contraire, le curseur se trouve sur la zone non cliente.</span><span class="sxs-lookup"><span data-stu-id="2dcd5-131">Otherwise, the cursor is over the nonclient area.</span></span> <span data-ttu-id="2dcd5-132">En règle générale, vous devez uniquement définir le curseur pour la zone cliente et laisser Windows définir le curseur pour la zone non cliente.</span><span class="sxs-lookup"><span data-stu-id="2dcd5-132">Typically, you should only set the cursor for the client area, and let Windows set the cursor for the nonclient area.</span></span>

## <a name="next"></a><span data-ttu-id="2dcd5-133">Suivant</span><span class="sxs-lookup"><span data-stu-id="2dcd5-133">Next</span></span>

[<span data-ttu-id="2dcd5-134">Entrée utilisateur : exemple étendu</span><span class="sxs-lookup"><span data-stu-id="2dcd5-134">User Input: Extended Example</span></span>](user-input--extended-example.md)

 

 
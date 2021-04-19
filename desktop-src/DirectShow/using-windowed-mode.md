---
description: Utilisation du mode fenêtre
ms.assetid: 09ee4568-348b-4cf9-bb38-dada291cdef9
title: Utilisation du mode fenêtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95309f5546ce4f00a8dde029390b2edf48544f1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534351"
---
# <a name="using-windowed-mode"></a><span data-ttu-id="88f8d-103">Utilisation du mode fenêtre</span><span class="sxs-lookup"><span data-stu-id="88f8d-103">Using Windowed Mode</span></span>

> [!Note]  
> <span data-ttu-id="88f8d-104">Le [filtre de convertisseur vidéo](video-renderer-filter.md) hérité utilise toujours le mode fenêtre.</span><span class="sxs-lookup"><span data-stu-id="88f8d-104">The legacy [Video Renderer Filter](video-renderer-filter.md) always uses windowed mode.</span></span> <span data-ttu-id="88f8d-105">Les filtres VMR-7 et VMR-9 utilisent le mode fenêtre par défaut, mais prennent également en charge le mode sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="88f8d-105">The VMR-7 and VMR-9 filters use windowed mode by default, but also support windowless mode.</span></span>

 

<span data-ttu-id="88f8d-106">En mode fenêtre, le convertisseur vidéo crée sa propre fenêtre dans laquelle il peint les images vidéo.</span><span class="sxs-lookup"><span data-stu-id="88f8d-106">In windowed mode, the video renderer creates its own window where it paints the video frames.</span></span> <span data-ttu-id="88f8d-107">À moins que vous ne spécifiiez sinon, cette fenêtre est une fenêtre de niveau supérieur avec ses propres bordures et barre de titre.</span><span class="sxs-lookup"><span data-stu-id="88f8d-107">Unless you specify otherwise, this window is a top-level window with its own borders and title bar.</span></span> <span data-ttu-id="88f8d-108">La plupart du temps, toutefois, vous attachez la fenêtre vidéo à une fenêtre d’application, de sorte que la vidéo est intégrée à l’interface utilisateur de votre application.</span><span class="sxs-lookup"><span data-stu-id="88f8d-108">Most of the time, however, you will attach the video window to an application window, so that the video is integrated into your application UI.</span></span> <span data-ttu-id="88f8d-109">Ce processus implique les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="88f8d-109">This requires the following steps:</span></span>

1.  <span data-ttu-id="88f8d-110">Requête pour **IVideoWindow**.</span><span class="sxs-lookup"><span data-stu-id="88f8d-110">Query for **IVideoWindow**.</span></span>
2.  <span data-ttu-id="88f8d-111">Définissez la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="88f8d-111">Set the parent window.</span></span>
3.  <span data-ttu-id="88f8d-112">Définissez de nouveaux styles de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="88f8d-112">Set new window styles.</span></span>
4.  <span data-ttu-id="88f8d-113">Placez la fenêtre vidéo à l’intérieur de la fenêtre propriétaire.</span><span class="sxs-lookup"><span data-stu-id="88f8d-113">Position the video window inside the owner window.</span></span>
5.  <span data-ttu-id="88f8d-114">Notifier la fenêtre vidéo des \_ messages de déplacement WM.</span><span class="sxs-lookup"><span data-stu-id="88f8d-114">Notify the video window of WM\_MOVE messages.</span></span>

<span data-ttu-id="88f8d-115">**Requête pour IVideoWindow**</span><span class="sxs-lookup"><span data-stu-id="88f8d-115">**Query for IVideoWindow**</span></span>

<span data-ttu-id="88f8d-116">Avant de commencer la lecture, interrogez le gestionnaire du graphique de filtre pour l’interface **IVideoWindow** :</span><span class="sxs-lookup"><span data-stu-id="88f8d-116">Before starting playback, query the Filter Graph Manager for the **IVideoWindow** interface:</span></span>


```C++
IVideoWindow *pVidWin = NULL;
pGraph->QueryInterface(IID_IVideoWindow, (void **)&pVidWin);
```



<span data-ttu-id="88f8d-117">**Définir la fenêtre parente**</span><span class="sxs-lookup"><span data-stu-id="88f8d-117">**Set the Parent Window**</span></span>

<span data-ttu-id="88f8d-118">Pour définir la fenêtre parente, appelez la méthode [**IVideoWindow ::p ut \_ owner**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) avec un handle vers la fenêtre de votre application.</span><span class="sxs-lookup"><span data-stu-id="88f8d-118">To set the parent window, call the [**IVideoWindow::put\_Owner**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) method with a handle to your application window.</span></span> <span data-ttu-id="88f8d-119">Cette méthode prend une variable de type [**OAHWND**](oahwnd.md), castant donc le handle en ce type :</span><span class="sxs-lookup"><span data-stu-id="88f8d-119">This method takes a variable of type [**OAHWND**](oahwnd.md), so cast the handle to this type:</span></span>


```C++
pVidWin->put_Owner((OAHWND)hwnd);
```



<span data-ttu-id="88f8d-120">**Définir de nouveaux styles de fenêtres**</span><span class="sxs-lookup"><span data-stu-id="88f8d-120">**Set New Window Styles**</span></span>

<span data-ttu-id="88f8d-121">Modifiez le style de la fenêtre vidéo en appelant la méthode [**IVideoWindow ::p ut \_ WindowStyle**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) :</span><span class="sxs-lookup"><span data-stu-id="88f8d-121">Change the style of the video window by calling the [**IVideoWindow::put\_WindowStyle**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) method:</span></span>


```C++
pVidWin->put_WindowStyle(WS_CHILD | WS_CLIPSIBLINGS);
```



<span data-ttu-id="88f8d-122">L' \_ indicateur WS Child définit la fenêtre comme une fenêtre enfant, et l’indicateur WS \_ CLIPSIBLINGS empêche la fenêtre de dessiner à l’intérieur de la zone cliente d’une autre fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="88f8d-122">The WS\_CHILD flag sets the window to be a child window, and the WS\_CLIPSIBLINGS flag prevents the window from drawing inside the client area of another child window.</span></span>

<span data-ttu-id="88f8d-123">**Positionner la fenêtre vidéo**</span><span class="sxs-lookup"><span data-stu-id="88f8d-123">**Position the Video Window**</span></span>

<span data-ttu-id="88f8d-124">Pour définir la position de la vidéo par rapport à la zone cliente de la fenêtre d’application, appelez la méthode [**IVideoWindow :: SetWindowPosition**](/windows/desktop/api/Control/nf-control-ivideowindow-setwindowposition) .</span><span class="sxs-lookup"><span data-stu-id="88f8d-124">To set the position of the video relative to the application window's client area, call the [**IVideoWindow::SetWindowPosition**](/windows/desktop/api/Control/nf-control-ivideowindow-setwindowposition) method.</span></span> <span data-ttu-id="88f8d-125">Cette méthode prend un rectangle qui spécifie le bord gauche, le bord supérieur, la largeur et la hauteur de la fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="88f8d-125">This method takes a rectangle that specifies the left edge, top edge, width, and height of the video window.</span></span> <span data-ttu-id="88f8d-126">Par exemple, le code suivant étire la fenêtre vidéo pour l’adapter à la totalité de la zone cliente de la fenêtre parente :</span><span class="sxs-lookup"><span data-stu-id="88f8d-126">For example, the following code stretches the video window to fit the entire client area of the parent window:</span></span>


```C++
RECT rc;
GetClientRect(hwnd, &rc);
pVidWin->SetWindowPosition(0, 0, rc.right, rc.bottom);
```



<span data-ttu-id="88f8d-127">Pour connaître la taille native de la vidéo, appelez la méthode [**IBasicVideo :: GetVideoSize**](/windows/desktop/api/Control/nf-control-ibasicvideo-getvideosize) sur le gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="88f8d-127">To get the native size of the video, call the [**IBasicVideo::GetVideoSize**](/windows/desktop/api/Control/nf-control-ibasicvideo-getvideosize) method on the Filter Graph Manager.</span></span> <span data-ttu-id="88f8d-128">Vous pouvez utiliser ces informations pour mettre à l’échelle la vidéo et conserver les proportions correctes.</span><span class="sxs-lookup"><span data-stu-id="88f8d-128">You can use that information to scale the video and keep the correct aspect ratio.</span></span>

<span data-ttu-id="88f8d-129">**Répondre aux \_ messages WM Move**</span><span class="sxs-lookup"><span data-stu-id="88f8d-129">**Respond to WM\_MOVE Messages**</span></span>

<span data-ttu-id="88f8d-130">Pour des performances optimales, vous devez notifier le convertisseur vidéo chaque fois que la fenêtre se déplace alors que le graphique est suspendu.</span><span class="sxs-lookup"><span data-stu-id="88f8d-130">For best performance, you should notify the video renderer whenever the window moves while the graph is paused.</span></span> <span data-ttu-id="88f8d-131">Appelez la méthode [**IVideoWindow :: NotifyOwnerMessage**](/windows/desktop/api/Control/nf-control-ivideowindow-notifyownermessage) pour transférer le \_ message WM Move :</span><span class="sxs-lookup"><span data-stu-id="88f8d-131">Call the [**IVideoWindow::NotifyOwnerMessage**](/windows/desktop/api/Control/nf-control-ivideowindow-notifyownermessage) method to forward the WM\_MOVE message:</span></span>


```C++
// (Inside your WindowProc)
case WM_MOVE:
    pVidWin->NotifyOwnerMessage((OAHWND)hWnd, msg, wParam, lParam);
    break;
```



<span data-ttu-id="88f8d-132">Si le convertisseur utilise une superposition matérielle, cette notification entraîne la mise à jour de la position de superposition par le convertisseur.</span><span class="sxs-lookup"><span data-stu-id="88f8d-132">If the renderer is using a hardware overlay, this notification causes the renderer to update the overlay position.</span></span> <span data-ttu-id="88f8d-133">(Le VMR-9 n’utilise pas de superpositions, vous n’avez donc pas besoin d’appeler cette méthode si vous utilisez VMR-9).</span><span class="sxs-lookup"><span data-stu-id="88f8d-133">(The VMR-9 does not use overlays, so you do not need to call this method if you are using the VMR-9.)</span></span>

<span data-ttu-id="88f8d-134">**Nettoyer**</span><span class="sxs-lookup"><span data-stu-id="88f8d-134">**Clean Up**</span></span>

<span data-ttu-id="88f8d-135">Avant de quitter l’application, arrêtez le graphique et redéfinissez le propriétaire de la fenêtre vidéo sur la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="88f8d-135">Before the application exits, stop the graph and reset the video window's owner to **NULL**.</span></span> <span data-ttu-id="88f8d-136">Sinon, les messages de fenêtre peuvent être envoyés à la mauvaise fenêtre, ce qui risque de provoquer des erreurs.</span><span class="sxs-lookup"><span data-stu-id="88f8d-136">Otherwise, window messages might be sent to the wrong window, which is likely to cause errors.</span></span> <span data-ttu-id="88f8d-137">Vous pouvez également masquer la fenêtre vidéo, ou une image vidéo scintillent momentanément à l’écran :</span><span class="sxs-lookup"><span data-stu-id="88f8d-137">Also, hide video window, or else you might see a video image flicker on the screen momentarily:</span></span>


```C++
pControl->Stop(); 
pVidWin->put_Visible(OAFALSE);
pVidWin->put_Owner(NULL);  
```



> [!Note]  
> <span data-ttu-id="88f8d-138">Si le parent de la fenêtre vidéo est un enfant de votre fenêtre d’application principale (en d’autres termes, si la fenêtre vidéo est un enfant d’un enfant), vous devez créer la fenêtre vidéo à l’aide de **CoCreateInstance** et l’ajouter au graphique, au lieu de laisser le gestionnaire de graphes de filtre ajouter le convertisseur vidéo pendant la [connexion intelligente](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="88f8d-138">If the parent of the video window is a child of your main application window (in other words, if the video window is a child of a child), you should create the video window using **CoCreateInstance** and add it to the graph, instead of letting the Filter Graph Manager add the video renderer during [Intelligent Connect](intelligent-connect.md).</span></span> <span data-ttu-id="88f8d-139">Cela permet de s’assurer que la fenêtre vidéo et la fenêtre enfant sont repeintes en même temps.</span><span class="sxs-lookup"><span data-stu-id="88f8d-139">This ensures that the video window and your child window are repainted at the same time.</span></span> <span data-ttu-id="88f8d-140">Dans le cas contraire, la fenêtre enfant peut être peinte sur la fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="88f8d-140">Otherwise, the child window may paint over the video window.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="88f8d-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="88f8d-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88f8d-142">Rendu vidéo</span><span class="sxs-lookup"><span data-stu-id="88f8d-142">Video Rendering</span></span>](video-rendering.md)
</dt> </dl>

 

 




---
title: Barres de défilement plat
description: Microsoft Internet Explorer 4,0 a introduit une nouvelle technologie visuelle appelée barres de défilement plat.
ms.assetid: f7e00e71-bf12-4db9-bb84-6d413b967049
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07fbbdb64aa9815cb56f5dc3bf55ffb17390db38
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730460"
---
# <a name="flat-scroll-bars"></a><span data-ttu-id="49ea8-103">Barres de défilement plat</span><span class="sxs-lookup"><span data-stu-id="49ea8-103">Flat Scroll Bars</span></span>

<span data-ttu-id="49ea8-104">Microsoft Internet Explorer 4,0 a introduit une nouvelle technologie visuelle appelée barres de défilement plat.</span><span class="sxs-lookup"><span data-stu-id="49ea8-104">Microsoft Internet Explorer 4.0 introduced a new visual technology called flat scroll bars.</span></span> <span data-ttu-id="49ea8-105">Fonctionnellement, les barres de défilement plat se comportent comme des barres de défilement standard.</span><span class="sxs-lookup"><span data-stu-id="49ea8-105">Functionally, flat scroll bars behave just like standard scroll bars.</span></span> <span data-ttu-id="49ea8-106">La différence est que vous pouvez personnaliser leur apparence dans une plus grande mesure par rapport aux barres de défilement standard.</span><span class="sxs-lookup"><span data-stu-id="49ea8-106">The difference is that you can customize their appearance to a greater extent than standard scroll bars.</span></span>

<span data-ttu-id="49ea8-107">L’illustration suivante montre une fenêtre qui contient une barre de défilement plate.</span><span class="sxs-lookup"><span data-stu-id="49ea8-107">The following illustration shows a window that contains a flat scroll bar.</span></span>

![capture d’écran d’une fenêtre qui contient une barre de défilement plate](images/flatsb.jpg)

> [!Note]  
> <span data-ttu-id="49ea8-109">Les barres de défilement plat sont prises en charge par les versions 4,71 à 5,82 de Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="49ea8-109">Flat scroll bars are supported by Comctl32.dll versions 4.71 through 5.82.</span></span> <span data-ttu-id="49ea8-110">Les versions 6,00 et ultérieures de Comctl32.dll ne prennent pas en charge les barres de défilement plat.</span><span class="sxs-lookup"><span data-stu-id="49ea8-110">Comctl32.dll versions 6.00 and later do not support flat scroll bars.</span></span>

 

## <a name="using-flat-scroll-bars"></a><span data-ttu-id="49ea8-111">Utilisation des barres de défilement plat</span><span class="sxs-lookup"><span data-stu-id="49ea8-111">Using Flat Scroll Bars</span></span>

<span data-ttu-id="49ea8-112">Cette section décrit comment implémenter des barres de défilement plates dans votre application.</span><span class="sxs-lookup"><span data-stu-id="49ea8-112">This section describes how to implement flat scroll bars in your application.</span></span>

### <a name="before-you-begin"></a><span data-ttu-id="49ea8-113">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="49ea8-113">Before You Begin</span></span>

<span data-ttu-id="49ea8-114">Pour utiliser les fonctions de barre de défilement plat, vous devez inclure commctrl. h dans vos fichiers sources et établir un lien avec Comctl32. lib.</span><span class="sxs-lookup"><span data-stu-id="49ea8-114">To use the flat scroll bar functions, you must include Commctrl.h in your source files and link with Comctl32.lib.</span></span>

### <a name="adding-flat-scroll-bars-to-a-window"></a><span data-ttu-id="49ea8-115">Ajout de barres de défilement plates à une fenêtre</span><span class="sxs-lookup"><span data-stu-id="49ea8-115">Adding Flat Scroll Bars to a Window</span></span>

<span data-ttu-id="49ea8-116">Pour ajouter des barres de défilement plates à une fenêtre, appelez [**InitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb), en passant le handle à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="49ea8-116">To add flat scroll bars to a window, call [**InitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb), passing the handle to the window.</span></span> <span data-ttu-id="49ea8-117">Au lieu d’utiliser les fonctions de barre de défilement standard pour manipuler vos barres de défilement, vous devez utiliser la fonction FlatSB xxx équivalente \_ .</span><span class="sxs-lookup"><span data-stu-id="49ea8-117">Instead of using the standard scroll bar functions to manipulate your scroll bars, you must use the equivalent FlatSB\_XXX function.</span></span> <span data-ttu-id="49ea8-118">Il existe des fonctions de barre de défilement plat pour définir et récupérer les informations de défilement, la plage et la position.</span><span class="sxs-lookup"><span data-stu-id="49ea8-118">There are flat scroll bar functions for setting and retrieving the scroll information, range, and position.</span></span> <span data-ttu-id="49ea8-119">Si les barres de défilement plat n’ont pas été initialisées pour votre fenêtre, l’API de barre de défilement plate sera différée aux fonctions standard correspondantes, si elles sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="49ea8-119">If flat scroll bars haven't been initialized for your window, the flat scroll bar API will defer to the corresponding standard functions, if any are used.</span></span> <span data-ttu-id="49ea8-120">Cela vous permet d’activer et de désactiver les barres de défilement plat sans avoir à écrire du code conditionnel.</span><span class="sxs-lookup"><span data-stu-id="49ea8-120">This allows you to turn flat scroll bars on and off without having to write conditional code.</span></span>

<span data-ttu-id="49ea8-121">Étant donné qu’une application a peut-être défini des métriques personnalisées pour ses barres de défilement plates, elles ne sont pas mises à jour automatiquement en cas de modification des mesures du système.</span><span class="sxs-lookup"><span data-stu-id="49ea8-121">Because an application may have set custom metrics for its flat scroll bars, they are not automatically updated when system metrics change.</span></span> <span data-ttu-id="49ea8-122">Lorsque les mesures de la barre de défilement système changent, un message [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) est Broadcast, avec son *wParam* défini sur [**SPI \_ SETNONCLIENTMETRICS**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).</span><span class="sxs-lookup"><span data-stu-id="49ea8-122">When the system scroll bar metrics change, a [**WM\_SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) message is broadcast, with its *wParam* set to [**SPI\_SETNONCLIENTMETRICS**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).</span></span> <span data-ttu-id="49ea8-123">Pour mettre à jour les barres de défilement plat avec les nouvelles métriques du système, les applications doivent gérer ce message et modifier les propriétés dépendantes de la barre de défilement plat de manière explicite.</span><span class="sxs-lookup"><span data-stu-id="49ea8-123">To update flat scroll bars to the new system metrics, applications must handle this message and change the flat scroll bar's metric-dependent properties explicitly.</span></span>

<span data-ttu-id="49ea8-124">Pour mettre à jour les propriétés de la barre de défilement, utilisez [**FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop).</span><span class="sxs-lookup"><span data-stu-id="49ea8-124">To update your scroll bar properties, use [**FlatSB\_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop).</span></span> <span data-ttu-id="49ea8-125">Le fragment de code suivant modifie les propriétés dépendantes de la mesure de la barre de défilement plate en valeurs système actuelles.</span><span class="sxs-lookup"><span data-stu-id="49ea8-125">The following code fragment changes a flat scroll bar's metric dependent properties to the current system values.</span></span>


```
void FlatSB_UpdateMetrics(HWND hWnd)
{
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXVSCROLL, GetSystemMetrics(SM_CXVSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXHSCROLL, GetSystemMetrics(SM_CXHSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYVSCROLL, GetSystemMetrics(SM_CYVSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYHSCROLL, GetSystemMetrics(SM_CYHSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXHTHUMB, GetSystemMetrics(SM_CXHTHUMB), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYVTHUMB, GetSystemMetrics(SM_CYVTHUMB), TRUE);
}
```



### <a name="enhancing-flat-scroll-bars"></a><span data-ttu-id="49ea8-126">Amélioration des barres de défilement plat</span><span class="sxs-lookup"><span data-stu-id="49ea8-126">Enhancing Flat Scroll Bars</span></span>

<span data-ttu-id="49ea8-127">[**FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) vous permet de modifier les barres de défilement plat pour personnaliser l’apparence de votre fenêtre.</span><span class="sxs-lookup"><span data-stu-id="49ea8-127">[**FlatSB\_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) allows you to modify the flat scroll bars to customize the look of your window.</span></span> <span data-ttu-id="49ea8-128">Pour les barres de défilement verticales, vous pouvez modifier la largeur de la barre et la hauteur des flèches de direction.</span><span class="sxs-lookup"><span data-stu-id="49ea8-128">For vertical scroll bars, you can change the width of the bar and the height of the direction arrows.</span></span> <span data-ttu-id="49ea8-129">Pour les barres de défilement horizontales, vous pouvez modifier la hauteur de la barre et la largeur des flèches de direction.</span><span class="sxs-lookup"><span data-stu-id="49ea8-129">For horizontal scroll bars, you can change the height of the bar and the width of the direction arrows.</span></span> <span data-ttu-id="49ea8-130">Vous pouvez également modifier la couleur d’arrière-plan des barres de défilement horizontale et verticale.</span><span class="sxs-lookup"><span data-stu-id="49ea8-130">You can also change the background color of both the horizontal and vertical scroll bars.</span></span>

<span data-ttu-id="49ea8-131">[**FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) vous permet également de personnaliser le mode d’affichage des barres de défilement plates.</span><span class="sxs-lookup"><span data-stu-id="49ea8-131">[**FlatSB\_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) also allows you to customize how the flat scroll bars are displayed.</span></span> <span data-ttu-id="49ea8-132">En modifiant les \_ Propriétés WSB prop \_ VSTYLE et WSB \_ prop \_ HSTYLE, vous pouvez définir le type de barre de défilement que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="49ea8-132">By changing the WSB\_PROP\_VSTYLE and WSB\_PROP\_HSTYLE properties, you can set the type of scroll bar that you want to use.</span></span> <span data-ttu-id="49ea8-133">Trois styles sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="49ea8-133">Three styles are available.</span></span>



|                    |                                                                                                                                                                          |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49ea8-134">MODE FSB d' \_ Encarta \_</span><span class="sxs-lookup"><span data-stu-id="49ea8-134">FSB\_ENCARTA\_MODE</span></span> | <span data-ttu-id="49ea8-135">Une barre de défilement standard standard est affichée.</span><span class="sxs-lookup"><span data-stu-id="49ea8-135">A standard flat scroll bar is displayed.</span></span> <span data-ttu-id="49ea8-136">Lorsque la souris se déplace sur un bouton de direction ou le curseur de défilement, cette partie de la barre de défilement s’affiche en 3D.</span><span class="sxs-lookup"><span data-stu-id="49ea8-136">When the mouse moves over a direction button or the thumb, that portion of the scroll bar will be displayed in 3-D.</span></span>             |
| <span data-ttu-id="49ea8-137">\_mode plat \_ FSB</span><span class="sxs-lookup"><span data-stu-id="49ea8-137">FSB\_FLAT\_MODE</span></span>    | <span data-ttu-id="49ea8-138">Une barre de défilement standard standard est affichée.</span><span class="sxs-lookup"><span data-stu-id="49ea8-138">A standard flat scroll bar is displayed.</span></span> <span data-ttu-id="49ea8-139">Lorsque la souris se déplace sur un bouton de direction ou le curseur de défilement, cette partie de la barre de défilement s’affiche dans les couleurs inversées.</span><span class="sxs-lookup"><span data-stu-id="49ea8-139">When the mouse moves over a direction button or the thumb, that portion of the scroll bar will be displayed in inverted colors.</span></span> |
| <span data-ttu-id="49ea8-140">\_mode normal \_ FSB</span><span class="sxs-lookup"><span data-stu-id="49ea8-140">FSB\_REGULAR\_MODE</span></span> | <span data-ttu-id="49ea8-141">Une barre de défilement normale et non plate est affichée.</span><span class="sxs-lookup"><span data-stu-id="49ea8-141">A normal, nonflat scroll bar is displayed.</span></span> <span data-ttu-id="49ea8-142">Aucun effet visuel spécial ne sera appliqué.</span><span class="sxs-lookup"><span data-stu-id="49ea8-142">No special visual effects will be applied.</span></span>                                                                                    |



 

### <a name="removing-flat-scroll-bars"></a><span data-ttu-id="49ea8-143">Supprimer des barres de défilement plat</span><span class="sxs-lookup"><span data-stu-id="49ea8-143">Removing Flat Scroll Bars</span></span>

<span data-ttu-id="49ea8-144">Si vous souhaitez supprimer les barres de défilement plat de votre fenêtre, appelez la fonction [**UninitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb) , en passant le handle à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="49ea8-144">If you want to remove flat scroll bars from your window, call the [**UninitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb) function, passing the handle to the window.</span></span> <span data-ttu-id="49ea8-145">Cette fonction supprime uniquement les barres de défilement plat de votre fenêtre au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="49ea8-145">This function only removes flat scroll bars from your window at run time.</span></span> <span data-ttu-id="49ea8-146">Vous n’avez pas besoin d’appeler cette fonction lorsque votre fenêtre est détruite.</span><span class="sxs-lookup"><span data-stu-id="49ea8-146">You do not need to call this function when your window is destroyed.</span></span>

 

 
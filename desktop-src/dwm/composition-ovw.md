---
title: Activer et contrôler la composition DWM
description: Les API de composition Gestionnaire de fenêtrage (DWM) fournissent plusieurs fonctions permettant de définir et d’interroger des informations de base utilisées par le DWM.
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_composition_ovw.htm
keywords:
- Gestionnaire de fenêtrage (DWM), composition
- DWM (Gestionnaire de fenêtrage), composition
- composition
- composition du Bureau
- colorisation
- rendu de région non cliente
- Gestionnaire de fenêtrage (DWM), colorisation
- DWM (Gestionnaire de fenêtrage), colorisation
- Gestionnaire de fenêtrage (DWM), rendu de région non client
- DWM (Gestionnaire de fenêtrage), rendu de région non client
- Gestionnaire de fenêtrage (DWM), messagerie
- DWM (Gestionnaire de fenêtrage), messagerie
- messagerie
ms.topic: article
ms.date: 05/30/2019
ms.openlocfilehash: 8d7654f479896002b4bc65df613fab9506caf2a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840645"
---
# <a name="enable-and-control-dwm-composition"></a><span data-ttu-id="401be-116">Activer et contrôler la composition DWM</span><span class="sxs-lookup"><span data-stu-id="401be-116">Enable and control DWM composition</span></span>

<span data-ttu-id="401be-117">Les API de composition Gestionnaire de fenêtrage (DWM) fournissent plusieurs fonctions permettant de définir et d’interroger des informations de base utilisées par le DWM.</span><span class="sxs-lookup"><span data-stu-id="401be-117">The Desktop Window Manager (DWM) composition APIs provide several functions for setting and querying for basic information that is used by the DWM.</span></span> <span data-ttu-id="401be-118">Ces API vous permettent d’interroger et de modifier l’état de la composition.</span><span class="sxs-lookup"><span data-stu-id="401be-118">These APIs enable you to query and change the composition state.</span></span> <span data-ttu-id="401be-119">En outre, vous pouvez définir et interroger la stratégie de rendu pour différents attributs de fenêtre DWM.</span><span class="sxs-lookup"><span data-stu-id="401be-119">Additionally, you can set and query the rendering policy for different DWM window attributes.</span></span>

## <a name="retrieving-colorization-information"></a><span data-ttu-id="401be-120">Récupération des informations de colorisation</span><span class="sxs-lookup"><span data-stu-id="401be-120">Retrieving colorization information</span></span>

<span data-ttu-id="401be-121">La couleur de la zone non cliente d’une fenêtre est déterminée par le thème de couleur système actuel.</span><span class="sxs-lookup"><span data-stu-id="401be-121">The color of the non-client region of a window is determined by the current system color theme.</span></span> <span data-ttu-id="401be-122">La valeur de colorisation est fournie via les API DWM pour permettre à votre application de correspondre à l’interface utilisateur du client avec le thème de couleur système.</span><span class="sxs-lookup"><span data-stu-id="401be-122">The colorization value is provided through the DWM APIs to enable your application to match client UI with the system color theme.</span></span>

<span data-ttu-id="401be-123">Pour accéder à cette valeur de colorisation et surveiller la modification de couleur, utilisez la fonction [**DwmGetColorizationColor**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetcolorizationcolor) et le message [**WM_DWMCOLORIZATIONCOLORCHANGED**](wm-dwmcolorizationcolorchanged.md) .</span><span class="sxs-lookup"><span data-stu-id="401be-123">To access this colorization value, and monitor the color change, use the [**DwmGetColorizationColor**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetcolorizationcolor) function and the [**WM_DWMCOLORIZATIONCOLORCHANGED**](wm-dwmcolorizationcolorchanged.md) message.</span></span>

<span data-ttu-id="401be-124">Cet exemple montre comment gérer le message de couleur modifiée et accéder à la nouvelle couleur.</span><span class="sxs-lookup"><span data-stu-id="401be-124">This example demonstrates how to handle the color changed message and access the new color.</span></span>

```cpp
...
case WM_DWMCOLORIZATIONCOLORCHANGED:
{
    DWORD newColorizationColor{ (DWORD)wParam };
    BOOL isBlendedWithOpacity{ (BOOL)lParam };
}
break;
...
```

## <a name="controlling-non-client-region-rendering"></a><span data-ttu-id="401be-125">Contrôle du rendu d’une région non cliente</span><span class="sxs-lookup"><span data-stu-id="401be-125">Controlling non-client region rendering</span></span>

<span data-ttu-id="401be-126">La transparence de la zone non cliente d’une fenêtre et des effets de transition sont deux des effets visuels que le DWM active.</span><span class="sxs-lookup"><span data-stu-id="401be-126">Two of the visual effects that DWM enables are transparency of the non-client region of a window, and transition effects.</span></span> <span data-ttu-id="401be-127">Votre application doit peut-être désactiver ou réactiver ces effets pour des raisons de style ou de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="401be-127">Your application might have to disable or re-enable these effects for styling or compatibility reasons.</span></span> <span data-ttu-id="401be-128">Les fonctions suivantes sont utilisées pour gérer la transparence et le comportement d’effet de transition.</span><span class="sxs-lookup"><span data-stu-id="401be-128">The following functions are used to manage transparency and transition effect behavior.</span></span>

- [<span data-ttu-id="401be-129">**DwmGetWindowAttribute**</span><span class="sxs-lookup"><span data-stu-id="401be-129">**DwmGetWindowAttribute**</span></span>](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute)
- [<span data-ttu-id="401be-130">**DwmSetWindowAttribute**</span><span class="sxs-lookup"><span data-stu-id="401be-130">**DwmSetWindowAttribute**</span></span>](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)

<span data-ttu-id="401be-131">Pour récupérer l’état de rendu non client actuel pour la fenêtre d’une application, appelez [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) avec *dwAttribute* défini sur [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute).</span><span class="sxs-lookup"><span data-stu-id="401be-131">To retrieve the current non-client rendering state for an application's window, call [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) with *dwAttribute* set to [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute).</span></span> <span data-ttu-id="401be-132">Comme vous pouvez le voir dans la documentation de [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute), lorsque vous transmettez cet indicateur à **DwmGetWindowAttribute**, la valeur d’attribut Récupérée est de type **bool**.</span><span class="sxs-lookup"><span data-stu-id="401be-132">As you can see from the documentation for [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute), when you pass that flag to **DwmGetWindowAttribute**, the retrieved attribute value is of type **BOOL**.</span></span> <span data-ttu-id="401be-133">Les différents indicateurs font en sorte que **DwmGetWindowAttribute** retourne des valeurs de types différents.</span><span class="sxs-lookup"><span data-stu-id="401be-133">Different flags cause **DwmGetWindowAttribute** to return values of different types.</span></span> <span data-ttu-id="401be-134">Voici un exemple de code :</span><span class="sxs-lookup"><span data-stu-id="401be-134">Here's a code example.</span></span>

```cpp
BOOL isNCRenderingEnabled{ FALSE };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_NCRENDERING_ENABLED,
    &isNCRenderingEnabled,
    sizeof(isNCRenderingEnabled));
```

<span data-ttu-id="401be-135">L’exemple suivant montre comment utiliser l’indicateur [**DWMWA_EXTENDED_FRAME_BOUNDS**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute) avec **DwmGetWindowAttribute** pour récupérer le rectangle de limites de cadre étendu d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="401be-135">This next example shows how to use the [**DWMWA_EXTENDED_FRAME_BOUNDS**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute) flag with **DwmGetWindowAttribute** to retrieve the extended frame bounds rectangle of a window.</span></span> <span data-ttu-id="401be-136">La documentation de cet indicateur nous indique que la valeur de l’attribut récupéré est de type **Rect**.</span><span class="sxs-lookup"><span data-stu-id="401be-136">The documentation for that flag tells us that the retrieved attribute value is of type **RECT**.</span></span>

```cpp
RECT extendedFrameBounds{ 0,0,0,0 };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_EXTENDED_FRAME_BOUNDS,
    &extendedFrameBounds,
    sizeof(extendedFrameBounds));
```

> [!NOTE]
> <span data-ttu-id="401be-137">Suivez le même modèle de programmation que celui illustré ci-dessus lorsque vous appelez [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) avec des indicateurs pour différents attributs.</span><span class="sxs-lookup"><span data-stu-id="401be-137">Follow the same programming pattern shown above when you call [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) with flags for different attributes.</span></span> <span data-ttu-id="401be-138">La rubrique d’énumération [**DWMWINDOWATTRIBUTE**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) indique, dans la ligne pour chaque indicateur, le type de valeur auquel vous devez passer un pointeur dans le paramètre *pvAttribute* pour **DwmGetWindowAttribute**.</span><span class="sxs-lookup"><span data-stu-id="401be-138">The [**DWMWINDOWATTRIBUTE**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) enumeration topic indicates, in the row for each flag, what type of value you should pass a pointer to in the *pvAttribute* parameter for **DwmGetWindowAttribute**.</span></span> <span data-ttu-id="401be-139">Le paramètre *cbAttribute* contient la taille, en octets, de cet objet.</span><span class="sxs-lookup"><span data-stu-id="401be-139">The *cbAttribute* parameter contains the size, in bytes, of that object.</span></span>

<span data-ttu-id="401be-140">[**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) permet à votre application de définir la stratégie de rendu de la zone non cliente.</span><span class="sxs-lookup"><span data-stu-id="401be-140">[**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) enables your application to set the non-client area rendering policy.</span></span> <span data-ttu-id="401be-141">Cette fonction détermine également la manière dont votre application doit gérer les effets de transition DWM.</span><span class="sxs-lookup"><span data-stu-id="401be-141">That function also determines how your application should handle DWM transition effects.</span></span>

<span data-ttu-id="401be-142">L’exemple suivant désactive le rendu de la zone non cliente.</span><span class="sxs-lookup"><span data-stu-id="401be-142">This next example disables non-client area rendering.</span></span> <span data-ttu-id="401be-143">Cela provoque la désactivation des appels précédents à [DwmEnableBlurBehindWindow](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenableblurbehindwindow) ou à [DwmExtendFrameIntoClientArea](/windows/desktop/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) .</span><span class="sxs-lookup"><span data-stu-id="401be-143">This causes any previous calls to [DwmEnableBlurBehindWindow](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenableblurbehindwindow) or to [DwmExtendFrameIntoClientArea](/windows/desktop/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) to be disabled.</span></span>

```
HRESULT DisableNCRendering(HWND hWnd)
{
    HRESULT hr = S_OK;

    DWMNCRENDERINGPOLICY ncrp = DWMNCRP_DISABLED;

    // Disable non-client area rendering on the window.
    hr = ::DwmSetWindowAttribute(hWnd,
        DWMWA_NCRENDERING_POLICY,
        &ncrp,
        sizeof(ncrp));

    if (SUCCEEDED(hr))
    {
        // ...
    }

    return hr;
}
```

<span data-ttu-id="401be-144">En plus de contrôler le rendu de la zone non cliente, [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) peut également contrôler les effets de transition DWM.</span><span class="sxs-lookup"><span data-stu-id="401be-144">In addition to controlling the non-client area rendering, [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) can also control DWM transition effects.</span></span> <span data-ttu-id="401be-145">Vous pouvez définir le comportement de transition en utilisant **DWMWA \_ transitions \_ FORCEDISABLED** comme paramètre *dwAttribute* .</span><span class="sxs-lookup"><span data-stu-id="401be-145">You can set transition behavior by using **DWMWA\_TRANSITIONS\_FORCEDISABLED** as the *dwAttribute* parameter.</span></span>

## <a name="messages"></a><span data-ttu-id="401be-146">Messages</span><span class="sxs-lookup"><span data-stu-id="401be-146">Messages</span></span>

<span data-ttu-id="401be-147">Les messages suivants fournissent une notification des événements DWM.</span><span class="sxs-lookup"><span data-stu-id="401be-147">The following messages provide notification of DWM events.</span></span> <span data-ttu-id="401be-148">Ces messages peuvent être utilisés pour surveiller les modifications telles que les modifications d’état de composition et les modifications de thème de couleur système.</span><span class="sxs-lookup"><span data-stu-id="401be-148">These messages can be used to monitor changes such as composition state changes and system color theme changes.</span></span>

- [<span data-ttu-id="401be-149">**\_DWMCOLORIZATIONCOLORCHANGED WM**</span><span class="sxs-lookup"><span data-stu-id="401be-149">**WM\_DWMCOLORIZATIONCOLORCHANGED**</span></span>](wm-dwmcolorizationcolorchanged.md)
- [<span data-ttu-id="401be-150">**\_DWMCOMPOSITIONCHANGED WM**</span><span class="sxs-lookup"><span data-stu-id="401be-150">**WM\_DWMCOMPOSITIONCHANGED**</span></span>](wm-dwmcompositionchanged.md)
- [<span data-ttu-id="401be-151">**\_DWMNCRENDERINGCHANGED WM**</span><span class="sxs-lookup"><span data-stu-id="401be-151">**WM\_DWMNCRENDERINGCHANGED**</span></span>](wm-dwmncrenderingchanged.md)
- [<span data-ttu-id="401be-152">**\_DWMWINDOWMAXIMIZEDCHANGE WM**</span><span class="sxs-lookup"><span data-stu-id="401be-152">**WM\_DWMWINDOWMAXIMIZEDCHANGE**</span></span>](wm-dwmwindowmaximizedchange.md)

## <a name="disabling-dwm-composition-windows7-and-earlier"></a><span data-ttu-id="401be-153">Désactivation de la composition DWM (Windows 7 et versions antérieures)</span><span class="sxs-lookup"><span data-stu-id="401be-153">Disabling DWM composition (Windows 7 and earlier)</span></span>

> [!WARNING]
> <span data-ttu-id="401be-154">Les informations de cette section s’appliquent uniquement aux systèmes Windows 7 et versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="401be-154">The info in this section applies only to Windows 7 and earlier systems.</span></span>

<span data-ttu-id="401be-155">Étant donné que DWM utilise l’unité de traitement graphique (GPU) pour la composition du bureau, votre application doit peut-être désactiver DWM pour des raisons de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="401be-155">Because DWM uses the graphics processing unit (GPU) for desktop composition, your application might have to disable DWM for compatibility.</span></span> <span data-ttu-id="401be-156">Les applications qui prennent le contrôle total du bureau, comme les jeux qui s’exécutent en mode plein écran, doivent déterminer si le DWM est activé et, si c’est le cas, le désactiver.</span><span class="sxs-lookup"><span data-stu-id="401be-156">Applications that take full control of the desktop, such as games that run in full-screen mode, must determine whether the DWM is enabled and if it is, disable it.</span></span> <span data-ttu-id="401be-157">Pour ce faire, deux fonctions sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="401be-157">To do this, two functions are needed.</span></span>

- [<span data-ttu-id="401be-158">**DwmIsCompositionEnabled**</span><span class="sxs-lookup"><span data-stu-id="401be-158">**DwmIsCompositionEnabled**</span></span>](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled)
- [<span data-ttu-id="401be-159">**DwmEnableComposition**</span><span class="sxs-lookup"><span data-stu-id="401be-159">**DwmEnableComposition**</span></span>](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)

<span data-ttu-id="401be-160">Un appel à [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition) avec *FEnable* défini sur **DWM \_ EC \_ DISABLECOMPOSITION** désactive la composition DWM jusqu’à ce que le processus appelant soit arrêté ou que la composition ait été réactivée en appelant **DwmEnableComposition** avec *fEnable* défini sur **DWM \_ EC \_ ENABLECOMPOSITION**.</span><span class="sxs-lookup"><span data-stu-id="401be-160">A call to [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition) with *fEnable* set to **DWM\_EC\_DISABLECOMPOSITION** disables DWM composition until either the calling process has shut down, or composition has been re-enabled by calling **DwmEnableComposition** with *fEnable* set to **DWM\_EC\_ENABLECOMPOSITION**.</span></span> <span data-ttu-id="401be-161">La composition DWM redémarre automatiquement dès que toutes les applications qui ont une composition désactivée ont été arrêtées ou ont été réactivées manuellement en appelant **DwmEnableComposition**.</span><span class="sxs-lookup"><span data-stu-id="401be-161">DWM composition restarts automatically as soon as all applications that have disabled composition have either shut down or have manually re-enabled composition by calling **DwmEnableComposition**.</span></span>

> [!NOTE]  
> <span data-ttu-id="401be-162">Le DWM désactive automatiquement la composition lorsqu’une application tente de dessiner directement sur la surface d’affichage principale.</span><span class="sxs-lookup"><span data-stu-id="401be-162">The DWM automatically disables composition when an application attempts to draw directly to the primary display surface.</span></span> <span data-ttu-id="401be-163">La composition sera désactivée jusqu’à ce que la surface principale du périphérique soit libérée par cette application.</span><span class="sxs-lookup"><span data-stu-id="401be-163">Composition will be disabled until the primary device surface is released by that application.</span></span>

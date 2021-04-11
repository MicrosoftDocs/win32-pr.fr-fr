---
title: Vue d’ensemble du DWM en arrière-plan
description: L’un des effets de signature Gestionnaire de fenêtrage (DWM) est une zone non cliente translucide et floue. Les API DWM permettent aux applications d’appliquer ces effets à la zone cliente de leurs fenêtres de niveau supérieur.
ms.assetid: bdf0f8bd-e399-4244-ae39-460f09a16f3c
keywords:
- Gestionnaire de fenêtrage (DWM), effet de flou-arrière-plan
- DWM (Gestionnaire de fenêtrage), effet de flou
- effet Flou-arrière-plan
- effet translucide
- effet de transparence transparent
- Gestionnaire de fenêtrage (DWM), effet translucide
- DWM (Gestionnaire de fenêtrage), effet translucide
- Gestionnaire de fenêtrage (DWM), effet de transparence transparent
- DWM (Gestionnaire de fenêtrage), effet de transparence transparent
- Gestionnaire de fenêtrage (DWM), extension du frame de fenêtre dans la zone cliente
- DWM (Gestionnaire de fenêtrage), extension du frame de fenêtre dans la zone cliente
- extension du frame de fenêtre dans la zone cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcf7378cfcaff93aa9a54ce399890ec1bfd8cc1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031755"
---
# <a name="dwm-blur-behind-overview"></a><span data-ttu-id="5b74e-116">Vue d’ensemble du DWM en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="5b74e-116">DWM Blur Behind Overview</span></span>

<span data-ttu-id="5b74e-117">L’un des effets de signature Gestionnaire de fenêtrage (DWM) est une zone non cliente translucide et floue.</span><span class="sxs-lookup"><span data-stu-id="5b74e-117">One of the signature Desktop Window Manager (DWM) effects is a translucent and blurred non-client area.</span></span> <span data-ttu-id="5b74e-118">Les API DWM permettent aux applications d’appliquer ces effets à la zone cliente de leurs fenêtres de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="5b74e-118">The DWM APIs enable applications to apply these effects to the client area of their top-level windows.</span></span>

> [!Note]  
> <span data-ttu-id="5b74e-119">Windows Vista Édition personnelle basique ne prend pas en charge l’effet de transparence transparent.</span><span class="sxs-lookup"><span data-stu-id="5b74e-119">Windows Vista Home Basic edition does not support the transparent glass effect.</span></span> <span data-ttu-id="5b74e-120">Les zones qui s’affichent généralement avec l’effet de transparence sur les autres éditions de Windows sont rendues opaques.</span><span class="sxs-lookup"><span data-stu-id="5b74e-120">Areas that would typically render with the transparent glass effect on other Windows editions are rendered as opaque.</span></span>
> <span data-ttu-id="5b74e-121">À partir de Windows 8, l’appel de cette fonction n’entraîne pas l’effet de flou, en raison d’un changement de style dans la manière dont les fenêtres sont affichées.</span><span class="sxs-lookup"><span data-stu-id="5b74e-121">Beginning with Windows 8, calling this function doesn't result in the blur effect, due to a style change in the way windows are rendered.</span></span>


 

<span data-ttu-id="5b74e-122">Cette rubrique décrit les scénarios de flou de client suivants que le DWM active.</span><span class="sxs-lookup"><span data-stu-id="5b74e-122">This topic discusses the following client blur-behind scenarios that the DWM enables.</span></span>

-   [<span data-ttu-id="5b74e-123">Ajout d’un flou à une région spécifique de la zone cliente</span><span class="sxs-lookup"><span data-stu-id="5b74e-123">Adding Blur to a Specific Region of the Client Area</span></span>](#adding-blur-to-a-specific-region-of-the-client-area)
-   [<span data-ttu-id="5b74e-124">Extension du frame de fenêtre dans la zone cliente</span><span class="sxs-lookup"><span data-stu-id="5b74e-124">Extending the Window Frame into the Client Area</span></span>](#extending-the-window-frame-into-the-client-area)
-   [<span data-ttu-id="5b74e-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5b74e-125">Related topics</span></span>](#related-topics)

## <a name="adding-blur-to-a-specific-region-of-the-client-area"></a><span data-ttu-id="5b74e-126">Ajout d’un flou à une région spécifique de la zone cliente</span><span class="sxs-lookup"><span data-stu-id="5b74e-126">Adding Blur to a Specific Region of the Client Area</span></span>

<span data-ttu-id="5b74e-127">Une application peut appliquer l’effet de flou derrière la région cliente entière de la fenêtre ou à une sous-région spécifique.</span><span class="sxs-lookup"><span data-stu-id="5b74e-127">An application can apply the blur effect behind the whole client region of the window or to a specific subregion.</span></span> <span data-ttu-id="5b74e-128">Cela permet aux applications d’ajouter un chemin d’accès et des barres de recherche stylisés qui sont visuellement séparés du reste de l’application.</span><span class="sxs-lookup"><span data-stu-id="5b74e-128">This enables applications to add styled path and search bars that are visually separate from the rest of the application.</span></span>

<span data-ttu-id="5b74e-129">L’API utilisée dans ce scénario est la fonction [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) , qui utilise le [**brouilleur de DWM derrière les constantes**](dwm-bb-constants.md) et la structure [**DWM \_ BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) .</span><span class="sxs-lookup"><span data-stu-id="5b74e-129">The API used in this scenario is the [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) function, which makes use of the [**DWM Blur Behind Constants**](dwm-bb-constants.md) and the [**DWM\_BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) structure.</span></span>

<span data-ttu-id="5b74e-130">L’exemple de fonction suivant, `EnableBlurBehind` , illustre comment appliquer l’effet Flou-arrière à la fenêtre entière.</span><span class="sxs-lookup"><span data-stu-id="5b74e-130">The following example function, `EnableBlurBehind`, illustrates how to apply the blur-behind effect to the whole window.</span></span>


```
HRESULT EnableBlurBehind(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Create and populate the blur-behind structure.
    DWM_BLURBEHIND bb = {0};

    // Specify blur-behind and blur region.
    bb.dwFlags = DWM_BB_ENABLE;
    bb.fEnable = true;
    bb.hRgnBlur = NULL;

    // Enable blur-behind.
    hr = DwmEnableBlurBehindWindow(hwnd, &bb);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



<span data-ttu-id="5b74e-131">Notez que la **valeur null** est spécifiée dans le paramètre *hRgnBlur* .</span><span class="sxs-lookup"><span data-stu-id="5b74e-131">Note that **NULL** is specified in the *hRgnBlur* parameter.</span></span> <span data-ttu-id="5b74e-132">Cela indique au DWM d’appliquer le flou derrière la fenêtre entière.</span><span class="sxs-lookup"><span data-stu-id="5b74e-132">This tells the DWM to apply the blur behind the whole window.</span></span>

<span data-ttu-id="5b74e-133">L’image suivante illustre l’effet de flou-behind appliqué à la fenêtre entière.</span><span class="sxs-lookup"><span data-stu-id="5b74e-133">The following image illustrates the blur-behind effect applied to the whole window.</span></span>

![effet Flou-behind appliqué à une fenêtre](images/dwm-blurbehindwindow.png)

<span data-ttu-id="5b74e-135">Pour appliquer le flou derrière une sous-région, appliquez un handle de région valide (HRGN) au membre **hRgnBlur** de la structure [**DWM \_ BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) et ajoutez l’indicateur **DWM \_ BB \_ BLURREGION** au membre **dwFlags** .</span><span class="sxs-lookup"><span data-stu-id="5b74e-135">To apply the blur behind a subregion, apply a valid region handle (HRGN) to the **hRgnBlur** member of the [**DWM\_BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) structure and add the **DWM\_BB\_BLURREGION** flag to the **dwFlags** member.</span></span>

<span data-ttu-id="5b74e-136">Lorsque vous appliquez l’effet Flou-arrière à une sous-région de la fenêtre, le canal alpha de la fenêtre est utilisé pour la zone non floue.</span><span class="sxs-lookup"><span data-stu-id="5b74e-136">When you apply the blur-behind effect to a subregion of the window, the alpha channel of the window is used for the nonblurred area.</span></span> <span data-ttu-id="5b74e-137">Cela peut provoquer une transparence inattendue dans la région non floue d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5b74e-137">This can cause an unexpected transparency in the nonblurred region of a window.</span></span> <span data-ttu-id="5b74e-138">Par conséquent, soyez vigilant lorsque vous appliquez un effet de flou à une sous-région.</span><span class="sxs-lookup"><span data-stu-id="5b74e-138">Therefore, be careful when you apply a blur effect to a subregion.</span></span>

## <a name="extending-the-window-frame-into-the-client-area"></a><span data-ttu-id="5b74e-139">Extension du frame de fenêtre dans la zone cliente</span><span class="sxs-lookup"><span data-stu-id="5b74e-139">Extending the Window Frame into the Client Area</span></span>

<span data-ttu-id="5b74e-140">Une application peut étendre le flou du frame de fenêtre dans la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="5b74e-140">An application can extend the blur of the window frame into the client area.</span></span> <span data-ttu-id="5b74e-141">Cela est utile lorsque vous appliquez l’effet de flou derrière une fenêtre avec une barre d’outils ancrée ou séparez visuellement les contrôles du reste d’une application.</span><span class="sxs-lookup"><span data-stu-id="5b74e-141">This is useful when you apply the blur effect behind a window with a docked toolbar or visually separate controls from the rest of an application.</span></span> <span data-ttu-id="5b74e-142">Cette fonctionnalité est exposée par la fonction [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) .</span><span class="sxs-lookup"><span data-stu-id="5b74e-142">This functionality is exposed by the [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) function.</span></span>

<span data-ttu-id="5b74e-143">Pour activer le flou à l’aide de [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea), utilisez la structure [**Margins**](/windows/win32/api/uxtheme/ns-uxtheme-margins) pour indiquer la quantité à étendre dans la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="5b74e-143">To enable blur by using [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea), use the [**MARGINS**](/windows/win32/api/uxtheme/ns-uxtheme-margins) structure to indicate how much to extend into the client area.</span></span> <span data-ttu-id="5b74e-144">L’exemple de fonction suivant, `ExtendIntoClientBottom` , active ou désactive l’extension floue en bas du frame non client dans la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="5b74e-144">The following example function, `ExtendIntoClientBottom`, toggles the blur extension on the bottom of the non-client frame into the client area.</span></span>


```
HRESULT ExtendIntoClientBottom(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Set the margins, extending the bottom margin.
    MARGINS margins = {0,0,0,25};

    // Extend the frame on the bottom of the client area.
    hr = DwmExtendFrameIntoClientArea(hwnd,&margins);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



<span data-ttu-id="5b74e-145">L’image suivante illustre l’effet de flou-behind étendu dans le bas de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="5b74e-145">The following image illustrates the blur-behind effect extended into the bottom of the client area.</span></span>

![image qui montre l’effet de flou-behind étendu au bas d’une zone cliente](images/dwm-extendedbottom.png)

<span data-ttu-id="5b74e-147">Également disponible par le biais de la méthode [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) , il s’agit de l’effet « feuille de verre », où l’effet de flou est appliqué à la surface entière de la fenêtre sans bordure visible de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5b74e-147">Also available through the [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) method is the "sheet of glass" effect, where the blur effect is applied to the whole surface of the window without a visible window border.</span></span> <span data-ttu-id="5b74e-148">L’exemple suivant illustre cet effet lorsque la zone cliente est rendue sans bordure de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5b74e-148">The following example demonstrates this effect where the client area is rendered without a window border.</span></span>


```
HRESULT ExtendIntoClientAll(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Negative margins have special meaning to DwmExtendFrameIntoClientArea.
    // Negative margins create the "sheet of glass" effect, where the client 
    // area is rendered as a solid surface without a window border.
    MARGINS margins = {-1};

    // Extend the frame across the whole window.
    hr = DwmExtendFrameIntoClientArea(hwnd,&margins);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



<span data-ttu-id="5b74e-149">L’image suivante illustre le flou-en arrière-plan dans le style de fenêtre « feuille de verre ».</span><span class="sxs-lookup"><span data-stu-id="5b74e-149">The following image illustrates the blur-behind in the "sheet of glass" window style.</span></span>

![image illustrant l’effet de flou-arrière dans le style de fenêtre « feuille de verre »](images/dwm-sheetofglass.png)

## <a name="related-topics"></a><span data-ttu-id="5b74e-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5b74e-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b74e-152">Vue d’ensemble du Gestionnaire de fenêtres du Bureau</span><span class="sxs-lookup"><span data-stu-id="5b74e-152">Desktop Window Manager Overview</span></span>](dwm-overview.md)
</dt> <dt>

[<span data-ttu-id="5b74e-153">Activer et contrôler la composition du Gestionnaire de fenêtrage</span><span class="sxs-lookup"><span data-stu-id="5b74e-153">Enable and Control DWM Composition</span></span>](composition-ovw.md)
</dt> <dt>

[<span data-ttu-id="5b74e-154">Considérations sur les performances et meilleures pratiques</span><span class="sxs-lookup"><span data-stu-id="5b74e-154">Performance Considerations and Best Practices</span></span>](bestpractices-ovw.md)
</dt> </dl>

 

 
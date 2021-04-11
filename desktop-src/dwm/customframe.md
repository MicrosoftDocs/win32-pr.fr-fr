---
title: Frame de fenêtre personnalisé à l’aide de DWM
description: Cette rubrique montre comment utiliser les API Gestionnaire de fenêtrage (DWM) pour créer des frames de fenêtre personnalisés pour votre application.
ms.assetid: 7f7dc902-40d3-44e9-adc2-05a39c634eb3
keywords:
- Gestionnaire de fenêtrage (DWM), frames de fenêtre personnalisés
- DWM (Gestionnaire de fenêtrage), frames de fenêtre personnalisés
- frames de fenêtre personnalisés
- suppression des frames standard
- extension des frames client
- Gestionnaire de fenêtrage (DWM), extension des frames client
- DWM (Gestionnaire de fenêtrage), étendre des frames client
- Gestionnaire de fenêtrage (DWM), suppression des frames standard
- DWM (Gestionnaire de fenêtrage), suppression des frames standard
- Gestionnaire de fenêtrage (DWM), dessin dans des frames étendus
- DWM (Gestionnaire de fenêtrage), dessin dans des frames étendus
- dessiner dans des frames étendus
- test des accès
- Gestionnaire de fenêtrage (DWM), test de positionnement
- DWM (Gestionnaire de fenêtrage), test de positionnement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a27a9b71dd2dd91cb000a352ef039de2a71cd9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031825"
---
# <a name="custom-window-frame-using-dwm"></a><span data-ttu-id="84e9e-118">Frame de fenêtre personnalisé à l’aide de DWM</span><span class="sxs-lookup"><span data-stu-id="84e9e-118">Custom Window Frame Using DWM</span></span>

<span data-ttu-id="84e9e-119">Cette rubrique montre comment utiliser les API Gestionnaire de fenêtrage (DWM) pour créer des frames de fenêtre personnalisés pour votre application.</span><span class="sxs-lookup"><span data-stu-id="84e9e-119">This topic demonstrates how to use the Desktop Window Manager (DWM) APIs to create custom window frames for your application.</span></span>

-   [<span data-ttu-id="84e9e-120">Introduction</span><span class="sxs-lookup"><span data-stu-id="84e9e-120">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="84e9e-121">Extension du frame client</span><span class="sxs-lookup"><span data-stu-id="84e9e-121">Extending the Client Frame</span></span>](#extending-the-client-frame)
-   [<span data-ttu-id="84e9e-122">Suppression du frame standard</span><span class="sxs-lookup"><span data-stu-id="84e9e-122">Removing the Standard Frame</span></span>](#removing-the-standard-frame)
-   [<span data-ttu-id="84e9e-123">Dessin dans la fenêtre frame étendue</span><span class="sxs-lookup"><span data-stu-id="84e9e-123">Drawing in the Extended Frame Window</span></span>](#drawing-in-the-extended-frame-window)
-   [<span data-ttu-id="84e9e-124">Activation du test de positionnement pour le frame personnalisé</span><span class="sxs-lookup"><span data-stu-id="84e9e-124">Enabling Hit Testing for the Custom Frame</span></span>](#enabling-hit-testing-for-the-custom-frame)
-   [<span data-ttu-id="84e9e-125">Annexe A : exemple de procédure de fenêtre</span><span class="sxs-lookup"><span data-stu-id="84e9e-125">Appendix A: Sample Window Procedure</span></span>](#appendix-a-sample-window-procedure)
-   [<span data-ttu-id="84e9e-126">Annexe B : peinture du titre de la légende</span><span class="sxs-lookup"><span data-stu-id="84e9e-126">Appendix B: Painting the Caption Title</span></span>](#appendix-b-painting-the-caption-title)
-   [<span data-ttu-id="84e9e-127">Annexe C : fonction HitTestNCA</span><span class="sxs-lookup"><span data-stu-id="84e9e-127">Appendix C: HitTestNCA Function</span></span>](#appendix-c-hittestnca-function)
-   [<span data-ttu-id="84e9e-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="84e9e-128">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="84e9e-129">Introduction</span><span class="sxs-lookup"><span data-stu-id="84e9e-129">Introduction</span></span>

<span data-ttu-id="84e9e-130">Dans Windows Vista et versions ultérieures, l’apparence des zones non clientes des fenêtres d’application (la barre de titre, l’icône, la bordure de la fenêtre et les boutons de légende) est contrôlée par le DWM.</span><span class="sxs-lookup"><span data-stu-id="84e9e-130">In Windows Vista and later, the appearance of the non-client areas of application windows (the title bar, icon, window border, and caption buttons) is controlled by the DWM.</span></span> <span data-ttu-id="84e9e-131">À l’aide des API DWM, vous pouvez modifier la façon dont le DWM restitue le frame d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="84e9e-131">Using the DWM APIs, you can change the way the DWM renders a window's frame.</span></span>

<span data-ttu-id="84e9e-132">L’une des fonctionnalités des API DWM est la possibilité d’étendre le frame d’application dans la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="84e9e-132">One feature of the DWM APIs is the ability to extend the application frame into the client area.</span></span> <span data-ttu-id="84e9e-133">Cela vous permet d’intégrer un élément d’interface utilisateur client, tel qu’une barre d’outils, dans le frame, en donnant à l’interface utilisateur des contrôles un emplacement plus important dans l’interface utilisateur de l’application.</span><span class="sxs-lookup"><span data-stu-id="84e9e-133">This enables you to integrate a client UI element—such as a toolbar—into the frame, giving the UI controls a more prominent place in the application UI.</span></span> <span data-ttu-id="84e9e-134">Par exemple, Windows Internet Explorer 7 sur Windows Vista intègre la barre de navigation dans le frame de fenêtre en étendant le haut du cadre comme indiqué dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="84e9e-134">For example, Windows Internet Explorer 7 on Windows Vista integrates the navigation bar into the window frame by extending the top of the frame as shown in the following screen shot.</span></span>

![barre de navigation intégrée dans le frame de fenêtre.](images/ie7-extendedborder-boxed.png)

<span data-ttu-id="84e9e-136">La possibilité d’étendre le frame de la fenêtre vous permet également de créer des frames personnalisés tout en conservant l’apparence de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="84e9e-136">The ability to extend the window frame also enables you to create custom frames while maintaining the window's look and feel.</span></span> <span data-ttu-id="84e9e-137">Par exemple, Microsoft Office Word 2007 dessine le bouton Office et la barre d’outils accès rapide dans le cadre personnalisé tout en fournissant les boutons standard réduire, agrandir et fermer la légende, comme illustré dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="84e9e-137">For example, Microsoft Office Word 2007 draws the Office button and the Quick Access toolbar inside the custom frame while providing the standard Minimize, Maximize, and Close caption buttons, as shown in the following screen shot.</span></span>

![bouton Office et barre d’outils accès rapide dans Word 2007](images/word2007-customborder-boxed.png)

## <a name="extending-the-client-frame"></a><span data-ttu-id="84e9e-139">Extension du frame client</span><span class="sxs-lookup"><span data-stu-id="84e9e-139">Extending the Client Frame</span></span>

<span data-ttu-id="84e9e-140">La fonctionnalité d’extension du frame dans la zone cliente est exposée par la fonction [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) .</span><span class="sxs-lookup"><span data-stu-id="84e9e-140">The functionality to extend the frame into the client area is exposed by the [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) function.</span></span> <span data-ttu-id="84e9e-141">Pour étendre le frame, transmettez le descripteur de la fenêtre cible avec les valeurs de marge intérieure à **DwmExtendFrameIntoClientArea**.</span><span class="sxs-lookup"><span data-stu-id="84e9e-141">To extend the frame, pass the handle of the target window together with the margin inset values to **DwmExtendFrameIntoClientArea**.</span></span> <span data-ttu-id="84e9e-142">Les valeurs d’incrustation de marge déterminent la distance d’extension du cadre sur les quatre côtés de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="84e9e-142">The margin inset values determine how far to extend the frame on the four sides of the window.</span></span>

<span data-ttu-id="84e9e-143">Le code suivant illustre l’utilisation de [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) pour étendre le frame.</span><span class="sxs-lookup"><span data-stu-id="84e9e-143">The following code demonstrates the use of [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) to extend the frame.</span></span>


```
// Handle the window activation.
if (message == WM_ACTIVATE)
{
    // Extend the frame into the client area.
    MARGINS margins;

    margins.cxLeftWidth = LEFTEXTENDWIDTH;      // 8
    margins.cxRightWidth = RIGHTEXTENDWIDTH;    // 8
    margins.cyBottomHeight = BOTTOMEXTENDWIDTH; // 20
    margins.cyTopHeight = TOPEXTENDWIDTH;       // 27

    hr = DwmExtendFrameIntoClientArea(hWnd, &margins);

    if (!SUCCEEDED(hr))
    {
        // Handle the error.
    }

    fCallDWP = true;
    lRet = 0;
}
```



<span data-ttu-id="84e9e-144">Notez que l’extension de cadre est effectuée dans le message [**WM \_ Activate**](/windows/desktop/inputdev/wm-activate) et non dans le message [**WM \_ Create**](/windows/desktop/winmsg/wm-create) .</span><span class="sxs-lookup"><span data-stu-id="84e9e-144">Note that the frame extension is done within the [**WM\_ACTIVATE**](/windows/desktop/inputdev/wm-activate) message rather than the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message.</span></span> <span data-ttu-id="84e9e-145">Cela garantit que l’extension de frame est gérée correctement quand la fenêtre est à sa taille par défaut et quand elle est agrandie.</span><span class="sxs-lookup"><span data-stu-id="84e9e-145">This ensures that frame extension is handled properly when the window is at its default size and when it is maximized.</span></span>

<span data-ttu-id="84e9e-146">L’illustration suivante montre un cadre de fenêtre standard (à gauche) et le même cadre de fenêtre étendu (à droite).</span><span class="sxs-lookup"><span data-stu-id="84e9e-146">The following image shows a standard window frame (on the left) and the same window frame extended (on the right).</span></span> <span data-ttu-id="84e9e-147">Le frame est étendu à l’aide de l’exemple de code précédent et de l’arrière-plan Microsoft Visual Studio [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) / [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) par défaut ( \_ fenêtre couleur + 1).</span><span class="sxs-lookup"><span data-stu-id="84e9e-147">The frame is extended using the previous code example and the default Microsoft Visual Studio [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)/[**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) background (COLOR\_WINDOW +1).</span></span>

![capture d’écran d’un cadre standard (gauche) et étendu (à droite) avec arrière-plan blanc](images/white-sidebyside.png)

<span data-ttu-id="84e9e-149">La différence visuelle entre ces deux fenêtres est très subtile.</span><span class="sxs-lookup"><span data-stu-id="84e9e-149">The visual difference between these two windows is very subtle.</span></span> <span data-ttu-id="84e9e-150">La seule différence entre les deux est que la bordure noire fine de la région du client dans la fenêtre de gauche est absente de la fenêtre de droite.</span><span class="sxs-lookup"><span data-stu-id="84e9e-150">The only difference between the two is that the thin black line border of the client region in the window on the left is missing from the window on the right.</span></span> <span data-ttu-id="84e9e-151">La raison de cette bordure manquante est qu’elle est incorporée dans le frame étendu, mais que le reste de la zone cliente ne l’est pas.</span><span class="sxs-lookup"><span data-stu-id="84e9e-151">The reason for this missing border is that it is incorporated into the extended frame, but the rest of the client area is not.</span></span> <span data-ttu-id="84e9e-152">Pour que les frames étendus soient visibles, les régions sous-jacentes de chaque côté du cadre étendu doivent avoir des données de pixels avec une valeur alpha de 0.</span><span class="sxs-lookup"><span data-stu-id="84e9e-152">For the extended frames to be visible, the regions underlying each of the extended frame's sides must have pixel data with an alpha value of 0.</span></span> <span data-ttu-id="84e9e-153">La bordure noire autour de la région du client contient des données de pixels dans lesquelles toutes les valeurs de couleur (rouge, vert, bleu et alpha) sont définies sur 0.</span><span class="sxs-lookup"><span data-stu-id="84e9e-153">The black border around the client region has pixel data in which all color values (red, green, blue, and alpha) are set to 0.</span></span> <span data-ttu-id="84e9e-154">Le reste de l’arrière-plan n’a pas la valeur alpha définie sur 0, donc le reste du frame étendu n’est pas visible.</span><span class="sxs-lookup"><span data-stu-id="84e9e-154">The rest of the background does not have the alpha value set to 0, so the rest of the extended frame is not visible.</span></span>

<span data-ttu-id="84e9e-155">Le moyen le plus simple de s’assurer que les frames étendus sont visibles consiste à peindre l’ensemble de la région cliente en noir.</span><span class="sxs-lookup"><span data-stu-id="84e9e-155">The easiest way to ensure that the extended frames are visible is to paint the entire client region black.</span></span> <span data-ttu-id="84e9e-156">Pour ce faire, initialisez le membre *hbrBackground* de votre structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) ou [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) sur le handle du pinceau noir de stock \_ .</span><span class="sxs-lookup"><span data-stu-id="84e9e-156">To accomplish this, initialize the *hbrBackground* member of your [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) or [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) structure to the handle of the stock BLACK\_BRUSH.</span></span> <span data-ttu-id="84e9e-157">L’illustration suivante montre le même frame standard (à gauche) et le même cadre étendu (à droite).</span><span class="sxs-lookup"><span data-stu-id="84e9e-157">The following image shows the same standard frame (left) and extended frame (right) shown previously.</span></span> <span data-ttu-id="84e9e-158">Cette fois, cependant, *hbrBackground* est défini sur la \_ poignée du pinceau noir obtenue à partir de la fonction [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) .</span><span class="sxs-lookup"><span data-stu-id="84e9e-158">This time, however, *hbrBackground* is set to the BLACK\_BRUSH handle obtained from the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) function.</span></span>

![capture d’écran d’un bloc standard (à gauche) et étendu (à droite) avec arrière-plan noir](images/standard-extended-sidebyside.png)

## <a name="removing-the-standard-frame"></a><span data-ttu-id="84e9e-160">Suppression du frame standard</span><span class="sxs-lookup"><span data-stu-id="84e9e-160">Removing the Standard Frame</span></span>

<span data-ttu-id="84e9e-161">Une fois que vous avez étendu le frame de votre application et que vous l’avez rendu visible, vous pouvez supprimer le cadre standard.</span><span class="sxs-lookup"><span data-stu-id="84e9e-161">After you have extended the frame of your application and made it visible, you can remove the standard frame.</span></span> <span data-ttu-id="84e9e-162">La suppression du frame standard vous permet de contrôler la largeur de chaque côté du cadre plutôt que d’étendre simplement le cadre standard.</span><span class="sxs-lookup"><span data-stu-id="84e9e-162">Removing the standard frame enables you to control the width of each side of the frame rather than simply extending the standard frame.</span></span>

<span data-ttu-id="84e9e-163">Pour supprimer le frame de fenêtre standard, vous devez gérer le message [**WM \_ NCCALCSIZE**](/windows/desktop/winmsg/wm-nccalcsize) , en particulier lorsque sa valeur *wParam* est **true** et que la valeur de retour est 0.</span><span class="sxs-lookup"><span data-stu-id="84e9e-163">To remove the standard window frame, you must handle the [**WM\_NCCALCSIZE**](/windows/desktop/winmsg/wm-nccalcsize) message, specifically when its *wParam* value is **TRUE** and the return value is 0.</span></span> <span data-ttu-id="84e9e-164">En procédant ainsi, votre application utilise la zone de fenêtre entière comme zone cliente, en supprimant le frame standard.</span><span class="sxs-lookup"><span data-stu-id="84e9e-164">By doing so, your application uses the entire window region as the client area, removing the standard frame.</span></span>

<span data-ttu-id="84e9e-165">Les résultats de la gestion du message [**WM \_ NCCALCSIZE**](/windows/desktop/winmsg/wm-nccalcsize) ne sont pas visibles tant que la région du client n’a pas besoin d’être redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="84e9e-165">The results of handling the [**WM\_NCCALCSIZE**](/windows/desktop/winmsg/wm-nccalcsize) message are not visible until the client region needs to be resized.</span></span> <span data-ttu-id="84e9e-166">Jusqu’à ce moment-là, la vue initiale de la fenêtre apparaît avec le frame standard et les bordures étendues.</span><span class="sxs-lookup"><span data-stu-id="84e9e-166">Until that time, the initial view of the window appears with the standard frame and extended borders.</span></span> <span data-ttu-id="84e9e-167">Pour remédier à cela, vous devez redimensionner votre fenêtre ou exécuter une action qui initie un message **WM \_ NCCALCSIZE** au moment de la création de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="84e9e-167">To overcome this, you must either resize your window or perform an action that initiates a **WM\_NCCALCSIZE** message at the time of window creation.</span></span> <span data-ttu-id="84e9e-168">Pour ce faire, vous pouvez utiliser la fonction [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) pour déplacer votre fenêtre et la redimensionner.</span><span class="sxs-lookup"><span data-stu-id="84e9e-168">This can be accomplished by using the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function to move your window and resize it.</span></span> <span data-ttu-id="84e9e-169">Le code suivant illustre un appel à **SetWindowPos** qui force l’envoi d’un message **WM \_ NCCALCSIZE** à l’aide des attributs du rectangle de la fenêtre active et de l' \_ indicateur de FRAMECHANGED SWP.</span><span class="sxs-lookup"><span data-stu-id="84e9e-169">The following code demonstrates a call to **SetWindowPos** that forces a **WM\_NCCALCSIZE** message to be sent using the current window rectangle attributes and the SWP\_FRAMECHANGED flag.</span></span>


```
// Handle window creation.
if (message == WM_CREATE)
{
    RECT rcClient;
    GetWindowRect(hWnd, &rcClient);

    // Inform the application of the frame change.
    SetWindowPos(hWnd, 
                 NULL, 
                 rcClient.left, rcClient.top,
                 RECTWIDTH(rcClient), RECTHEIGHT(rcClient),
                 SWP_FRAMECHANGED);

    fCallDWP = true;
    lRet = 0;
}
```



<span data-ttu-id="84e9e-170">L’illustration suivante montre le cadre standard (à gauche) et le cadre nouvellement étendu sans le cadre standard (à droite).</span><span class="sxs-lookup"><span data-stu-id="84e9e-170">The following image shows the standard frame (left) and the newly extended frame without the standard frame (right).</span></span>

![capture d’écran d’un cadre standard (à gauche) et d’un cadre personnalisé (à droite)](images/standard-custom-sidebyside.png)

## <a name="drawing-in-the-extended-frame-window"></a><span data-ttu-id="84e9e-172">Dessin dans la fenêtre frame étendue</span><span class="sxs-lookup"><span data-stu-id="84e9e-172">Drawing in the Extended Frame Window</span></span>

<span data-ttu-id="84e9e-173">En supprimant le cadre standard, vous perdez le dessin automatique de l’icône et du titre de l’application.</span><span class="sxs-lookup"><span data-stu-id="84e9e-173">By removing the standard frame, you lose the automatic drawing of the application icon and title.</span></span> <span data-ttu-id="84e9e-174">Pour rajouter ces éléments à votre application, vous devez les dessiner vous-même.</span><span class="sxs-lookup"><span data-stu-id="84e9e-174">To add these back to your application, you must draw them yourself.</span></span> <span data-ttu-id="84e9e-175">Pour ce faire, examinez d’abord les modifications qui se sont produites dans votre zone cliente.</span><span class="sxs-lookup"><span data-stu-id="84e9e-175">To do this, first look at the change that has occurred to your client area.</span></span>

<span data-ttu-id="84e9e-176">Avec la suppression du frame standard, votre zone cliente se compose désormais de la totalité de la fenêtre, y compris le cadre étendu.</span><span class="sxs-lookup"><span data-stu-id="84e9e-176">With the removal of the standard frame, your client area now consists of the entire window, including the extended frame.</span></span> <span data-ttu-id="84e9e-177">Cela comprend la région dans laquelle les boutons de légende sont dessinés.</span><span class="sxs-lookup"><span data-stu-id="84e9e-177">This includes the region where the caption buttons are drawn.</span></span> <span data-ttu-id="84e9e-178">Dans la comparaison côte à côte suivante, la zone cliente pour le frame standard et le frame étendu personnalisé est mise en surbrillance en rouge.</span><span class="sxs-lookup"><span data-stu-id="84e9e-178">In the following side-by-side comparison, the client area for both the standard frame and the custom extended frame is highlighted in red.</span></span> <span data-ttu-id="84e9e-179">La zone cliente de la fenêtre frame standard (à gauche) est la région noire.</span><span class="sxs-lookup"><span data-stu-id="84e9e-179">The client area for the standard frame window (left) is the black region.</span></span> <span data-ttu-id="84e9e-180">Dans la fenêtre frame étendue (à droite), la zone cliente est la fenêtre entière.</span><span class="sxs-lookup"><span data-stu-id="84e9e-180">On the extended frame window (right), the client area is the entire window.</span></span>

![capture d’écran des zones clientes en rouge en surbrillance dans le frame standard et personnalisé](images/clientarea-sidebyside.png)

<span data-ttu-id="84e9e-182">Étant donné que la totalité de la fenêtre est votre zone cliente, vous pouvez simplement dessiner ce que vous souhaitez dans le frame étendu.</span><span class="sxs-lookup"><span data-stu-id="84e9e-182">Because the entire window is your client area, you can simply draw what you want in the extended frame.</span></span> <span data-ttu-id="84e9e-183">Pour ajouter un titre à votre application, il vous suffit de dessiner du texte dans la région appropriée.</span><span class="sxs-lookup"><span data-stu-id="84e9e-183">To add a title to your application, just draw text in the appropriate region.</span></span> <span data-ttu-id="84e9e-184">L’illustration suivante montre le texte à thème dessiné sur le cadre de légende personnalisé.</span><span class="sxs-lookup"><span data-stu-id="84e9e-184">The following image shows themed text drawn on the custom caption frame.</span></span> <span data-ttu-id="84e9e-185">Le titre est dessiné à l’aide de la fonction [**DrawThemeTextEx**](/windows/win32/api/uxtheme/nf-uxtheme-drawthemetextex) .</span><span class="sxs-lookup"><span data-stu-id="84e9e-185">The title is drawn using the [**DrawThemeTextEx**](/windows/win32/api/uxtheme/nf-uxtheme-drawthemetextex) function.</span></span> <span data-ttu-id="84e9e-186">Pour afficher le code qui peint le titre, consultez l' [annexe B : peinture du titre de la légende](#appendix-b-painting-the-caption-title).</span><span class="sxs-lookup"><span data-stu-id="84e9e-186">To view the code that paints the title, see [Appendix B: Painting the Caption Title](#appendix-b-painting-the-caption-title).</span></span>

![capture d’écran d’un cadre personnalisé avec titre](images/custom-caption-title.png)

> [!Note]  
> <span data-ttu-id="84e9e-188">Quand vous dessinez dans votre Frame personnalisé, soyez prudent lorsque vous placez des contrôles d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="84e9e-188">When drawing in your custom frame, be careful when placing UI controls.</span></span> <span data-ttu-id="84e9e-189">Étant donné que la totalité de la fenêtre est votre région cliente, vous devez ajuster le placement de votre contrôle d’interface utilisateur pour chaque largeur d’image si vous ne souhaitez pas qu’elles apparaissent sur ou dans le frame étendu.</span><span class="sxs-lookup"><span data-stu-id="84e9e-189">Because the entire window is your client region, you must adjust your UI control placement for each frame width if you do not want them to appear on or in the extended frame.</span></span>

 

## <a name="enabling-hit-testing-for-the-custom-frame"></a><span data-ttu-id="84e9e-190">Activation du test de positionnement pour le frame personnalisé</span><span class="sxs-lookup"><span data-stu-id="84e9e-190">Enabling Hit Testing for the Custom Frame</span></span>

<span data-ttu-id="84e9e-191">L’un des effets secondaires de la suppression du frame standard est la perte du comportement de redimensionnement et de déplacement par défaut.</span><span class="sxs-lookup"><span data-stu-id="84e9e-191">A side effect of removing the standard frame is the loss of the default resizing and moving behavior.</span></span> <span data-ttu-id="84e9e-192">Pour que votre application puisse émuler correctement le comportement de fenêtre standard, vous devez implémenter une logique pour gérer le test de positionnement de bouton de légende et le redimensionnement/déplacement de frame.</span><span class="sxs-lookup"><span data-stu-id="84e9e-192">For your application to properly emulate standard window behavior, you will need to implement logic to handle caption button hit testing and frame resizing/moving.</span></span>

<span data-ttu-id="84e9e-193">Pour le test de positionnement des boutons de légende, DWM fournit la fonction [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) .</span><span class="sxs-lookup"><span data-stu-id="84e9e-193">For caption button hit testing, DWM provides the [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) function.</span></span> <span data-ttu-id="84e9e-194">Pour tester correctement les boutons de légende dans les scénarios de frame personnalisé, les messages doivent d’abord être transmis à **DwmDefWindowProc** pour être géré.</span><span class="sxs-lookup"><span data-stu-id="84e9e-194">To properly hit test the caption buttons in custom frame scenarios, messages should first be passed to **DwmDefWindowProc** for handling.</span></span> <span data-ttu-id="84e9e-195">**DwmDefWindowProc** retourne la **valeur true** si un message est géré et **false** si ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="84e9e-195">**DwmDefWindowProc** returns **TRUE** if a message is handled and **FALSE** if it is not.</span></span> <span data-ttu-id="84e9e-196">Si le message n’est pas géré par **DwmDefWindowProc**, votre application doit gérer le message lui-même ou passer le message sur [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="84e9e-196">If the message is not handled by **DwmDefWindowProc**, your application should handle the message itself or pass the message onto [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="84e9e-197">Pour le redimensionnement et le déplacement de frame, votre application doit fournir la logique de test de positionnement et gérer les messages de test de positionnement de frame.</span><span class="sxs-lookup"><span data-stu-id="84e9e-197">For frame resizing and moving, your application must provide the hit testing logic and handle frame hit test messages.</span></span> <span data-ttu-id="84e9e-198">Les messages de test de positionnement de frame sont envoyés via le message [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) , même si votre application crée un frame personnalisé sans le frame standard.</span><span class="sxs-lookup"><span data-stu-id="84e9e-198">Frame hit test messages are sent to you through the [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) message, even if your application creates a custom frame without the standard frame.</span></span> <span data-ttu-id="84e9e-199">Le code suivant illustre la gestion du message **WM \_ NCHITTEST** lorsque [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) ne le gère pas.</span><span class="sxs-lookup"><span data-stu-id="84e9e-199">The following code demonstrates handling the **WM\_NCHITTEST** message when [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) does not handle it.</span></span> <span data-ttu-id="84e9e-200">Pour afficher le code de la `HitTestNCA` fonction appelée, consultez l' [annexe C : fonction HitTestNCA](#appendix-c-hittestnca-function).</span><span class="sxs-lookup"><span data-stu-id="84e9e-200">To see the code of the called `HitTestNCA` function, see [Appendix C: HitTestNCA Function](#appendix-c-hittestnca-function).</span></span>


```
// Handle hit testing in the NCA if not handled by DwmDefWindowProc.
if ((message == WM_NCHITTEST) && (lRet == 0))
{
    lRet = HitTestNCA(hWnd, wParam, lParam);

    if (lRet != HTNOWHERE)
    {
        fCallDWP = false;
    }
}
```



## <a name="appendix-a-sample-window-procedure"></a><span data-ttu-id="84e9e-201">Annexe A : exemple de procédure de fenêtre</span><span class="sxs-lookup"><span data-stu-id="84e9e-201">Appendix A: Sample Window Procedure</span></span>

<span data-ttu-id="84e9e-202">L’exemple de code suivant illustre une procédure de fenêtre et ses fonctions de travail de prise en charge utilisées pour créer une application Frame personnalisée.</span><span class="sxs-lookup"><span data-stu-id="84e9e-202">The following code sample demonstrates a window procedure and its supporting worker functions used to create a custom frame application.</span></span>


```
//
//  Main WinProc.
//
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    bool fCallDWP = true;
    BOOL fDwmEnabled = FALSE;
    LRESULT lRet = 0;
    HRESULT hr = S_OK;

    // Winproc worker for custom frame issues.
    hr = DwmIsCompositionEnabled(&fDwmEnabled);
    if (SUCCEEDED(hr))
    {
        lRet = CustomCaptionProc(hWnd, message, wParam, lParam, &fCallDWP);
    }

    // Winproc worker for the rest of the application.
    if (fCallDWP)
    {
        lRet = AppWinProc(hWnd, message, wParam, lParam);
    }
    return lRet;
}

//
// Message handler for handling the custom caption messages.
//
LRESULT CustomCaptionProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam, bool* pfCallDWP)
{
    LRESULT lRet = 0;
    HRESULT hr = S_OK;
    bool fCallDWP = true; // Pass on to DefWindowProc?

    fCallDWP = !DwmDefWindowProc(hWnd, message, wParam, lParam, &lRet);

    // Handle window creation.
    if (message == WM_CREATE)
    {
        RECT rcClient;
        GetWindowRect(hWnd, &rcClient);

        // Inform application of the frame change.
        SetWindowPos(hWnd, 
                     NULL, 
                     rcClient.left, rcClient.top,
                     RECTWIDTH(rcClient), RECTHEIGHT(rcClient),
                     SWP_FRAMECHANGED);

        fCallDWP = true;
        lRet = 0;
    }

    // Handle window activation.
    if (message == WM_ACTIVATE)
    {
        // Extend the frame into the client area.
        MARGINS margins;

        margins.cxLeftWidth = LEFTEXTENDWIDTH;      // 8
        margins.cxRightWidth = RIGHTEXTENDWIDTH;    // 8
        margins.cyBottomHeight = BOTTOMEXTENDWIDTH; // 20
        margins.cyTopHeight = TOPEXTENDWIDTH;       // 27

        hr = DwmExtendFrameIntoClientArea(hWnd, &margins);

        if (!SUCCEEDED(hr))
        {
            // Handle error.
        }

        fCallDWP = true;
        lRet = 0;
    }

    if (message == WM_PAINT)
    {
        HDC hdc;
        {
            PAINTSTRUCT ps;
            hdc = BeginPaint(hWnd, &ps);
            PaintCustomCaption(hWnd, hdc);
            EndPaint(hWnd, &ps);
        }

        fCallDWP = true;
        lRet = 0;
    }

    // Handle the non-client size message.
    if ((message == WM_NCCALCSIZE) && (wParam == TRUE))
    {
        // Calculate new NCCALCSIZE_PARAMS based on custom NCA inset.
        NCCALCSIZE_PARAMS *pncsp = reinterpret_cast<NCCALCSIZE_PARAMS*>(lParam);

        pncsp->rgrc[0].left   = pncsp->rgrc[0].left   + 0;
        pncsp->rgrc[0].top    = pncsp->rgrc[0].top    + 0;
        pncsp->rgrc[0].right  = pncsp->rgrc[0].right  - 0;
        pncsp->rgrc[0].bottom = pncsp->rgrc[0].bottom - 0;

        lRet = 0;
        
        // No need to pass the message on to the DefWindowProc.
        fCallDWP = false;
    }

    // Handle hit testing in the NCA if not handled by DwmDefWindowProc.
    if ((message == WM_NCHITTEST) && (lRet == 0))
    {
        lRet = HitTestNCA(hWnd, wParam, lParam);

        if (lRet != HTNOWHERE)
        {
            fCallDWP = false;
        }
    }

    *pfCallDWP = fCallDWP;

    return lRet;
}

//
// Message handler for the application.
//
LRESULT AppWinProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;
    HRESULT hr; 
    LRESULT result = 0;

    switch (message)
    {
        case WM_CREATE:
            {}
            break;
        case WM_COMMAND:
            wmId    = LOWORD(wParam);
            wmEvent = HIWORD(wParam);

            // Parse the menu selections:
            switch (wmId)
            {
                default:
                    return DefWindowProc(hWnd, message, wParam, lParam);
            }
            break;
        case WM_PAINT:
            {
                hdc = BeginPaint(hWnd, &ps);
                PaintCustomCaption(hWnd, hdc);
                
                // Add any drawing code here...
    
                EndPaint(hWnd, &ps);
            }
            break;
        case WM_DESTROY:
            PostQuitMessage(0);
            break;
        default:
            return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



## <a name="appendix-b-painting-the-caption-title"></a><span data-ttu-id="84e9e-203">Annexe B : peinture du titre de la légende</span><span class="sxs-lookup"><span data-stu-id="84e9e-203">Appendix B: Painting the Caption Title</span></span>

<span data-ttu-id="84e9e-204">Le code suivant montre comment peindre un titre de légende sur le frame étendu.</span><span class="sxs-lookup"><span data-stu-id="84e9e-204">The following code demonstrates how to paint a caption title on the extended frame.</span></span> <span data-ttu-id="84e9e-205">Cette fonction doit être appelée à partir des appels [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) et [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) .</span><span class="sxs-lookup"><span data-stu-id="84e9e-205">This function must be called from within the [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) and [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) calls.</span></span>


```
// Paint the title on the custom frame.
void PaintCustomCaption(HWND hWnd, HDC hdc)
{
    RECT rcClient;
    GetClientRect(hWnd, &rcClient);

    HTHEME hTheme = OpenThemeData(NULL, L"CompositedWindow::Window");
    if (hTheme)
    {
        HDC hdcPaint = CreateCompatibleDC(hdc);
        if (hdcPaint)
        {
            int cx = RECTWIDTH(rcClient);
            int cy = RECTHEIGHT(rcClient);

            // Define the BITMAPINFO structure used to draw text.
            // Note that biHeight is negative. This is done because
            // DrawThemeTextEx() needs the bitmap to be in top-to-bottom
            // order.
            BITMAPINFO dib = { 0 };
            dib.bmiHeader.biSize            = sizeof(BITMAPINFOHEADER);
            dib.bmiHeader.biWidth           = cx;
            dib.bmiHeader.biHeight          = -cy;
            dib.bmiHeader.biPlanes          = 1;
            dib.bmiHeader.biBitCount        = BIT_COUNT;
            dib.bmiHeader.biCompression     = BI_RGB;

            HBITMAP hbm = CreateDIBSection(hdc, &dib, DIB_RGB_COLORS, NULL, NULL, 0);
            if (hbm)
            {
                HBITMAP hbmOld = (HBITMAP)SelectObject(hdcPaint, hbm);

                // Setup the theme drawing options.
                DTTOPTS DttOpts = {sizeof(DTTOPTS)};
                DttOpts.dwFlags = DTT_COMPOSITED | DTT_GLOWSIZE;
                DttOpts.iGlowSize = 15;

                // Select a font.
                LOGFONT lgFont;
                HFONT hFontOld = NULL;
                if (SUCCEEDED(GetThemeSysFont(hTheme, TMT_CAPTIONFONT, &lgFont)))
                {
                    HFONT hFont = CreateFontIndirect(&lgFont);
                    hFontOld = (HFONT) SelectObject(hdcPaint, hFont);
                }

                // Draw the title.
                RECT rcPaint = rcClient;
                rcPaint.top += 8;
                rcPaint.right -= 125;
                rcPaint.left += 8;
                rcPaint.bottom = 50;
                DrawThemeTextEx(hTheme, 
                                hdcPaint, 
                                0, 0, 
                                szTitle, 
                                -1, 
                                DT_LEFT | DT_WORD_ELLIPSIS, 
                                &rcPaint, 
                                &DttOpts);

                // Blit text to the frame.
                BitBlt(hdc, 0, 0, cx, cy, hdcPaint, 0, 0, SRCCOPY);

                SelectObject(hdcPaint, hbmOld);
                if (hFontOld)
                {
                    SelectObject(hdcPaint, hFontOld);
                }
                DeleteObject(hbm);
            }
            DeleteDC(hdcPaint);
        }
        CloseThemeData(hTheme);
    }
}
```



## <a name="appendix-c-hittestnca-function"></a><span data-ttu-id="84e9e-206">Annexe C : fonction HitTestNCA</span><span class="sxs-lookup"><span data-stu-id="84e9e-206">Appendix C: HitTestNCA Function</span></span>

<span data-ttu-id="84e9e-207">Le code suivant illustre la `HitTestNCA` fonction utilisée [pour activer le test de positionnement pour le frame personnalisé](#enabling-hit-testing-for-the-custom-frame).</span><span class="sxs-lookup"><span data-stu-id="84e9e-207">The following code shows the `HitTestNCA` function used in [Enabling Hit Testing for the Custom Frame](#enabling-hit-testing-for-the-custom-frame).</span></span> <span data-ttu-id="84e9e-208">Cette fonction gère la logique de test de positionnement pour le [**\_ NCHITTEST WM**](/windows/desktop/inputdev/wm-nchittest) lorsque [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) ne gère pas le message.</span><span class="sxs-lookup"><span data-stu-id="84e9e-208">This function handles the hit testing logic for the [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) when [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) does not handle the message.</span></span>


```
// Hit test the frame for resizing and moving.
LRESULT HitTestNCA(HWND hWnd, WPARAM wParam, LPARAM lParam)
{
    // Get the point coordinates for the hit test.
    POINT ptMouse = { GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam)};

    // Get the window rectangle.
    RECT rcWindow;
    GetWindowRect(hWnd, &rcWindow);

    // Get the frame rectangle, adjusted for the style without a caption.
    RECT rcFrame = { 0 };
    AdjustWindowRectEx(&rcFrame, WS_OVERLAPPEDWINDOW & ~WS_CAPTION, FALSE, NULL);

    // Determine if the hit test is for resizing. Default middle (1,1).
    USHORT uRow = 1;
    USHORT uCol = 1;
    bool fOnResizeBorder = false;

    // Determine if the point is at the top or bottom of the window.
    if (ptMouse.y >= rcWindow.top && ptMouse.y < rcWindow.top + TOPEXTENDWIDTH)
    {
        fOnResizeBorder = (ptMouse.y < (rcWindow.top - rcFrame.top));
        uRow = 0;
    }
    else if (ptMouse.y < rcWindow.bottom && ptMouse.y >= rcWindow.bottom - BOTTOMEXTENDWIDTH)
    {
        uRow = 2;
    }

    // Determine if the point is at the left or right of the window.
    if (ptMouse.x >= rcWindow.left && ptMouse.x < rcWindow.left + LEFTEXTENDWIDTH)
    {
        uCol = 0; // left side
    }
    else if (ptMouse.x < rcWindow.right && ptMouse.x >= rcWindow.right - RIGHTEXTENDWIDTH)
    {
        uCol = 2; // right side
    }

    // Hit test (HTTOPLEFT, ... HTBOTTOMRIGHT)
    LRESULT hitTests[3][3] = 
    {
        { HTTOPLEFT,    fOnResizeBorder ? HTTOP : HTCAPTION,    HTTOPRIGHT },
        { HTLEFT,       HTNOWHERE,     HTRIGHT },
        { HTBOTTOMLEFT, HTBOTTOM, HTBOTTOMRIGHT },
    };

    return hitTests[uRow][uCol];
}
```



## <a name="related-topics"></a><span data-ttu-id="84e9e-209">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="84e9e-209">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84e9e-210">Vue d’ensemble du Gestionnaire de fenêtres du Bureau</span><span class="sxs-lookup"><span data-stu-id="84e9e-210">Desktop Window Manager Overview</span></span>](dwm-overview.md)
</dt> </dl>

 

 
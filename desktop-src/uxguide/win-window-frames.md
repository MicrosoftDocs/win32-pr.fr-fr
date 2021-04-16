---
title: Frames de fenêtre
description: La plupart des programmes doivent utiliser des frames de fenêtre standard. Les applications immersives peuvent avoir un mode plein écran qui masque le cadre de la fenêtre. Envisagez d’utiliser la transparence de manière stratégique pour obtenir une apparence plus simple, plus claire et plus cohérente.
ms.assetid: 6613e07a-2466-4283-88a9-02f2a3fea079
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 40aa58ab48c032519f55afa7c269be6452956912
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104557318"
---
# <a name="window-frames"></a><span data-ttu-id="72e44-105">Frames de fenêtre</span><span class="sxs-lookup"><span data-stu-id="72e44-105">Window Frames</span></span>

> [!NOTE]
> <span data-ttu-id="72e44-106">Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows.</span><span class="sxs-lookup"><span data-stu-id="72e44-106">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="72e44-107">La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.</span><span class="sxs-lookup"><span data-stu-id="72e44-107">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="72e44-108">La plupart des programmes doivent utiliser des frames de fenêtre standard.</span><span class="sxs-lookup"><span data-stu-id="72e44-108">Most programs should use standard window frames.</span></span> <span data-ttu-id="72e44-109">Les applications immersives peuvent avoir un mode plein écran qui masque le cadre de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="72e44-109">Immersive applications can have a full screen mode that hides the window frame.</span></span> <span data-ttu-id="72e44-110">Envisagez d’utiliser la transparence de manière stratégique pour obtenir une apparence plus simple, plus claire et plus cohérente.</span><span class="sxs-lookup"><span data-stu-id="72e44-110">Consider using glass strategically for a simpler, lighter, more cohesive look.</span></span>

<span data-ttu-id="72e44-111">Avec un frame de fenêtre, les utilisateurs peuvent manipuler une fenêtre et afficher le titre et l’icône pour identifier son contenu.</span><span class="sxs-lookup"><span data-stu-id="72e44-111">With a window frame, users can manipulate a window and view the title and icon to identify its contents.</span></span>

![<span data-ttu-id="72e44-112">capture d’écran d’un cadre de fenêtre autour de la fenêtre du bloc-notes</span><span class="sxs-lookup"><span data-stu-id="72e44-112">screen shot of window frame around notepad window</span></span> ](images/win-window-frames-image1.png)

<span data-ttu-id="72e44-113">Frame de fenêtre classique.</span><span class="sxs-lookup"><span data-stu-id="72e44-113">A typical window frame.</span></span>

<span data-ttu-id="72e44-114">**Remarque :** Les instructions relatives à la gestion et à la [personnalisation](exper-branding.md) des [fenêtres](win-window-mgt.md) sont présentées dans des articles distincts.</span><span class="sxs-lookup"><span data-stu-id="72e44-114">**Note:** Guidelines related to [window management](win-window-mgt.md) and [branding](exper-branding.md) are presented in separate articles.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="72e44-115">Principes de conception</span><span class="sxs-lookup"><span data-stu-id="72e44-115">Design concepts</span></span>

### <a name="glass-window-frames"></a><span data-ttu-id="72e44-116">Frames de fenêtres en verre</span><span class="sxs-lookup"><span data-stu-id="72e44-116">Glass window frames</span></span>

<span data-ttu-id="72e44-117">Les cadres de fenêtres en verre sont un nouvel aspect de Microsoft Windows esthétique, qui vise à être à la fois attrayant et léger.</span><span class="sxs-lookup"><span data-stu-id="72e44-117">The glass window frames are a striking new aspect of the Microsoft Windows aesthetic, aiming to be both attractive and lightweight.</span></span> <span data-ttu-id="72e44-118">Ces frames translucides offrent aux fenêtres une apparence ouverte, moins intrusive, permettant aux utilisateurs de se concentrer sur le contenu et les fonctionnalités plutôt que sur l’interface qui les entoure.</span><span class="sxs-lookup"><span data-stu-id="72e44-118">These translucent frames give windows an open, less intrusive appearance, helping users focus on content and functionality rather than the interface surrounding it.</span></span>

![<span data-ttu-id="72e44-119">capture d’écran d’un cadre de transparence autour de la calculatrice</span><span class="sxs-lookup"><span data-stu-id="72e44-119">screen shot of glass frame around calculator</span></span> ](images/win-window-frames-image2.png)

<span data-ttu-id="72e44-120">Frames de fenêtres en verre.</span><span class="sxs-lookup"><span data-stu-id="72e44-120">Glass window frames.</span></span>

<span data-ttu-id="72e44-121">Vous pouvez utiliser la transparence de manière stratégique dans les petites zones d’une fenêtre qui touchent le cadre de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="72e44-121">You can use glass strategically in small regions within a window that touch the window frame.</span></span> <span data-ttu-id="72e44-122">Ces régions semblent faire partie du cadre de la fenêtre, même si techniquement elles font partie de la zone cliente de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="72e44-122">Such regions appear to be part of the window frame, even though technically they are part of the window's client area.</span></span>

![<span data-ttu-id="72e44-123">capture d’écran de la fenêtre avec bord translucide</span><span class="sxs-lookup"><span data-stu-id="72e44-123">screen shot of window with translucent edge</span></span> ](images/win-window-frames-image3.png)

<span data-ttu-id="72e44-124">Dans cet exemple, la transparence est utilisée dans la zone cliente pour qu’elle ressemble à une partie du cadre.</span><span class="sxs-lookup"><span data-stu-id="72e44-124">In this example, glass is used in the client area to make it look like part of the frame.</span></span>

### <a name="hidden-frames"></a><span data-ttu-id="72e44-125">Frames masqués</span><span class="sxs-lookup"><span data-stu-id="72e44-125">Hidden frames</span></span>

<span data-ttu-id="72e44-126">Parfois, le meilleur frame de fenêtre n’est pas du tout.</span><span class="sxs-lookup"><span data-stu-id="72e44-126">Sometimes the best window frame is no frame at all.</span></span> <span data-ttu-id="72e44-127">C’est souvent le cas pour la [fenêtre principale](glossary.md) d’applications [plein écran](glossary.md) immersives qui ne sont pas utilisées conjointement avec d’autres programmes, tels que des lecteurs multimédias, des jeux et des applications kiosque.</span><span class="sxs-lookup"><span data-stu-id="72e44-127">This is often the case for the [primary window](glossary.md) of immersive [full screen](glossary.md) applications that aren't used in conjunction with other programs, such as media players, games, and kiosk applications.</span></span>

<span data-ttu-id="72e44-128">Les visionneuses de contenu bénéficient souvent d’une option permettant d’afficher le contenu en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="72e44-128">Content viewers often benefit from having the option to show content full screen.</span></span> <span data-ttu-id="72e44-129">Voici quelques exemples : Windows Internet Explorer, Galerie de photos Windows Live, Windows Movie Maker HD, Microsoft PowerPoint et Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="72e44-129">Examples include Windows Internet Explorer , Windows Live Photo Gallery, Windows Movie Maker HD, Microsoft PowerPoint , and Microsoft Word.</span></span>

![<span data-ttu-id="72e44-130">capture d’écran du lecteur multimédia en mode plein écran</span><span class="sxs-lookup"><span data-stu-id="72e44-130">screen shot of media player in full-screen view</span></span> ](images/win-window-frames-image4.png)

<span data-ttu-id="72e44-131">Dans cet exemple, le lecteur Windows Media peut afficher son contenu en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="72e44-131">In this example, Windows Media Player can display its content full screen.</span></span>

### <a name="custom-frames"></a><span data-ttu-id="72e44-132">Frames personnalisés</span><span class="sxs-lookup"><span data-stu-id="72e44-132">Custom frames</span></span>

<span data-ttu-id="72e44-133">La plupart des applications Windows doivent utiliser les frames de fenêtre standard.</span><span class="sxs-lookup"><span data-stu-id="72e44-133">Most Windows applications should use the standard window frames.</span></span> <span data-ttu-id="72e44-134">Toutefois, pour les applications isolées, plein écran et autonomes comme les jeux et les applications kiosque, il peut être approprié d’utiliser des frames personnalisés pour toutes les fenêtres qui ne sont pas affichées en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="72e44-134">However, for immersive, full screen, stand-alone applications like games and kiosk applications, it may be appropriate to use custom frames for any windows that aren't shown full screen.</span></span> <span data-ttu-id="72e44-135">La motivation d’utiliser des frames personnalisés doit être d’offrir une expérience globale unique, pas seulement pour la [personnalisation](exper-branding.md).</span><span class="sxs-lookup"><span data-stu-id="72e44-135">The motivation to use custom frames should be to give the overall experience a unique feel, not just for [branding](exper-branding.md).</span></span>

![<span data-ttu-id="72e44-136">illustration du puzzle image brouillé et du cadre</span><span class="sxs-lookup"><span data-stu-id="72e44-136">illustration of scrambled picture puzzle and frame</span></span> ](images/win-window-frames-image5.png)

<span data-ttu-id="72e44-137">Les trames personnalisées sont appropriées pour les applications immersives, plein écran et autonomes, telles que les jeux.</span><span class="sxs-lookup"><span data-stu-id="72e44-137">Custom frames are appropriate for immersive, full screen, stand-alone applications such as games.</span></span>

## <a name="guidelines"></a><span data-ttu-id="72e44-138">Consignes</span><span class="sxs-lookup"><span data-stu-id="72e44-138">Guidelines</span></span>

### <a name="window-frames"></a><span data-ttu-id="72e44-139">Frames de fenêtre</span><span class="sxs-lookup"><span data-stu-id="72e44-139">Window frames</span></span>

-   <span data-ttu-id="72e44-140">Utilisez des frames de fenêtre standard.</span><span class="sxs-lookup"><span data-stu-id="72e44-140">Use standard window frames.</span></span>
    -   <span data-ttu-id="72e44-141">**Exception :** Pour fournir aux applications autonomes plein écran, une sensation unique :</span><span class="sxs-lookup"><span data-stu-id="72e44-141">**Exception:** To give immersive full screen, stand-alone applications a unique feel:</span></span>
        -   <span data-ttu-id="72e44-142">Envisagez de masquer le cadre de fenêtre de la [fenêtre principale](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="72e44-142">Consider hiding the window frame of the [primary window](glossary.md).</span></span>
        -   <span data-ttu-id="72e44-143">Envisagez d’utiliser des frames personnalisés pour la [fenêtre secondaire](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="72e44-143">Consider using custom frames for [secondary window](glossary.md).</span></span>
        -   <span data-ttu-id="72e44-144">Si un frame personnalisé est approprié, choisissez une conception légère et n’attire pas trop l’attention sur elle-même.</span><span class="sxs-lookup"><span data-stu-id="72e44-144">If a custom frame is appropriate, choose a design that is lightweight and doesn't draw too much attention to itself.</span></span>

            <span data-ttu-id="72e44-145">**Incorrect :**</span><span class="sxs-lookup"><span data-stu-id="72e44-145">**Incorrect:**</span></span>

            ![<span data-ttu-id="72e44-146">capture d’écran du cadre gênant</span><span class="sxs-lookup"><span data-stu-id="72e44-146">screen shot of distracting frame</span></span> ](images/win-window-frames-image6.png)

            <span data-ttu-id="72e44-147">Dans cet exemple, le frame personnalisé s’attire trop bien sur lui-même.</span><span class="sxs-lookup"><span data-stu-id="72e44-147">In this example, the custom frame draws too much attention to itself.</span></span>
-   <span data-ttu-id="72e44-148">N’ajoutez pas de contrôles à un frame de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="72e44-148">Don't add controls to a window frame.</span></span> <span data-ttu-id="72e44-149">Placez plutôt les contrôles dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="72e44-149">Put the controls within the window instead.</span></span>

    <span data-ttu-id="72e44-150">**Incorrect :**</span><span class="sxs-lookup"><span data-stu-id="72e44-150">**Incorrect:**</span></span>

    ![<span data-ttu-id="72e44-151">capture d’écran du contrôle dans le frame de fenêtre</span><span class="sxs-lookup"><span data-stu-id="72e44-151">screen shot of control in window frame</span></span> ](images/win-window-frames-image7.png)

    <span data-ttu-id="72e44-152">**Correct :**</span><span class="sxs-lookup"><span data-stu-id="72e44-152">**Correct:**</span></span>

    ![<span data-ttu-id="72e44-153">capture d’écran du contrôle dans la zone cliente</span><span class="sxs-lookup"><span data-stu-id="72e44-153">screen shot of control in client area</span></span> ](images/win-window-frames-image8.png)

    <span data-ttu-id="72e44-154">Dans l’exemple correct, le contrôle se trouve dans la zone cliente et non dans le cadre de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="72e44-154">In the correct example, the control is within the client area instead of the window frame.</span></span>

### <a name="full-screen-mode"></a><span data-ttu-id="72e44-155">Mode plein écran</span><span class="sxs-lookup"><span data-stu-id="72e44-155">Full screen mode</span></span>

-   <span data-ttu-id="72e44-156">Pour les programmes qui ont un mode plein écran facultatif, pour activer le mode plein écran :</span><span class="sxs-lookup"><span data-stu-id="72e44-156">For programs that have an optional full screen mode, to enable full screen mode:</span></span>
    -   <span data-ttu-id="72e44-157">Utilisez une commande modale plein écran dans la barre de menus ou la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="72e44-157">Have a modal full screen command in the menu bar or toolbar.</span></span> <span data-ttu-id="72e44-158">Lorsque l’utilisateur clique sur la commande, affichez la commande dans son état sélectionné.</span><span class="sxs-lookup"><span data-stu-id="72e44-158">When the user clicks the command, show the command in its selected state.</span></span>

        ![<span data-ttu-id="72e44-159">capture d’écran de la fenêtre avec l’élément de menu plein écran</span><span class="sxs-lookup"><span data-stu-id="72e44-159">screen shot of window with full screen menu item</span></span> ](images/win-window-frames-image9.png)

        <span data-ttu-id="72e44-160">Cet exemple montre la commande plein écran avec sa touche de raccourci standard.</span><span class="sxs-lookup"><span data-stu-id="72e44-160">This example shows the full screen command along with its standard shortcut key.</span></span>

-   <span data-ttu-id="72e44-161">Utilisez F11 pour la touche de raccourci plein écran.</span><span class="sxs-lookup"><span data-stu-id="72e44-161">Use F11 for the full screen shortcut key.</span></span>
-   <span data-ttu-id="72e44-162">S’il y a une barre d’outils et que le mode plein écran est couramment utilisé, vous avez également un bouton de barre d’outils graphique avec une info-bulle en plein écran.</span><span class="sxs-lookup"><span data-stu-id="72e44-162">If there is a toolbar and full screen mode is commonly used, also have a graphic toolbar button with a Full screen tooltip.</span></span>

    ![<span data-ttu-id="72e44-163">capture d’écran des boutons plein écran et rétablir</span><span class="sxs-lookup"><span data-stu-id="72e44-163">screen shot of full screen and revert buttons</span></span> ](images/win-window-frames-image10.png)

    <span data-ttu-id="72e44-164">Exemples de boutons de la barre d’outils plein écran.</span><span class="sxs-lookup"><span data-stu-id="72e44-164">Examples of full screen toolbar buttons.</span></span>

-   <span data-ttu-id="72e44-165">Pour revenir en arrière en mode plein écran :</span><span class="sxs-lookup"><span data-stu-id="72e44-165">To revert back from full screen mode:</span></span>
    -   <span data-ttu-id="72e44-166">Utilisez une commande modale plein écran dans la barre de menus ou la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="72e44-166">Have a modal full screen command in the menu bar or toolbar.</span></span> <span data-ttu-id="72e44-167">Lorsque l’utilisateur clique sur la commande, affichez la commande dans son état d’effacement.</span><span class="sxs-lookup"><span data-stu-id="72e44-167">When the user clicks the command, show the command in its cleared state.</span></span>
    -   <span data-ttu-id="72e44-168">Utilisez F11 pour la touche de raccourci plein écran.</span><span class="sxs-lookup"><span data-stu-id="72e44-168">Use F11 for the full screen shortcut key.</span></span> <span data-ttu-id="72e44-169">Si ce n’est déjà fait, la touche Échap peut également être utilisée à cet effet.</span><span class="sxs-lookup"><span data-stu-id="72e44-169">If not already assigned, Esc can also be used for this purpose.</span></span>

### <a name="glass"></a><span data-ttu-id="72e44-170">Glass</span><span class="sxs-lookup"><span data-stu-id="72e44-170">Glass</span></span>

<span data-ttu-id="72e44-171">Les frames de fenêtre standard utilisent le verre automatiquement dans Windows, mais vous pouvez également utiliser le verre dans les régions qui touchent le cadre de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="72e44-171">Standard window frames use glass automatically in Windows, but you can also use glass in regions that touch the window frame.</span></span>

-   <span data-ttu-id="72e44-172">**Envisagez d’utiliser la transparence de manière stratégique dans les petites régions qui touchent le cadre de la fenêtre sans texte.**</span><span class="sxs-lookup"><span data-stu-id="72e44-172">**Consider using glass strategically in small regions touching the window frame without text.**</span></span> <span data-ttu-id="72e44-173">Cela peut donner à un programme un aspect plus simple, plus clair et plus cohérent en faisant en sorte que la région apparaisse comme faisant partie du cadre.</span><span class="sxs-lookup"><span data-stu-id="72e44-173">Doing so can give a program a simpler, lighter, more cohesive look by making the region appear to be part of the frame.</span></span>
-   ![<span data-ttu-id="72e44-174">capture d’écran de la fenêtre avec bord translucide</span><span class="sxs-lookup"><span data-stu-id="72e44-174">screen shot of window with translucent edge</span></span> ](images/win-window-frames-image3.png)
-   <span data-ttu-id="72e44-175">Dans cet exemple, la transparence porte l’attention de l’utilisateur sur le contenu au lieu des contrôles.</span><span class="sxs-lookup"><span data-stu-id="72e44-175">In this example, glass focuses the user's attention on the content instead of the controls.</span></span>
-   <span data-ttu-id="72e44-176">**N’utilisez pas de verre dans les situations où un arrière-plan de fenêtre ordinaire serait plus attrayant ou plus facile à utiliser.**</span><span class="sxs-lookup"><span data-stu-id="72e44-176">**Don't use glass in situations where a plain window background would be more attractive or easier to use.**</span></span>

<span data-ttu-id="72e44-177">**Correct :**</span><span class="sxs-lookup"><span data-stu-id="72e44-177">**Correct:**</span></span>

![<span data-ttu-id="72e44-178">capture d’écran de la fenêtre avec quatre graphiques et étiquette</span><span class="sxs-lookup"><span data-stu-id="72e44-178">screen shot of window with four graphics and label</span></span> ](images/win-window-frames-image11.png)

<span data-ttu-id="72e44-179">Dans cet exemple, la transparence est utilisée pour attribuer une apparence légère à la fenêtre ALT + TAB.</span><span class="sxs-lookup"><span data-stu-id="72e44-179">In this example, glass is used to give the Alt+Tab window a lightweight appearance.</span></span> <span data-ttu-id="72e44-180">La vitre fonctionne pour cette fenêtre, car elle se compose de graphiques et d’une seule étiquette de texte fort.</span><span class="sxs-lookup"><span data-stu-id="72e44-180">Glass works for this window because it consists of graphics and a single, strong text label.</span></span>

<span data-ttu-id="72e44-181">**Incorrect :**</span><span class="sxs-lookup"><span data-stu-id="72e44-181">**Incorrect:**</span></span>

![<span data-ttu-id="72e44-182">capture d’écran de la fenêtre avec douze graphiques</span><span class="sxs-lookup"><span data-stu-id="72e44-182">screen shot of window with twelve graphics</span></span> ](images/win-window-frames-image12.png)

<span data-ttu-id="72e44-183">Dans cet exemple incorrect, l’utilisation de la vitre est gênante.</span><span class="sxs-lookup"><span data-stu-id="72e44-183">In this incorrect example, the use of glass is distracting.</span></span> <span data-ttu-id="72e44-184">Un arrière-plan de fenêtre ordinaire est un meilleur choix.</span><span class="sxs-lookup"><span data-stu-id="72e44-184">A plain window background would be a better choice.</span></span>

 

 
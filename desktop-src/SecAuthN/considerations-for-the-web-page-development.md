---
description: Le Service Broker d’authentification Web est basé sur les technologies qui alimentent Internet Explorer dans Windows.
ms.assetid: 4BBAE30F-63AB-4AB0-9C99-016EF05220E8
title: Considérations sur le développement de pages web
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbe7e738616589afc4f7ba4f03d92a12207d189c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319378"
---
# <a name="considerations-for-the-web-page-development"></a><span data-ttu-id="12125-103">Considérations sur le développement de pages web</span><span class="sxs-lookup"><span data-stu-id="12125-103">Considerations for the web page development</span></span>

<span data-ttu-id="12125-104">Le Service Broker d’authentification Web est basé sur les technologies qui alimentent Internet Explorer dans Windows.</span><span class="sxs-lookup"><span data-stu-id="12125-104">Web Authentication Broker is built on the top of the same technologies that power Internet Explorer in Windows.</span></span> <span data-ttu-id="12125-105">Toutefois, en raison d’un objectif très spécial de ce composant, certaines fonctionnalités d’Internet Explorer ont été désactivées ou verrouillées à une configuration spécifique.</span><span class="sxs-lookup"><span data-stu-id="12125-105">However, due to a very special purpose of this component some features of the Internet Explorer were disabled or locked to specific configuration.</span></span> <span data-ttu-id="12125-106">En outre, le Service Broker d’authentification Web fournit un canal de journalisation des événements dédié pour aider à résoudre les problèmes liés aux pages qu’il traite.</span><span class="sxs-lookup"><span data-stu-id="12125-106">Also, Web Authentication Broker provides a dedicated event logging channel to help troubleshoot issues with pages that it processes.</span></span>

## <a name="internet-explorer-10-standard-document-mode"></a><span data-ttu-id="12125-107">Mode de document standard d’Internet Explorer 10</span><span class="sxs-lookup"><span data-stu-id="12125-107">Internet Explorer 10 standard document mode</span></span>

<span data-ttu-id="12125-108">Le Service Broker d’authentification Web affiche toutes les pages en « IE10 standard mode ».</span><span class="sxs-lookup"><span data-stu-id="12125-108">The Web Authentication Broker displays all pages in the "IE10 Standards Mode".</span></span> <span data-ttu-id="12125-109">Vous pouvez utiliser les outils de développement dans Internet Explorer pour voir comment votre page fonctionne dans différents modes de document.</span><span class="sxs-lookup"><span data-stu-id="12125-109">You can use the developer tools in Internet Explorer to see how your page works under different document modes.</span></span> <span data-ttu-id="12125-110">Pour plus d’informations sur la compatibilité d’Internet Explorer 10, consultez les rubriques MSDN pour [Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/dev-guides/hh673527(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="12125-110">For more information on Internet Explorer 10 compatibility, see the MSDN topics for [Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/dev-guides/hh673527(v=vs.85)).</span></span>

## <a name="disabled-and-locked-down-features"></a><span data-ttu-id="12125-111">Fonctionnalités désactivées et verrouillées</span><span class="sxs-lookup"><span data-stu-id="12125-111">Disabled and locked down features</span></span>

<span data-ttu-id="12125-112">Plusieurs fonctionnalités d’Internet Explorer sont complètement désactivées ou verrouillées vers des valeurs spécifiques qui ne peuvent pas être modifiées dans les options Internet du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="12125-112">Several features of Internet Explorer are either completely disabled or locked down to specific values that can’t be changed in the Internet Options of the operating system.</span></span>



| <span data-ttu-id="12125-113">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="12125-113">Feature</span></span>                            | <span data-ttu-id="12125-114">Statut</span><span class="sxs-lookup"><span data-stu-id="12125-114">Status</span></span>                                                                                                                                                                                                          |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12125-115">API du cache d’application (« AppCache) »)</span><span class="sxs-lookup"><span data-stu-id="12125-115">Application Cache API ("AppCache")</span></span> | <span data-ttu-id="12125-116">Désactivé</span><span class="sxs-lookup"><span data-stu-id="12125-116">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="12125-117">Historique des liens</span><span class="sxs-lookup"><span data-stu-id="12125-117">Link history</span></span>                       | <span data-ttu-id="12125-118">Désactivé</span><span class="sxs-lookup"><span data-stu-id="12125-118">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="12125-119">Fichiers temporaires</span><span class="sxs-lookup"><span data-stu-id="12125-119">Temporary files</span></span>                    | <span data-ttu-id="12125-120">activé</span><span class="sxs-lookup"><span data-stu-id="12125-120">Enabled</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="12125-121">Cookies</span><span class="sxs-lookup"><span data-stu-id="12125-121">Cookies</span></span>                            | <span data-ttu-id="12125-122">Les cookies de session sont activés.</span><span class="sxs-lookup"><span data-stu-id="12125-122">Session cookies are enabled.</span></span> <span data-ttu-id="12125-123">Les cookies persistants sont autorisés, mais ils sont soumis au nettoyage automatique, sauf si le répartiteur d’authentification Web est en mode SSO.</span><span class="sxs-lookup"><span data-stu-id="12125-123">Persisted cookies are allowed, but are subject to automatic cleanup unless the Web Authentication Broker is in the SSO mode.</span></span> <span data-ttu-id="12125-124">Pour plus d’informations, consultez la section authentification unique.</span><span class="sxs-lookup"><span data-stu-id="12125-124">For more information, see the Single Sign On section.</span></span> |
| <span data-ttu-id="12125-125">BASE de l’index</span><span class="sxs-lookup"><span data-stu-id="12125-125">Index DB</span></span>                           | <span data-ttu-id="12125-126">Désactivé</span><span class="sxs-lookup"><span data-stu-id="12125-126">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="12125-127">Stockage DOM</span><span class="sxs-lookup"><span data-stu-id="12125-127">DOM storage</span></span>                        | <span data-ttu-id="12125-128">Désactivé</span><span class="sxs-lookup"><span data-stu-id="12125-128">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="12125-129">ActiveX</span><span class="sxs-lookup"><span data-stu-id="12125-129">ActiveX</span></span>                            | <span data-ttu-id="12125-130">Désactivé</span><span class="sxs-lookup"><span data-stu-id="12125-130">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="12125-131">Téléchargements de fichiers</span><span class="sxs-lookup"><span data-stu-id="12125-131">File downloads</span></span>                     | <span data-ttu-id="12125-132">Désactivé</span><span class="sxs-lookup"><span data-stu-id="12125-132">Disabled</span></span>                                                                                                                                                                                                        |



 

## <a name="https-requirement"></a><span data-ttu-id="12125-133">Configuration requise pour HTTPs</span><span class="sxs-lookup"><span data-stu-id="12125-133">HTTPS requirement</span></span>

<span data-ttu-id="12125-134">La première URL qu’une application doit utiliser pour communiquer avec le fournisseur en ligne doit être HTTPs.</span><span class="sxs-lookup"><span data-stu-id="12125-134">The first URL that an application will use to communicate with the online provider is required to be HTTPS.</span></span>

## <a name="dimension-for-different-window-sizes"></a><span data-ttu-id="12125-135">Dimension pour différentes tailles de fenêtre</span><span class="sxs-lookup"><span data-stu-id="12125-135">Dimension for different window sizes</span></span>

<span data-ttu-id="12125-136">Une application Windows 8 peut apparaître dans différentes tailles, par exemple plein écran, une fenêtre redimensionnée ou une icône de partage.</span><span class="sxs-lookup"><span data-stu-id="12125-136">A Windows 8 app may appear in several different sizes such as full screen, a resized window, or within a Charm such as Share Charm.</span></span> <span data-ttu-id="12125-137">En fonction de la disposition de fenêtre affichée par le répartiteur d’authentification Web, la taille avec laquelle les pages Web doivent fonctionner peut être différente.</span><span class="sxs-lookup"><span data-stu-id="12125-137">Depending in which window layout the Web Authentication Broker appears, the size with which the web pages have to work could be different.</span></span> <span data-ttu-id="12125-138">Pour plus d’informations, consultez la rubrique [instructions pour le redimensionnement des dispositions étroites](/previous-versions/windows/hh465371(v=win.10)) et la rubrique [instructions de partage de contenu](/previous-versions/windows/hh465251(v=win.10)) .</span><span class="sxs-lookup"><span data-stu-id="12125-138">For more information, see the [Guidelines for resizing to narrow layouts](/previous-versions/windows/hh465371(v=win.10)) topic and the [Guidelines for sharing content](/previous-versions/windows/hh465251(v=win.10)) topic.</span></span>

<span data-ttu-id="12125-139">La page Web doit utiliser des requêtes de média CSS pour vérifier la taille à laquelle elle doit travailler et se présenter en conséquence.</span><span class="sxs-lookup"><span data-stu-id="12125-139">The web page should use CSS media queries to check the size it has to work with and lay itself out accordingly.</span></span> <span data-ttu-id="12125-140">Toutefois, la page ne doit pas être conçue en fonction des pixels exacts décrits ici et doit être en mesure de s’adapter à différentes tailles.</span><span class="sxs-lookup"><span data-stu-id="12125-140">However, the page should not be designed based on the exact pixels documented here and should be able to scale to different sizes.</span></span> <span data-ttu-id="12125-141">Les tailles spécifiées dans ce document sont susceptibles d’être modifiées dans les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="12125-141">The sizes specified in this document are subject to change in future OS versions.</span></span>

<span data-ttu-id="12125-142">Si une page ne peut pas contenir toutes les informations de l’espace alloué (par exemple, une longue liste d’autorisations demandées par une application), le répartiteur d’authentification Web fournit des barres de défilement pour permettre à l’utilisateur de faire défiler la page en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="12125-142">If a page can’t fit all of the information in the allotted space (for example, a long list of permissions that an application is requesting), the Web Authentication Broker will provide scroll bars to allow the user to scroll the page as needed.</span></span> <span data-ttu-id="12125-143">Le zoom est également fourni par pincer pour les appareils tactiles et CTRL + roulette de la souris pour les PC de bureau et les ordinateurs portables.</span><span class="sxs-lookup"><span data-stu-id="12125-143">Zooming is also provided by pinch zoom for touch-based devices and Ctrl + mouse wheel for desktop and laptop PCs.</span></span>

<span data-ttu-id="12125-144">Pour tester différents facteurs de mise à l’échelle, utilisez l ['exemple d’application du kit de développement logiciel (SDK) Web Authentication Broker](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) chargée dans Microsoft Visual Studio Professional 2012 qui permet de simuler les États en plein écran et redimensionnés.</span><span class="sxs-lookup"><span data-stu-id="12125-144">To test different scaling factors use the [Web Authentication Broker SDK sample app](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) loaded in Microsoft Visual Studio Professional 2012 which allows simulating the full screen and resized states.</span></span>

<span data-ttu-id="12125-145">Outre les différentes dispositions documentées ci-dessus, veillez à tester votre page dans une autre orientation d’écran (par exemple, portrait et paysage), ainsi que des paramètres régionaux et des langages différents, ainsi que des fonctionnalités d’accessibilité telles que l’option « rendre tout le plus grand » activée.</span><span class="sxs-lookup"><span data-stu-id="12125-145">In addition to different layouts documented above, make sure to test your page in different screen orientation (for example, portrait and landscape), and different locales and languages as well as with accessibility features such as the "Make everything bigger" option turned on.</span></span>

<span data-ttu-id="12125-146">Les dispositions disponibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="12125-146">The available layouts are:</span></span>

-   [<span data-ttu-id="12125-147">Plein écran</span><span class="sxs-lookup"><span data-stu-id="12125-147">Full screen</span></span>](#full-screen)
-   [<span data-ttu-id="12125-148">Fenêtre redimensionnée</span><span class="sxs-lookup"><span data-stu-id="12125-148">Resized window</span></span>](#resized)
-   [<span data-ttu-id="12125-149">Vue de l’icône</span><span class="sxs-lookup"><span data-stu-id="12125-149">Charm view</span></span>](#charm-view)
-   [<span data-ttu-id="12125-150">Vue du sélecteur de fichiers</span><span class="sxs-lookup"><span data-stu-id="12125-150">File picker view</span></span>](#file-picker-view)

### <a name="full-screen"></a><span data-ttu-id="12125-151">Plein écran</span><span class="sxs-lookup"><span data-stu-id="12125-151">Full screen</span></span>

<span data-ttu-id="12125-152">Pour la disposition plein écran, les dimensions de la page Web sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="12125-152">For the full screen layout, the web page dimensions are:</span></span>

-   <span data-ttu-id="12125-153">Largeur : 566 pixels</span><span class="sxs-lookup"><span data-stu-id="12125-153">Width: 566 pixels</span></span>
-   <span data-ttu-id="12125-154">Hauteur : hauteur de l’écran (dépend de la résolution de l’écran)</span><span class="sxs-lookup"><span data-stu-id="12125-154">Height: Screen height (depends on the screen resolution)</span></span>

<span data-ttu-id="12125-155">L’exemple suivant montre l’interface utilisateur du répartiteur d’authentification Web en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="12125-155">The following example shows the web authentication broker UI in full screen layout.</span></span>

![exemple d’interface utilisateur du Broker d’authentification Web en mode plein écran](images/wab-figure2.png)

### <a name="resized"></a><span data-ttu-id="12125-157">Redimensionné</span><span class="sxs-lookup"><span data-stu-id="12125-157">Resized</span></span>

<span data-ttu-id="12125-158">Pour une fenêtre redimensionnée, les dimensions de la page Web peuvent être :</span><span class="sxs-lookup"><span data-stu-id="12125-158">For a resized window, the web page dimensions can be:</span></span>

-   <span data-ttu-id="12125-159">Largeur : 260 pixels</span><span class="sxs-lookup"><span data-stu-id="12125-159">Width: 260 pixels</span></span>
-   <span data-ttu-id="12125-160">Hauteur : hauteur de l’écran (dépend de la résolution de l’écran)</span><span class="sxs-lookup"><span data-stu-id="12125-160">Height: Screen height (depends on the screen resolution)</span></span>

<span data-ttu-id="12125-161">L’exemple suivant montre l’interface utilisateur du répartiteur d’authentification Web dans une fenêtre redimensionnée sur la page Web XBox.</span><span class="sxs-lookup"><span data-stu-id="12125-161">The following example shows the Web Authentication Broker UI in a resized window on the XBox web page.</span></span> <span data-ttu-id="12125-162">Notez que l’interface utilisateur du répartiteur d’authentification Web se trouve uniquement sur le côté droit de la capture d’écran.</span><span class="sxs-lookup"><span data-stu-id="12125-162">Note that the Web Authentication Broker UI is only on the right side of the screen capture.</span></span>

![exemple d’interface utilisateur du Broker d’authentification Web dans une fenêtre redimensionnée](images/wab-figure3.png)

### <a name="charm-view"></a><span data-ttu-id="12125-164">Vue de l’icône</span><span class="sxs-lookup"><span data-stu-id="12125-164">Charm view</span></span>

<span data-ttu-id="12125-165">Pour la vue de l’icône, les dimensions de la page Web sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="12125-165">For the Charm view, the web page dimensions are:</span></span>

-   <span data-ttu-id="12125-166">Largeur : 566 pixels</span><span class="sxs-lookup"><span data-stu-id="12125-166">Width: 566 pixels</span></span>
-   <span data-ttu-id="12125-167">Hauteur : hauteur de l’écran (dépend de la résolution de l’écran)</span><span class="sxs-lookup"><span data-stu-id="12125-167">Height: Screen height (depends on the screen resolution)</span></span>

<span data-ttu-id="12125-168">L’exemple suivant montre l’interface utilisateur du répartiteur d’authentification Web dans la vue icône.</span><span class="sxs-lookup"><span data-stu-id="12125-168">The following example shows the Web Authentication Broker UI in Charm view.</span></span>

![un exemple illustre l’interface utilisateur du répartiteur d’authentification Web dans la vue icône](images/wab-figure4.png)

### <a name="file-picker-view"></a><span data-ttu-id="12125-170">Vue du sélecteur de fichiers</span><span class="sxs-lookup"><span data-stu-id="12125-170">File picker view</span></span>

<span data-ttu-id="12125-171">Pour la vue sélecteur de fichiers, les dimensions de la page Web sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="12125-171">For the file picker view, the web page dimensions are:</span></span>

-   <span data-ttu-id="12125-172">Largeur : 566 pixels</span><span class="sxs-lookup"><span data-stu-id="12125-172">Width: 566 pixels</span></span>
-   <span data-ttu-id="12125-173">Hauteur : hauteur de l’écran (dépend de la résolution de l’écran)</span><span class="sxs-lookup"><span data-stu-id="12125-173">Height: Screen height (depends on the screen resolution)</span></span>

<span data-ttu-id="12125-174">L’exemple suivant montre l’interface utilisateur du répartiteur d’authentification Web dans la vue sélecteur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="12125-174">The following example shows the Web Authentication Broker UI in file picker view.</span></span>

![un exemple illustre l’interface utilisateur du Service Broker d’authentification Web dans la vue sélecteur de fichiers](images/wab-figure5.png)

## <a name="no-new-windows-by-default"></a><span data-ttu-id="12125-176">Aucune nouvelle fenêtre par défaut</span><span class="sxs-lookup"><span data-stu-id="12125-176">No new windows by default</span></span>

<span data-ttu-id="12125-177">Par défaut, aucune URL n’entraîne l’ouverture d’une nouvelle fenêtre, mais elle s’affiche à la place dans la fenêtre du répartiteur d’authentification Web.</span><span class="sxs-lookup"><span data-stu-id="12125-177">By default, no URLs will result in a new window being opened but will instead be displayed within the Web Authentication Broker window.</span></span> <span data-ttu-id="12125-178">Cela comprend la méthode JavaScript window. Open, l’attribut « Target » des liens hypertexte ou lorsque l’utilisateur utilise le mécanisme Ctrl + clic pour forcer l’ouverture d’une nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="12125-178">This includes window.open JavaScript method, "target" attribute of the hyperlinks, or when the user uses the Ctrl+Click mechanism to force a new window to open.</span></span> <span data-ttu-id="12125-179">La seule exception à cette règle est lorsqu’une page Web déclare un lien comme étant sécurisé pour naviguer dans un navigateur, comme décrit dans la cible de personnalisation des liens hypertexte.</span><span class="sxs-lookup"><span data-stu-id="12125-179">The exception to this rule is when a web page declares a link as safe to be navigated in a browser as described in the Customizing Target of the Hyperlinks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12125-180">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="12125-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12125-181">Exemple d’application du SDK du Broker d’authentification Web</span><span class="sxs-lookup"><span data-stu-id="12125-181">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="12125-182">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="12125-182">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 

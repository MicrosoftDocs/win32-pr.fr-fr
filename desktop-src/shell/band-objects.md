---
description: La barre d’exploration a été introduite avec Microsoft Internet Explorer 4,0 pour fournir une zone d’affichage adjacente au volet du navigateur.
title: Créer des barres d’explorateur, des bandes d’outils et des bandes de bureau personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4bf46b3f-f833-42e0-baf7-21bfa9e6d890
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b4adeaaf089c22bd3e1db3d60d552ccc3252545a
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104562930"
---
# <a name="creating-custom-explorer-bars-tool-bands-and-desk-bands"></a><span data-ttu-id="77037-103">Création de barres d’exploration, de bandes d’outils et de bandes de bureau personnalisées</span><span class="sxs-lookup"><span data-stu-id="77037-103">Creating Custom Explorer Bars, Tool Bands, and Desk Bands</span></span>

<span data-ttu-id="77037-104">La barre d’exploration a été introduite avec Microsoft Internet Explorer 4,0 pour fournir une zone d’affichage adjacente au volet du navigateur.</span><span class="sxs-lookup"><span data-stu-id="77037-104">The Explorer Bar was introduced with Microsoft Internet Explorer 4.0 to provide a display area adjacent to the browser pane.</span></span> <span data-ttu-id="77037-105">En fait, il s’agit d’une fenêtre enfant dans la fenêtre Windows Internet Explorer, qui peut être utilisée pour afficher des informations et interagir avec l’utilisateur à peu près de la même façon.</span><span class="sxs-lookup"><span data-stu-id="77037-105">It is basically a child window within the Windows Internet Explorer window, and it can be used to display information and interact with the user in much the same way.</span></span> <span data-ttu-id="77037-106">Les barres d’exploration sont le plus souvent affichées sous la forme d’un volet vertical sur le côté gauche du volet du navigateur.</span><span class="sxs-lookup"><span data-stu-id="77037-106">Explorer Bars are most commonly displayed as a vertical pane on the left side of the browser pane.</span></span> <span data-ttu-id="77037-107">Toutefois, une barre d’exploration peut également être affichée horizontalement, sous le volet du navigateur.</span><span class="sxs-lookup"><span data-stu-id="77037-107">However, an Explorer Bar can also be displayed horizontally, below the browser pane.</span></span>

![Capture d’écran montrant les barres d’exploration verticales et horizontales.](images/expl1.jpg)

<span data-ttu-id="77037-109">Il existe un large éventail d’utilisations possibles pour le volet d’exploration.</span><span class="sxs-lookup"><span data-stu-id="77037-109">There is a wide range of possible uses for the Explorer Bar.</span></span> <span data-ttu-id="77037-110">Les utilisateurs peuvent sélectionner l’option qu’ils souhaitent voir de différentes façons, notamment en les sélectionnant dans le sous-menu du **volet d’exploration** du menu **affichage** ou en cliquant sur un bouton de barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="77037-110">Users can select which option they want to see in several different ways, including selecting it from the **Explorer Bar** submenu of the **View** menu, or clicking a toolbar button.</span></span> <span data-ttu-id="77037-111">Internet Explorer propose plusieurs barres d’exploration standard, y compris les favoris et la recherche.</span><span class="sxs-lookup"><span data-stu-id="77037-111">Internet Explorer provides several standard Explorer Bars, including Favorites and Search.</span></span>

<span data-ttu-id="77037-112">L’une des méthodes permettant de personnaliser Internet Explorer consiste à ajouter un volet d’exploration personnalisé.</span><span class="sxs-lookup"><span data-stu-id="77037-112">One of the ways you can customize Internet Explorer is by adding a custom Explorer Bar.</span></span> <span data-ttu-id="77037-113">Lorsqu’elle est implémentée et inscrite, elle est ajoutée au sous-menu du **volet d’exploration** du menu **affichage** .</span><span class="sxs-lookup"><span data-stu-id="77037-113">When implemented and registered, it will be added to the **Explorer Bar** submenu of the **View** menu.</span></span> <span data-ttu-id="77037-114">Lorsqu’il est sélectionné par l’utilisateur, la zone d’affichage de la barre d’exploration peut ensuite être utilisée pour afficher des informations et effectuer des entrées utilisateur de la même façon qu’une fenêtre normale.</span><span class="sxs-lookup"><span data-stu-id="77037-114">When selected by the user, the Explorer Bar's display area can then be used to display information and take user input in much the same way as a normal window.</span></span>

![capture d’écran des barres de l’Explorateur](images/expl2.jpg)

<span data-ttu-id="77037-116">Pour créer une barre d’exploration personnalisée, vous devez implémenter et inscrire un *objet de bande*.</span><span class="sxs-lookup"><span data-stu-id="77037-116">To create a custom Explorer Bar, you must implement and register a *band object*.</span></span> <span data-ttu-id="77037-117">Les objets Band ont été introduits avec la version 4,71 de l’interpréteur de commandes et offrent des fonctionnalités similaires à celles des fenêtres normales.</span><span class="sxs-lookup"><span data-stu-id="77037-117">Band objects were introduced with version 4.71 of the Shell and provide capabilities similar to those of normal windows.</span></span> <span data-ttu-id="77037-118">Toutefois, étant donné qu’il s’agit d’objets COM (Component Object Model) et qu’ils sont contenus par Internet Explorer ou le shell, ils sont implémentés un peu différemment.</span><span class="sxs-lookup"><span data-stu-id="77037-118">However, because they are Component Object Model (COM) objects and contained by either Internet Explorer or the Shell, they are implemented somewhat differently.</span></span> <span data-ttu-id="77037-119">Des objets de bande simples ont été utilisés pour créer les exemples de barres d’explorateur affichées dans le premier graphique.</span><span class="sxs-lookup"><span data-stu-id="77037-119">Simple band objects were used to create the sample Explorer Bars displayed in the first graphic.</span></span> <span data-ttu-id="77037-120">L’implémentation de l’exemple de barre d’exploration verticale sera traitée en détail dans une section ultérieure.</span><span class="sxs-lookup"><span data-stu-id="77037-120">The implementation of the vertical Explorer Bar sample will be discussed in detail in a later section.</span></span>

## <a name="tool-bands"></a><span data-ttu-id="77037-121">Bandes d’outils</span><span class="sxs-lookup"><span data-stu-id="77037-121">Tool Bands</span></span>

<span data-ttu-id="77037-122">Une *bande d’outils* est un objet de bande introduit avec Microsoft Internet Explorer 5 pour prendre en charge la fonctionnalité de la barre d’outils radio Windows.</span><span class="sxs-lookup"><span data-stu-id="77037-122">A *tool band* is a band object that was introduced with Microsoft Internet Explorer 5 to support the Windows radio toolbar feature.</span></span> <span data-ttu-id="77037-123">La barre d’outils Internet Explorer est en fait un [contrôle rebar](../controls/rebar-controls.md) qui contient plusieurs [contrôles ToolBar](../controls/toolbar-control-reference.md).</span><span class="sxs-lookup"><span data-stu-id="77037-123">The Internet Explorer toolbar is actually a [rebar control](../controls/rebar-controls.md) that contains several [toolbar controls](../controls/toolbar-control-reference.md).</span></span> <span data-ttu-id="77037-124">En créant une bande d’outils, vous pouvez ajouter une bande à ce contrôle rebar.</span><span class="sxs-lookup"><span data-stu-id="77037-124">By creating a tool band, you can add a band to that rebar control.</span></span> <span data-ttu-id="77037-125">Toutefois, comme les barres d’exploration, une bande d’outils est une fenêtre à usage général.</span><span class="sxs-lookup"><span data-stu-id="77037-125">However, like Explorer Bars, a tool band is a general purpose window.</span></span>

![capture d’écran des bandes d’outils](images/toolband1.jpg)

<span data-ttu-id="77037-127">Les utilisateurs affichent une barre d’outils en les sélectionnant dans le sous-menu **barres** d’outils du menu **affichage** ou dans le menu contextuel qui s’affiche lorsque vous cliquez avec le bouton droit sur la zone de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="77037-127">Users display a toolbar by selecting it from the **Toolbars** submenu of the **View** menu or from the shortcut menu that is displayed by right-clicking the toolbar area.</span></span>

## <a name="desk-bands"></a><span data-ttu-id="77037-128">Bandes de bureau</span><span class="sxs-lookup"><span data-stu-id="77037-128">Desk Bands</span></span>

<span data-ttu-id="77037-129">Les objets de bande peuvent également être utilisés pour créer des *bandes de bureau*.</span><span class="sxs-lookup"><span data-stu-id="77037-129">Band objects can also be used to create *desk bands*.</span></span> <span data-ttu-id="77037-130">Bien que leur implémentation de base soit similaire aux barres d’exploration, les bandes de bureau ne sont pas liées à Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="77037-130">While their basic implementation is similar to Explorer Bars, desk bands are unrelated to Internet Explorer.</span></span> <span data-ttu-id="77037-131">Une bande de bureau est fondamentalement un moyen de créer une fenêtre Ancrable sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="77037-131">A desk band is basically a way to create a dockable window on the desktop.</span></span> <span data-ttu-id="77037-132">L’utilisateur le sélectionne en cliquant avec le bouton droit sur la barre des tâches et en le sélectionnant dans le sous-menu **barres d’outils** .</span><span class="sxs-lookup"><span data-stu-id="77037-132">The user selects it by right-clicking the taskbar and selecting it from the **Toolbars** submenu.</span></span>

![Capture d’écran montrant un exemple de bande de bureau.](images/desk2.png)

<span data-ttu-id="77037-134">Initialement, les bandes de bureau sont ancrées dans la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="77037-134">Initially, desk bands are docked on the taskbar.</span></span>

![Capture d’écran montrant les bandes de bureau ancrées dans la barre des tâches.](images/desk1.jpg)

<span data-ttu-id="77037-136">L’utilisateur peut ensuite faire glisser la bande de bureau sur le Bureau pour qu’elle s’affiche en tant que fenêtre normale.</span><span class="sxs-lookup"><span data-stu-id="77037-136">The user can then drag the desk band to the desktop, and it will appear as a normal window.</span></span>

![capture d’écran des bandes de bureau](images/desk3.png)

## <a name="implementing-band-objects"></a><span data-ttu-id="77037-138">Implémentation d’objets de bande</span><span class="sxs-lookup"><span data-stu-id="77037-138">Implementing Band Objects</span></span>

<span data-ttu-id="77037-139">Les rubriques suivantes sont présentées.</span><span class="sxs-lookup"><span data-stu-id="77037-139">The following topics are discussed.</span></span>

-   [<span data-ttu-id="77037-140">Notions de base sur les objets Band</span><span class="sxs-lookup"><span data-stu-id="77037-140">Band Object Basics</span></span>](#band-object-basics)
-   [<span data-ttu-id="77037-141">Enregistrement de la bande</span><span class="sxs-lookup"><span data-stu-id="77037-141">Band Registration</span></span>](#band-registration)
-   [<span data-ttu-id="77037-142">Exemple simple d’une barre d’exploration personnalisée</span><span class="sxs-lookup"><span data-stu-id="77037-142">A Simple Example of a Custom Explorer Bar</span></span>](#a-simple-example-of-a-custom-explorer-bar)

### <a name="band-object-basics"></a><span data-ttu-id="77037-143">Notions de base sur les objets Band</span><span class="sxs-lookup"><span data-stu-id="77037-143">Band Object Basics</span></span>

<span data-ttu-id="77037-144">Bien qu’ils puissent être utilisés comme des fenêtres normales, les objets de bande sont des objets COM qui existent au sein d’un conteneur.</span><span class="sxs-lookup"><span data-stu-id="77037-144">Although they can be used much like normal windows, band objects are COM objects that exist within a container.</span></span> <span data-ttu-id="77037-145">Les barres d’exploration sont contenues dans Internet Explorer et les bandes de bureau sont contenues dans l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="77037-145">Explorer Bars are contained by Internet Explorer, and desk bands are contained by the Shell.</span></span> <span data-ttu-id="77037-146">Bien qu’elles remplissent des fonctions différentes, leur implémentation de base est très similaire.</span><span class="sxs-lookup"><span data-stu-id="77037-146">While they serve different functions, their basic implementation is very similar.</span></span> <span data-ttu-id="77037-147">La principale différence réside dans la façon dont l’objet de bande est inscrit, qui à son tour contrôle le type d’objet et son conteneur.</span><span class="sxs-lookup"><span data-stu-id="77037-147">The primary difference is in how the band object is registered, which in turn controls the type of object and its container.</span></span> <span data-ttu-id="77037-148">Cette section décrit les aspects de l’implémentation qui sont communs à tous les objets de bande.</span><span class="sxs-lookup"><span data-stu-id="77037-148">This section discusses those aspects of implementation that are common to all band objects.</span></span> <span data-ttu-id="77037-149">Pour plus d’informations sur l’implémentation, consultez [un exemple simple d’une barre d’explorateur personnalisée](#a-simple-example-of-a-custom-explorer-bar) .</span><span class="sxs-lookup"><span data-stu-id="77037-149">See [A Simple Example of a Custom Explorer Bar](#a-simple-example-of-a-custom-explorer-bar) for additional implementation details.</span></span>

<span data-ttu-id="77037-150">En plus des [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) et [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory), tous les objets Band doivent implémenter les interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="77037-150">In addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) and [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory), all band objects must implement the following interfaces.</span></span>

-   [<span data-ttu-id="77037-151">**IDeskBand**</span><span class="sxs-lookup"><span data-stu-id="77037-151">**IDeskBand**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)
-   [<span data-ttu-id="77037-152">**IObjectWithSite**</span><span class="sxs-lookup"><span data-stu-id="77037-152">**IObjectWithSite**</span></span>](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)
-   [<span data-ttu-id="77037-153">**IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="77037-153">**IPersistStream**</span></span>](/windows/win32/api/objidl/nn-objidl-ipersiststream)

<span data-ttu-id="77037-154">En plus d’inscrire leur identificateur de classe (CLSID), le volet d’exploration et les objets de la bande de bureau doivent également être inscrits pour la catégorie de composant appropriée.</span><span class="sxs-lookup"><span data-stu-id="77037-154">In addition to registering their class identifier (CLSID), the Explorer Bar and desk band objects must also be registered for the appropriate component category.</span></span> <span data-ttu-id="77037-155">L’inscription de la catégorie de composant détermine le type de l’objet et son conteneur.</span><span class="sxs-lookup"><span data-stu-id="77037-155">Registering the component category determines the object type and its container.</span></span> <span data-ttu-id="77037-156">Les bandes d’outils utilisent une autre procédure d’inscription et n’ont pas d’identificateur de catégorie (CATID).</span><span class="sxs-lookup"><span data-stu-id="77037-156">Tool bands use a different registration procedure and do not have a category identifier (CATID).</span></span> <span data-ttu-id="77037-157">Les CATID des objets à trois bandes qui en ont besoin sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="77037-157">The CATIDs for the three band objects that require them are:</span></span>



| <span data-ttu-id="77037-158">Type de bande</span><span class="sxs-lookup"><span data-stu-id="77037-158">Band Type</span></span>               | <span data-ttu-id="77037-159">Catégorie de composant</span><span class="sxs-lookup"><span data-stu-id="77037-159">Component Category</span></span> |
|-------------------------|--------------------|
| <span data-ttu-id="77037-160">Barre d’explorateur verticale</span><span class="sxs-lookup"><span data-stu-id="77037-160">Vertical Explorer Bar</span></span>   | <span data-ttu-id="77037-161">InfoBand CATID \_</span><span class="sxs-lookup"><span data-stu-id="77037-161">CATID\_InfoBand</span></span>    |
| <span data-ttu-id="77037-162">Barre d’explorateur horizontale</span><span class="sxs-lookup"><span data-stu-id="77037-162">Horizontal Explorer Bar</span></span> | <span data-ttu-id="77037-163">CommBand CATID \_</span><span class="sxs-lookup"><span data-stu-id="77037-163">CATID\_CommBand</span></span>    |
| <span data-ttu-id="77037-164">Bande de bureau</span><span class="sxs-lookup"><span data-stu-id="77037-164">Desk Band</span></span>               | <span data-ttu-id="77037-165">Deskband CATID \_</span><span class="sxs-lookup"><span data-stu-id="77037-165">CATID\_DeskBand</span></span>    |



 

<span data-ttu-id="77037-166">Pour plus d’informations sur la façon d’inscrire des objets de bande, consultez enregistrement de la [bande](#band-registration) .</span><span class="sxs-lookup"><span data-stu-id="77037-166">See [Band Registration](#band-registration) for further discussion of how to register band objects.</span></span>

<span data-ttu-id="77037-167">Si l’objet de bande doit accepter l’entrée d’utilisateur, il doit également implémenter [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject).</span><span class="sxs-lookup"><span data-stu-id="77037-167">If the band object is to accept user input, it must also implement [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject).</span></span> <span data-ttu-id="77037-168">Pour ajouter des éléments au menu contextuel pour la barre d’explorateur ou les bandes de bureau, l’objet Band doit exporter [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span><span class="sxs-lookup"><span data-stu-id="77037-168">To add items to the shortcut menu for Explorer Bar or desk bands, the band object must export [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span> <span data-ttu-id="77037-169">Les bandes d’outils ne prennent pas en charge les menus contextuels.</span><span class="sxs-lookup"><span data-stu-id="77037-169">Tool bands do not support shortcut menus.</span></span>

<span data-ttu-id="77037-170">Étant donné que les objets de bande implémentent une fenêtre enfant, ils doivent également implémenter une procédure de fenêtre pour gérer Windows Messaging.</span><span class="sxs-lookup"><span data-stu-id="77037-170">Because band objects implement a child window, they must also implement a window procedure to handle Windows messaging.</span></span>

<span data-ttu-id="77037-171">Les objets Band peuvent envoyer des commandes à leur conteneur par le biais de l’interface [**IOleCommandTarget**](/windows/win32/api/docobj/nn-docobj-iolecommandtarget) du conteneur.</span><span class="sxs-lookup"><span data-stu-id="77037-171">Band objects can send commands to their container through the container's [**IOleCommandTarget**](/windows/win32/api/docobj/nn-docobj-iolecommandtarget) interface.</span></span> <span data-ttu-id="77037-172">Pour obtenir le pointeur d’interface, appelez la méthode [**IInputObjectSite :: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) du conteneur et demandez l’IID \_ IOleCommandTarget.</span><span class="sxs-lookup"><span data-stu-id="77037-172">To obtain the interface pointer, call the container's [**IInputObjectSite::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method and ask for IID\_IOleCommandTarget.</span></span> <span data-ttu-id="77037-173">Vous envoyez ensuite des commandes au conteneur avec [**IOleCommandTarget :: exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec).</span><span class="sxs-lookup"><span data-stu-id="77037-173">You then send commands to the container with [**IOleCommandTarget::Exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec).</span></span> <span data-ttu-id="77037-174">Le groupe de commandes est CGID \_ Deskband.</span><span class="sxs-lookup"><span data-stu-id="77037-174">The command group is CGID\_DeskBand.</span></span> <span data-ttu-id="77037-175">Quand la méthode [**IDeskBand :: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) d’un objet Band est appelée, le conteneur utilise le paramètre *dwBandID* pour affecter à l’objet Band un identificateur utilisé pour trois des commandes.</span><span class="sxs-lookup"><span data-stu-id="77037-175">When a band object's [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) method is called, the container uses the *dwBandID* parameter to assign the band object an identifier that is used for three of the commands.</span></span> <span data-ttu-id="77037-176">Quatre ID de commande **IOleCommandTarget :: exec** sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="77037-176">Four **IOleCommandTarget::Exec** command IDs are supported.</span></span>

-   <span data-ttu-id="77037-177">DBID \_ BANDINFOCHANGED</span><span class="sxs-lookup"><span data-stu-id="77037-177">DBID\_BANDINFOCHANGED</span></span>

    <span data-ttu-id="77037-178">Les informations de la bande ont changé.</span><span class="sxs-lookup"><span data-stu-id="77037-178">The band's information has changed.</span></span> <span data-ttu-id="77037-179">Définissez le paramètre *pvaIn* sur l’identificateur de bande reçu lors de l’appel le plus récent à [**IDeskBand :: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span><span class="sxs-lookup"><span data-stu-id="77037-179">Set the *pvaIn* parameter to the band identifier that was received in the most recent call to [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span></span> <span data-ttu-id="77037-180">Le conteneur appellera la méthode **IDeskBand :: GetBandInfo** de l’objet de la bande pour demander les informations mises à jour.</span><span class="sxs-lookup"><span data-stu-id="77037-180">The container will call the band object's **IDeskBand::GetBandInfo** method to request the updated information.</span></span>

-   <span data-ttu-id="77037-181">DBID \_ MAXIMIZEBAND</span><span class="sxs-lookup"><span data-stu-id="77037-181">DBID\_MAXIMIZEBAND</span></span>

    <span data-ttu-id="77037-182">Agrandissez la bande.</span><span class="sxs-lookup"><span data-stu-id="77037-182">Maximize the band.</span></span> <span data-ttu-id="77037-183">Définissez le paramètre *pvaIn* sur l’identificateur de bande reçu lors de l’appel le plus récent à [**IDeskBand :: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span><span class="sxs-lookup"><span data-stu-id="77037-183">Set the *pvaIn* parameter to the band identifier that was received in the most recent call to [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span></span>

-   <span data-ttu-id="77037-184">DBID \_ SHOWONLY</span><span class="sxs-lookup"><span data-stu-id="77037-184">DBID\_SHOWONLY</span></span>

    <span data-ttu-id="77037-185">Activez ou désactivez les autres bandes dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="77037-185">Turn other bands in the container on or off.</span></span> <span data-ttu-id="77037-186">Définissez le paramètre *pvaIn* sur le \_ type VT inconnu avec l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="77037-186">Set the *pvaIn* parameter to the VT\_UNKNOWN type with one of the following values:</span></span>

    

    | <span data-ttu-id="77037-187">Valeur</span><span class="sxs-lookup"><span data-stu-id="77037-187">Value</span></span> | <span data-ttu-id="77037-188">Description</span><span class="sxs-lookup"><span data-stu-id="77037-188">Description</span></span>                                                                                                 |
    |-------|-------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="77037-189">pUnk</span><span class="sxs-lookup"><span data-stu-id="77037-189">pUnk</span></span>  | <span data-ttu-id="77037-190">Pointeur vers l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) de l’objet de bande.</span><span class="sxs-lookup"><span data-stu-id="77037-190">A pointer to the band object's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="77037-191">Toutes les autres bandes de bureau seront masquées.</span><span class="sxs-lookup"><span data-stu-id="77037-191">All other desk bands will be hidden.</span></span> |
    | <span data-ttu-id="77037-192">0</span><span class="sxs-lookup"><span data-stu-id="77037-192">0</span></span>     | <span data-ttu-id="77037-193">Masquer toutes les bandes de bureau.</span><span class="sxs-lookup"><span data-stu-id="77037-193">Hide all desk bands.</span></span>                                                                                        |
    | <span data-ttu-id="77037-194">1</span><span class="sxs-lookup"><span data-stu-id="77037-194">1</span></span>     | <span data-ttu-id="77037-195">Afficher toutes les bandes de bureau.</span><span class="sxs-lookup"><span data-stu-id="77037-195">Show all desk bands.</span></span>                                                                                        |

    

     

-   <span data-ttu-id="77037-196">DBID \_ PUSHCHEVRON</span><span class="sxs-lookup"><span data-stu-id="77037-196">DBID\_PUSHCHEVRON</span></span>

    <span data-ttu-id="77037-197">[Version 5](versions.md).</span><span class="sxs-lookup"><span data-stu-id="77037-197">[Version 5](versions.md).</span></span> <span data-ttu-id="77037-198">Affichez un menu Chevron.</span><span class="sxs-lookup"><span data-stu-id="77037-198">Display a chevron menu.</span></span> <span data-ttu-id="77037-199">Le conteneur envoie un message [**RB \_ PUSHCHEVRON**](../controls/rb-pushchevron.md) et l’objet Band reçoit une notification [ \_ CHEVRONPUSHED RBN](../controls/rbn-chevronpushed.md) qui lui invite à afficher le menu Chevron.</span><span class="sxs-lookup"><span data-stu-id="77037-199">The container sends an [**RB\_PUSHCHEVRON**](../controls/rb-pushchevron.md) message, and the band object receives an [RBN\_CHEVRONPUSHED](../controls/rbn-chevronpushed.md) notification that prompts it to display the chevron menu.</span></span> <span data-ttu-id="77037-200">Définissez le paramètre *nCmdExecOpt* de la méthode [**IOleCommandTarget :: exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec) sur l’identificateur de bande reçu lors de l’appel le plus récent à [**IDeskBand :: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span><span class="sxs-lookup"><span data-stu-id="77037-200">Set the [**IOleCommandTarget::Exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec) method's *nCmdExecOpt* parameter to the band identifier received in the most recent call to [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span></span> <span data-ttu-id="77037-201">Définissez le paramètre *pvaIn* de la méthode **IOleCommandTarget :: exec** sur le \_ type VT I4 avec une valeur définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="77037-201">Set the **IOleCommandTarget::Exec** method's *pvaIn* parameter to the VT\_I4 type with an application-defined value.</span></span> <span data-ttu-id="77037-202">Elle est retransmise à l’objet de bande comme valeur *lAppValue* de la \_ notification CHEVRONPUSHED RBN.</span><span class="sxs-lookup"><span data-stu-id="77037-202">It passes back to the band object as the *lAppValue* value of the RBN\_CHEVRONPUSHED notification.</span></span>

### <a name="band-registration"></a><span data-ttu-id="77037-203">Enregistrement de la bande</span><span class="sxs-lookup"><span data-stu-id="77037-203">Band Registration</span></span>

<span data-ttu-id="77037-204">Un objet de bande doit être inscrit en tant que serveur OLE in-process qui prend en charge le thread cloisonné.</span><span class="sxs-lookup"><span data-stu-id="77037-204">A band object must be registered as an OLE in-process server that supports apartment threading.</span></span> <span data-ttu-id="77037-205">La valeur par défaut pour le serveur est une chaîne de texte de menu.</span><span class="sxs-lookup"><span data-stu-id="77037-205">The default value for the server is a menu text string.</span></span> <span data-ttu-id="77037-206">Pour les barres d’exploration, elles s’affichent dans le sous-menu du **volet d’exploration** du menu **affichage** d’Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="77037-206">For Explorer Bars, it will appear in the **Explorer Bar** submenu of the Internet Explorer **View** menu.</span></span> <span data-ttu-id="77037-207">Pour les bandes d’outils, elles s’affichent dans le sous-menu **barres d’outils** du menu **affichage** d’Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="77037-207">For tool bands, it will appear in the **Toolbars** submenu of the Internet Explorer **View** menu.</span></span> <span data-ttu-id="77037-208">Pour les bandes de bureau, elles s’affichent dans le sous-menu **barres d’outils** du menu contextuel de la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="77037-208">For desk bands, it will appear in the **Toolbars** submenu of the taskbar's shortcut menu.</span></span> <span data-ttu-id="77037-209">Comme pour les ressources de menu, le fait de placer un et commercial (&) devant une lettre est alors souligné et active les raccourcis clavier.</span><span class="sxs-lookup"><span data-stu-id="77037-209">As with menu resources, placing an ampersand (&) in front of a letter will cause it to be underlined and enable keyboard shortcuts.</span></span> <span data-ttu-id="77037-210">Par exemple, la chaîne de menu de la barre d’explorateur verticale affichée dans le premier graphique est « exemple &barre d’exploration verticale ».</span><span class="sxs-lookup"><span data-stu-id="77037-210">For example, the menu string for the vertical Explorer Bar shown in the first graphic is "Sample &Vertical Explorer Bar".</span></span>

<span data-ttu-id="77037-211">Au départ, Internet Explorer récupère une énumération des objets de la barre d’exploration inscrits à partir du Registre à l’aide des catégories de composants.</span><span class="sxs-lookup"><span data-stu-id="77037-211">Initially, Internet Explorer retrieves an enumeration of the registered Explorer Bar objects from the registry using the component categories.</span></span> <span data-ttu-id="77037-212">Pour améliorer les performances, il met en cache cette énumération, ce qui a pour effet d’ajouter à la suite des barres de l’Explorateur.</span><span class="sxs-lookup"><span data-stu-id="77037-212">To increase performance, it then caches this enumeration, causing subsequently added Explorer Bars to be overlooked.</span></span> <span data-ttu-id="77037-213">Pour forcer Windows Internet Explorer à reconstruire le cache et à reconnaître un nouveau volet d’exploration, supprimez les clés de Registre suivantes lors de l’inscription de la nouvelle barre d’exploration :</span><span class="sxs-lookup"><span data-stu-id="77037-213">To force Windows Internet Explorer to rebuild the cache and recognize a new Explorer Bar, delete the following registry keys during the registration of the new Explorer Bar:</span></span>

<span data-ttu-id="77037-214">**HKEY \_ Logiciel \_ utilisateur actuel** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\  \\ **PostSetup** les \\ **catégories** \\ **de composants de composant {00021493-0000-0000-C000-000000000046}** \\ **enum**</span><span class="sxs-lookup"><span data-stu-id="77037-214">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Explorer**\\**Discardable**\\**PostSetup**\\**Component Categories**\\ **{00021493-0000-0000-C000-000000000046}**\\**Enum**</span></span>

<span data-ttu-id="77037-215">**HKEY \_ Logiciel \_ utilisateur actuel** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\  \\ **PostSetup** les \\ **catégories** \\ **de composants de composant {00021494-0000-0000-C000-000000000046}** \\ **enum**</span><span class="sxs-lookup"><span data-stu-id="77037-215">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Explorer**\\**Discardable**\\**PostSetup**\\**Component Categories**\\ **{00021494-0000-0000-C000-000000000046}**\\**Enum**</span></span>

> [!Note]  
> <span data-ttu-id="77037-216">Étant donné qu’un cache de barre d’exploration est créé pour chaque utilisateur, votre application de configuration doit peut-être énumérer toutes les ruches de Registre utilisateur ou ajouter un stub par utilisateur à exécuter lorsque l’utilisateur se connecte pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="77037-216">Because an Explorer Bar cache is created for each user, your setup application may need to enumerate all the user registry hives or add a per-user stub to run when the user first logs on.</span></span>

 

<span data-ttu-id="77037-217">En général, l’entrée de registre de base pour un objet de bande s’affiche comme suit.</span><span class="sxs-lookup"><span data-stu-id="77037-217">In general, the basic registry entry for a band object will appear as follows.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         (Default) = Menu Text String
         InProcServer32
            (Default) = DLL Path Name
            ThreadingModel = Apartment
```

<span data-ttu-id="77037-218">Le CLSID de l’objet doit également être inscrit auprès d’Internet Explorer pour les bandes d’outils.</span><span class="sxs-lookup"><span data-stu-id="77037-218">Tool bands must also have their object's CLSID registered with Internet Explorer.</span></span> <span data-ttu-id="77037-219">Pour ce faire, affectez une valeur sous la barre d’outils **HKEY \_ local \_ machine** \\ **Software** \\ **Microsoft** \\ **Internet Explorer** \\  avec le GUID CLSID de l’objet de la bande outil, comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="77037-219">To do this, assign a value under **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Internet Explorer**\\**Toolbar** named with the tool band object's CLSID GUID as shown here.</span></span> <span data-ttu-id="77037-220">Comme sa valeur de données est ignorée, le type de valeur n’est pas important.</span><span class="sxs-lookup"><span data-stu-id="77037-220">Its data value is ignored, so the value type is unimportant.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Internet Explorer
            Toolbar
               {Your Band Object's CLSID GUID}
```

<span data-ttu-id="77037-221">Plusieurs valeurs facultatives peuvent également être ajoutées au registre.</span><span class="sxs-lookup"><span data-stu-id="77037-221">There are several optional values that can also be added to the registry.</span></span> <span data-ttu-id="77037-222">Par exemple, la valeur suivante est nécessaire si vous souhaitez utiliser le volet d’exploration pour afficher le code HTML. la valeur affichée n’est pas un exemple, mais la valeur réelle à utiliser.</span><span class="sxs-lookup"><span data-stu-id="77037-222">For instance, the following value is necessary if you want to use the Explorer Bar to display HTML The value shown is not an example, but the actual value that should be used.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            CLSID
               (Default) = {4D5C8C2A-D075-11D0-B416-00C04FB90376}
```

<span data-ttu-id="77037-223">Utilisé conjointement avec la valeur indiquée ci-dessus, la valeur facultative suivante est également nécessaire si vous souhaitez utiliser le volet d’exploration pour afficher du code HTML.</span><span class="sxs-lookup"><span data-stu-id="77037-223">Used in conjunction with the value shown above, the following optional value is also necessary if you want to use the Explorer Bar to display HTML.</span></span> <span data-ttu-id="77037-224">Cette valeur doit être définie sur l’emplacement du fichier qui contient le contenu HTML pour le volet d’exploration.</span><span class="sxs-lookup"><span data-stu-id="77037-224">This value should be set to the location of the file that contains the HTML content for the Explorer Bar.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            InitPropertyBag
               Url
```

<span data-ttu-id="77037-225">Une autre valeur facultative définit la largeur ou la hauteur par défaut du volet d’exploration, selon qu’il est vertical ou horizontal, respectivement.</span><span class="sxs-lookup"><span data-stu-id="77037-225">Another optional value defines the default width or height of the Explorer Bar, depending on whether it is vertical or horizontal, respectively.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Internet Explorer
            Explorer Bars
               {Your Band Object's CLSID GUID}
                  BarSize
```

<span data-ttu-id="77037-226">La valeur de la coordonnée doit être définie sur la largeur ou la hauteur de la barre.</span><span class="sxs-lookup"><span data-stu-id="77037-226">The BarSize value should be set to the width or height of the bar.</span></span> <span data-ttu-id="77037-227">La valeur nécessite huit octets et est placée dans le registre en tant que valeur binaire.</span><span class="sxs-lookup"><span data-stu-id="77037-227">The value requires eight bytes and is placed in the registry as a binary value.</span></span> <span data-ttu-id="77037-228">Les quatre premiers octets spécifient la taille en pixels, au format hexadécimal, à partir de l’octet le plus à gauche.</span><span class="sxs-lookup"><span data-stu-id="77037-228">The first four bytes specify the size in pixels, in hexadecimal format, starting from the leftmost byte.</span></span> <span data-ttu-id="77037-229">Les quatre derniers octets sont réservés et doivent être définis sur zéro.</span><span class="sxs-lookup"><span data-stu-id="77037-229">The last four bytes are reserved and should be set to zero.</span></span>

<span data-ttu-id="77037-230">Par exemple, les entrées de Registre complètes pour un volet d’exploration HTML avec une largeur par défaut de 291 (0X123) pixels sont indiquées ici.</span><span class="sxs-lookup"><span data-stu-id="77037-230">As an example, the full registry entries for an HTML-capable Explorer Bar with a default width of 291 (0x123) pixels are shown here.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         (Default) = Menu Text String
         InProcServer32
            (Default) = DLL Path Name
            ThreadingModel = Apartment
         Instance
            CLSID
               (Default) = {4D5C8C2A-D075-11D0-B416-00C04FB90376}
            InitPropertyBag
               Url = Your HTML File
HKEY_CURRENT_USER
   Software
      Microsoft
         Internet Explorer
            Explorer Bars
               {Your Band Object's CLSID GUID}
                  BarSize = 23 01 00 00 00 00 00 00
```

<span data-ttu-id="77037-231">Vous pouvez gérer l’inscription du CATID d’un objet de bande par programme.</span><span class="sxs-lookup"><span data-stu-id="77037-231">You can handle registration of a band object's CATID programmatically.</span></span> <span data-ttu-id="77037-232">Créez un objet gestionnaire de catégories de composants (CLSID \_ StdComponentCategoriesMgr) et demandez un pointeur vers son interface [**ICatRegister**](/windows/win32/api/comcat/nn-comcat-icatregister) .</span><span class="sxs-lookup"><span data-stu-id="77037-232">Create a component categories manager object (CLSID\_StdComponentCategoriesMgr) and request a pointer to its [**ICatRegister**](/windows/win32/api/comcat/nn-comcat-icatregister) interface.</span></span> <span data-ttu-id="77037-233">Transmettez le CLSID de l’objet de la bande et le CATID à [**ICatRegister :: RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories).</span><span class="sxs-lookup"><span data-stu-id="77037-233">Pass the band object's CLSID and CATID to [**ICatRegister::RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories).</span></span>

### <a name="a-simple-example-of-a-custom-explorer-bar"></a><span data-ttu-id="77037-234">Exemple simple d’une barre d’exploration personnalisée</span><span class="sxs-lookup"><span data-stu-id="77037-234">A Simple Example of a Custom Explorer Bar</span></span>

<span data-ttu-id="77037-235">Cet exemple passe en revue l’implémentation de l’exemple de barre d’exploration verticale présentée dans l’introduction.</span><span class="sxs-lookup"><span data-stu-id="77037-235">This example goes through the implementation of the sample vertical Explorer Bar shown in the introduction.</span></span>

<span data-ttu-id="77037-236">La procédure de base pour créer une barre d’exploration personnalisée est la suivante.</span><span class="sxs-lookup"><span data-stu-id="77037-236">The basic procedure for creating a custom Explorer Bar is as follows.</span></span>

1.  <span data-ttu-id="77037-237">[Implémentez les fonctions nécessaires à la dll](#dll-functions).</span><span class="sxs-lookup"><span data-stu-id="77037-237">[Implement the functions needed by the DLL](#dll-functions).</span></span>
2.  [<span data-ttu-id="77037-238">Implémentez les interfaces COM requises.</span><span class="sxs-lookup"><span data-stu-id="77037-238">Implement the required COM interfaces.</span></span>](#required-interface-implementations)
3.  [<span data-ttu-id="77037-239">Implémentez toutes les interfaces COM facultatives souhaitées.</span><span class="sxs-lookup"><span data-stu-id="77037-239">Implement any desired optional COM interfaces.</span></span>](#optional-interface-implementations)
4.  [<span data-ttu-id="77037-240">Enregistrez le CLSID de l’objet et, si nécessaire, la catégorie du composant.</span><span class="sxs-lookup"><span data-stu-id="77037-240">Register the object's CLSID and, if required, component category.</span></span>](#clsid-registration)
5.  <span data-ttu-id="77037-241">Créer une fenêtre enfant d’Internet Explorer, dimensionnée pour s’ajuster à la zone d’affichage de la barre d’exploration.</span><span class="sxs-lookup"><span data-stu-id="77037-241">Create a child window of Internet Explorer, sized to fit the Explorer Bar's display region.</span></span>
6.  [<span data-ttu-id="77037-242">Utilisez la fenêtre enfant pour afficher des informations et interagir avec l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="77037-242">Use the child window to display information and interact with the user.</span></span>](#the-window-procedure)

<span data-ttu-id="77037-243">L’implémentation très simple utilisée dans l’exemple de volet d’exploration peut être utilisée pour un type de barre d’exploration ou une bande de bureau, en l’inscrivant simplement pour la catégorie de composant appropriée.</span><span class="sxs-lookup"><span data-stu-id="77037-243">The very simple implementation used in the Explorer Bar sample could actually be used for either type of Explorer Bar, or a desk band, by simply registering it for the appropriate component category.</span></span> <span data-ttu-id="77037-244">Des implémentations plus sophistiquées devront être personnalisées pour la région d’affichage et le conteneur de chaque type d’objet.</span><span class="sxs-lookup"><span data-stu-id="77037-244">More sophisticated implementations will need to be customized for each object type's display region and container.</span></span> <span data-ttu-id="77037-245">Toutefois, une grande partie de cette personnalisation peut être accomplie en utilisant l’exemple de code et en l’étendant en appliquant des techniques de programmation Windows familières à la fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="77037-245">However, much of this customization can be accomplished by taking the sample code and extending it by applying familiar Windows programming techniques to the child window.</span></span> <span data-ttu-id="77037-246">Par exemple, vous pouvez ajouter des contrôles pour l’interaction de l’utilisateur ou des graphiques pour un affichage plus riche.</span><span class="sxs-lookup"><span data-stu-id="77037-246">For example, you can add controls for user interaction, or graphics for a richer display.</span></span>

### <a name="dll-functions"></a><span data-ttu-id="77037-247">Fonctions DLL</span><span class="sxs-lookup"><span data-stu-id="77037-247">DLL Functions</span></span>

<span data-ttu-id="77037-248">Les trois objets sont empaquetés dans une seule DLL, qui expose les fonctions suivantes.</span><span class="sxs-lookup"><span data-stu-id="77037-248">All three objects are packaged in a single DLL, which exposes the following functions.</span></span>

-   [<span data-ttu-id="77037-249">**DllMain**</span><span class="sxs-lookup"><span data-stu-id="77037-249">**DllMain**</span></span>](../dlls/dllmain.md)
-   [<span data-ttu-id="77037-250">**DllCanUnloadNow**</span><span class="sxs-lookup"><span data-stu-id="77037-250">**DllCanUnloadNow**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)
-   [<span data-ttu-id="77037-251">**DllGetClassObject**</span><span class="sxs-lookup"><span data-stu-id="77037-251">**DllGetClassObject**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)
-   [<span data-ttu-id="77037-252">**Accompli**</span><span class="sxs-lookup"><span data-stu-id="77037-252">**DllRegisterServer**</span></span>](/windows/win32/api/olectl/nf-olectl-dllregisterserver)

<span data-ttu-id="77037-253">Les trois premières fonctions sont des implémentations standard et ne sont pas abordées ici.</span><span class="sxs-lookup"><span data-stu-id="77037-253">The first three functions are standard implementations and will not be discussed here.</span></span> <span data-ttu-id="77037-254">L’implémentation de la fabrique de classes est également standard.</span><span class="sxs-lookup"><span data-stu-id="77037-254">The Class Factory implementation is also standard.</span></span>

### <a name="required-interface-implementations"></a><span data-ttu-id="77037-255">Implémentations d’interface requises</span><span class="sxs-lookup"><span data-stu-id="77037-255">Required Interface Implementations</span></span>

<span data-ttu-id="77037-256">L’exemple vertical du volet d’exploration implémente les quatre interfaces requises : [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite), [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)et [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) dans le cadre de la classe CExplorerBar.</span><span class="sxs-lookup"><span data-stu-id="77037-256">The vertical Explorer Bar sample implements the four required interfaces: [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite), [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream), and [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) as part of the CExplorerBar class.</span></span> <span data-ttu-id="77037-257">Le constructeur, le destructeur et les implémentations **IUnknown** sont simples et ne seront pas abordés ici.</span><span class="sxs-lookup"><span data-stu-id="77037-257">The constructor, destructor, and **IUnknown** implementations are straightforward, and will not be discussed here.</span></span> <span data-ttu-id="77037-258">Consultez l'exemple de code pour plus d'informations.</span><span class="sxs-lookup"><span data-stu-id="77037-258">See the sample code for details.</span></span>

<span data-ttu-id="77037-259">Les interfaces suivantes sont décrites en détail.</span><span class="sxs-lookup"><span data-stu-id="77037-259">The following interfaces are discussed in detail.</span></span>

-   [<span data-ttu-id="77037-260">IObjectWithSite</span><span class="sxs-lookup"><span data-stu-id="77037-260">IObjectWithSite</span></span>](#iobjectwithsite)
-   [<span data-ttu-id="77037-261">IPersistStream</span><span class="sxs-lookup"><span data-stu-id="77037-261">IPersistStream</span></span>](#ipersiststream)
-   [<span data-ttu-id="77037-262">IDeskBand</span><span class="sxs-lookup"><span data-stu-id="77037-262">IDeskBand</span></span>](#ideskband)

### <a name="iobjectwithsite"></a><span data-ttu-id="77037-263">IObjectWithSite</span><span class="sxs-lookup"><span data-stu-id="77037-263">IObjectWithSite</span></span>

<span data-ttu-id="77037-264">Quand l’utilisateur sélectionne une barre d’exploration, le conteneur appelle la méthode [**IObjectWithSite :: SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) correspondante de l’objet de bande.</span><span class="sxs-lookup"><span data-stu-id="77037-264">When the user selects an Explorer Bar, the container calls the corresponding band object's [**IObjectWithSite::SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) method.</span></span> <span data-ttu-id="77037-265">Le paramètre *punkSite* est défini sur le pointeur [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) du site.</span><span class="sxs-lookup"><span data-stu-id="77037-265">The *punkSite* parameter will be set to the site's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer.</span></span>

<span data-ttu-id="77037-266">En général, une implémentation de [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) doit effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="77037-266">In general, a [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) implementation should perform the following steps:</span></span>

1.  <span data-ttu-id="77037-267">Libère tout pointeur de site qui est actuellement détenu.</span><span class="sxs-lookup"><span data-stu-id="77037-267">Release any site pointer that is currently being held.</span></span>
2.  <span data-ttu-id="77037-268">Si le pointeur passé à [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) a la valeur **null**, la bande est en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="77037-268">If the pointer passed to [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) is set to **NULL**, the band is being removed.</span></span> <span data-ttu-id="77037-269">**SetSite** peut retourner S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="77037-269">**SetSite** can return S\_OK.</span></span>
3.  <span data-ttu-id="77037-270">Si le pointeur passé à [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) est non **null**, un nouveau site est défini.</span><span class="sxs-lookup"><span data-stu-id="77037-270">If the pointer passed to [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) is non-**NULL**, a new site is being set.</span></span> <span data-ttu-id="77037-271">La **SetSite** doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="77037-271">**SetSite** should do the following:</span></span>
    1.  <span data-ttu-id="77037-272">Appelez [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur le site pour son interface [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) .</span><span class="sxs-lookup"><span data-stu-id="77037-272">Call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the site for its [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) interface.</span></span>
    2.  <span data-ttu-id="77037-273">Appelez [**IOleWindow :: GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) pour obtenir le handle de la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="77037-273">Call [**IOleWindow::GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) to obtain the parent window's handle.</span></span> <span data-ttu-id="77037-274">Enregistrez le descripteur pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="77037-274">Save the handle for later use.</span></span> <span data-ttu-id="77037-275">Release [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) si elle n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="77037-275">Release [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) if it is no longer needed.</span></span>
    3.  <span data-ttu-id="77037-276">Créez la fenêtre de l’objet de la bande en tant qu’enfant de la fenêtre obtenue à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="77037-276">Create the band object's window as a child of the window obtained in the previous step.</span></span> <span data-ttu-id="77037-277">Ne le créez pas en tant que fenêtre visible.</span><span class="sxs-lookup"><span data-stu-id="77037-277">Do not create it as a visible window.</span></span>
    4.  <span data-ttu-id="77037-278">Si l’objet de bande implémente [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject), appelez [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur le site pour son interface [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) .</span><span class="sxs-lookup"><span data-stu-id="77037-278">If the band object implements [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject), call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the site for its [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) interface.</span></span> <span data-ttu-id="77037-279">Stockez le pointeur vers cette interface pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="77037-279">Store the pointer to this interface for use later.</span></span>
    5.  <span data-ttu-id="77037-280">Si toutes les étapes sont réussies, l’opération retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="77037-280">If all steps are successful, return S\_OK.</span></span> <span data-ttu-id="77037-281">Si ce n’est pas le cas, retournez le code d’erreur défini par OLE indiquant ce qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="77037-281">If not, return the OLE-defined error code indicating what failed.</span></span>

<span data-ttu-id="77037-282">L’exemple de volet d’exploration implémente [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) de la façon suivante.</span><span class="sxs-lookup"><span data-stu-id="77037-282">The Explorer Bar sample implements [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) in the following way.</span></span> <span data-ttu-id="77037-283">Dans le code m suivant, *\_ pSite* est une variable membre privée qui contient le pointeur [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) et *m \_ hwndParent* contient le handle de la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="77037-283">In the following code *m\_pSite* is a private member variable that holds the [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) pointer and *m\_hwndParent* holds the parent window's handle.</span></span> <span data-ttu-id="77037-284">Dans cet exemple, la création de fenêtres est également gérée.</span><span class="sxs-lookup"><span data-stu-id="77037-284">In this sample, window creation is also handled.</span></span> <span data-ttu-id="77037-285">Si la fenêtre n’existe pas, cette méthode crée la fenêtre de la barre d’exploration en tant qu’enfant de taille appropriée de la fenêtre parente obtenue par **SetSite**.</span><span class="sxs-lookup"><span data-stu-id="77037-285">If the window does not exist, this method creates the Explorer Bar's window as an appropriately sized child of the parent window obtained by **SetSite**.</span></span> <span data-ttu-id="77037-286">Le handle de la fenêtre enfant est stocké dans *m \_ HWND*.</span><span class="sxs-lookup"><span data-stu-id="77037-286">The child window's handle is stored in *m\_hwnd*.</span></span>


```C++
STDMETHODIMP CDeskBand::SetSite(IUnknown *pUnkSite)
{
    HRESULT hr = S_OK;

    m_hwndParent = NULL;

    if (m_pSite)
    {
        m_pSite->Release();
    }

    if (pUnkSite)
    {
        IOleWindow *pow;
        hr = pUnkSite->QueryInterface(IID_IOleWindow, reinterpret_cast<void **>(&pow));
        if (SUCCEEDED(hr))
        {
            hr = pow->GetWindow(&m_hwndParent);
            if (SUCCEEDED(hr))
            {
                WNDCLASSW wc = { 0 };
                wc.style         = CS_HREDRAW | CS_VREDRAW;
                wc.hCursor       = LoadCursor(NULL, IDC_ARROW);
                wc.hInstance     = g_hInst;
                wc.lpfnWndProc   = WndProc;
                wc.lpszClassName = g_szDeskBandSampleClass;
                wc.hbrBackground = CreateSolidBrush(RGB(255, 255, 0));

                RegisterClassW(&wc);

                CreateWindowExW(0,
                                g_szDeskBandSampleClass,
                                NULL,
                                WS_CHILD | WS_CLIPCHILDREN | WS_CLIPSIBLINGS,
                                0,
                                0,
                                0,
                                0,
                                m_hwndParent,
                                NULL,
                                g_hInst,
                                this);

                if (!m_hwnd)
                {
                    hr = E_FAIL;
                }
            }

            pow->Release();
        }

        hr = pUnkSite->QueryInterface(IID_IInputObjectSite, reinterpret_cast<void **>(&m_pSite));
    }

    return hr;
}
```



<span data-ttu-id="77037-287">L’implémentation [**GetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-getsite) de l’exemple encapsule simplement un appel à la méthode [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) du site, à l’aide du pointeur de site enregistré par [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite).</span><span class="sxs-lookup"><span data-stu-id="77037-287">The sample's [**GetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-getsite) implementation simply wraps a call to the site's [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method, using the site pointer saved by [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite).</span></span>


```C++
STDMETHODIMP CDeskBand::GetSite(REFIID riid, void **ppv)
{
    HRESULT hr = E_FAIL;

    if (m_pSite)
    {
        hr =  m_pSite->QueryInterface(riid, ppv);
    }
    else
    {
        *ppv = NULL;
    }

    return hr;
}
```



### <a name="ipersiststream"></a><span data-ttu-id="77037-288">IPersistStream</span><span class="sxs-lookup"><span data-stu-id="77037-288">IPersistStream</span></span>

<span data-ttu-id="77037-289">Internet Explorer appellera l’interface [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) de la barre d’explorateur pour permettre au volet d’exploration de charger ou d’enregistrer les données persistantes.</span><span class="sxs-lookup"><span data-stu-id="77037-289">Internet Explorer will call the Explorer Bar's [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) interface to allow the Explorer Bar to load or save persistent data.</span></span> <span data-ttu-id="77037-290">S’il n’y a pas de données persistantes, les méthodes doivent toujours retourner un code de réussite.</span><span class="sxs-lookup"><span data-stu-id="77037-290">If there is no persistent data, the methods must still return a success code.</span></span> <span data-ttu-id="77037-291">L’interface **IPersistStream** hérite d' [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), donc cinq méthodes doivent être implémentées.</span><span class="sxs-lookup"><span data-stu-id="77037-291">The **IPersistStream** interface inherits from [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), so five methods must be implemented.</span></span>

-   [<span data-ttu-id="77037-292">**IPersist :: GetClassID**</span><span class="sxs-lookup"><span data-stu-id="77037-292">**IPersist::GetClassID**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid)
-   [<span data-ttu-id="77037-293">**IPersistStream :: IsDirty**</span><span class="sxs-lookup"><span data-stu-id="77037-293">**IPersistStream::IsDirty**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersiststream-isdirty)
-   [<span data-ttu-id="77037-294">**IPersistStream :: Load**</span><span class="sxs-lookup"><span data-stu-id="77037-294">**IPersistStream::Load**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersiststream-load)
-   [<span data-ttu-id="77037-295">**IPersistStream :: Save**</span><span class="sxs-lookup"><span data-stu-id="77037-295">**IPersistStream::Save**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersiststream-save)
-   [<span data-ttu-id="77037-296">**IPersistStream :: GetSizeMax**</span><span class="sxs-lookup"><span data-stu-id="77037-296">**IPersistStream::GetSizeMax**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersiststream-getsizemax)

<span data-ttu-id="77037-297">L’exemple de volet d’exploration n’utilise pas de données persistantes et n’a qu’une implémentation minimale d' [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream).</span><span class="sxs-lookup"><span data-stu-id="77037-297">The Explorer Bar sample does not use any persistent data and has only a minimal implementation of [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream).</span></span> <span data-ttu-id="77037-298">[**IPersist :: GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) retourne le CLSID de l’objet (CLSID \_ SampleExplorerBar) et le reste retourne soit S \_ OK, s \_ false, soit E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="77037-298">[**IPersist::GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) returns the object's CLSID (CLSID\_SampleExplorerBar), and the remainder return either S\_OK, S\_FALSE, or E\_NOTIMPL.</span></span>

### <a name="ideskband"></a><span data-ttu-id="77037-299">IDeskBand</span><span class="sxs-lookup"><span data-stu-id="77037-299">IDeskBand</span></span>

<span data-ttu-id="77037-300">L’interface [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) est spécifique aux objets Band.</span><span class="sxs-lookup"><span data-stu-id="77037-300">The [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) interface is specific to band objects.</span></span> <span data-ttu-id="77037-301">En plus de sa méthode, elle hérite de [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow), qui à son tour hérite de [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow).</span><span class="sxs-lookup"><span data-stu-id="77037-301">In addition to its one method, it inherits from [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow), which in turn inherits from [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow).</span></span>

<span data-ttu-id="77037-302">Il existe deux méthodes [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) : [**GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) et [**IOleWindow :: ContextSensitiveHelp**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-contextsensitivehelp).</span><span class="sxs-lookup"><span data-stu-id="77037-302">There are two [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) methods: [**GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) and [**IOleWindow::ContextSensitiveHelp**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-contextsensitivehelp).</span></span> <span data-ttu-id="77037-303">L’implémentation de **GetWindow** de l’exemple de volet d’exploration retourne le handle de fenêtre enfant de la barre d’exploration, *m \_ HWND*.</span><span class="sxs-lookup"><span data-stu-id="77037-303">The Explorer Bar sample's implementation of **GetWindow** returns the Explorer Bar's child window handle, *m\_hwnd*.</span></span> <span data-ttu-id="77037-304">L’aide contextuelle n’étant pas implémentée, **ContextSensitiveHelp** retourne **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="77037-304">Context-sensitive Help is not implemented, so **ContextSensitiveHelp** returns **E\_NOTIMPL**.</span></span>

<span data-ttu-id="77037-305">L’interface [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) a trois méthodes.</span><span class="sxs-lookup"><span data-stu-id="77037-305">The [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface has three methods.</span></span>

-   [<span data-ttu-id="77037-306">**IDockingWindow::ShowDW**</span><span class="sxs-lookup"><span data-stu-id="77037-306">**IDockingWindow::ShowDW**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw)
-   [<span data-ttu-id="77037-307">**IDockingWindow::CloseDW**</span><span class="sxs-lookup"><span data-stu-id="77037-307">**IDockingWindow::CloseDW**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw)
-   [<span data-ttu-id="77037-308">**IDockingWindow::ResizeBorderDW**</span><span class="sxs-lookup"><span data-stu-id="77037-308">**IDockingWindow::ResizeBorderDW**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw)

<span data-ttu-id="77037-309">La méthode [**ResizeBorderDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw) n’est pas utilisée avec un type d’objet Band et doit toujours retourner E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="77037-309">The [**ResizeBorderDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw) method is not used with any type of band object and should always return E\_NOTIMPL.</span></span> <span data-ttu-id="77037-310">La méthode [**ShowDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw) affiche ou masque la fenêtre de la barre d’exploration, en fonction de la valeur de son paramètre.</span><span class="sxs-lookup"><span data-stu-id="77037-310">The [**ShowDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw) method either shows or hides the Explorer Bar's window, depending on the value of its parameter.</span></span>


```C++
STDMETHODIMP CDeskBand::ShowDW(BOOL fShow)
{
    if (m_hwnd)
    {
        ShowWindow(m_hwnd, fShow ? SW_SHOW : SW_HIDE);
    }

    return S_OK;
}
```



<span data-ttu-id="77037-311">La méthode [**CloseDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw) détruit la fenêtre de la barre d’exploration.</span><span class="sxs-lookup"><span data-stu-id="77037-311">The [**CloseDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw) method destroys the Explorer Bar's window.</span></span>


```C++
STDMETHODIMP CDeskBand::CloseDW(DWORD)
{
    if (m_hwnd)
    {
        ShowWindow(m_hwnd, SW_HIDE);
        DestroyWindow(m_hwnd);
        m_hwnd = NULL;
    }

    return S_OK;
}
```



<span data-ttu-id="77037-312">La méthode restante, [**GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband), est spécifique à **IDeskBand**.</span><span class="sxs-lookup"><span data-stu-id="77037-312">The remaining method, [**GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband), is specific to **IDeskBand**.</span></span> <span data-ttu-id="77037-313">Internet Explorer l’utilise pour spécifier l’identificateur et le mode d’affichage de la barre d’exploration.</span><span class="sxs-lookup"><span data-stu-id="77037-313">Internet Explorer uses it to specify the Explorer Bar's identifier and viewing mode.</span></span> <span data-ttu-id="77037-314">Internet Explorer peut également demander une ou plusieurs informations à partir du volet de l’Explorateur en remplissant le membre **dwMask** de la structure [**DESKBANDINFO**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-deskbandinfo) qui est passée comme troisième paramètre.</span><span class="sxs-lookup"><span data-stu-id="77037-314">Internet Explorer also may request one or more pieces of information from the Explorer Bar by filling the **dwMask** member of the [**DESKBANDINFO**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-deskbandinfo) structure that is passed as the third parameter.</span></span> <span data-ttu-id="77037-315">**GetBandInfo** doit stocker l’identificateur et le mode d’affichage, et remplir la structure **DESKBANDINFO** avec les données demandées.</span><span class="sxs-lookup"><span data-stu-id="77037-315">**GetBandInfo** should store the identifier and viewing mode and fill the **DESKBANDINFO** structure with the requested data.</span></span> <span data-ttu-id="77037-316">L’exemple de volet d’exploration implémente **GetBandInfo** comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="77037-316">The Explorer Bar sample implements **GetBandInfo** as shown in the following code example.</span></span>


```C++
STDMETHODIMP CDeskBand::GetBandInfo(DWORD dwBandID, DWORD, DESKBANDINFO *pdbi)
{
    HRESULT hr = E_INVALIDARG;

    if (pdbi)
    {
        m_dwBandID = dwBandID;

        if (pdbi->dwMask & DBIM_MINSIZE)
        {
            pdbi->ptMinSize.x = 200;
            pdbi->ptMinSize.y = 30;
        }

        if (pdbi->dwMask & DBIM_MAXSIZE)
        {
            pdbi->ptMaxSize.y = -1;
        }

        if (pdbi->dwMask & DBIM_INTEGRAL)
        {
            pdbi->ptIntegral.y = 1;
        }

        if (pdbi->dwMask & DBIM_ACTUAL)
        {
            pdbi->ptActual.x = 200;
            pdbi->ptActual.y = 30;
        }

        if (pdbi->dwMask & DBIM_TITLE)
        {
            // Don't show title by removing this flag.
            pdbi->dwMask &= ~DBIM_TITLE;
        }

        if (pdbi->dwMask & DBIM_MODEFLAGS)
        {
            pdbi->dwModeFlags = DBIMF_NORMAL | DBIMF_VARIABLEHEIGHT;
        }

        if (pdbi->dwMask & DBIM_BKCOLOR)
        {
            // Use the default background color by removing this flag.
            pdbi->dwMask &= ~DBIM_BKCOLOR;
        }

        hr = S_OK;
    }

    return hr;
}
```



### <a name="optional-interface-implementations"></a><span data-ttu-id="77037-317">Implémentations d’interface facultatives</span><span class="sxs-lookup"><span data-stu-id="77037-317">Optional Interface Implementations</span></span>

<span data-ttu-id="77037-318">Il existe deux interfaces qui ne sont pas requises, mais qui peuvent être utiles pour implémenter : [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) et [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span><span class="sxs-lookup"><span data-stu-id="77037-318">There are two interfaces that are not required, but that may be useful to implement: [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) and [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span> <span data-ttu-id="77037-319">L’exemple de volet d’exploration implémente **IInputObject**.</span><span class="sxs-lookup"><span data-stu-id="77037-319">The Explorer Bar sample implements **IInputObject**.</span></span> <span data-ttu-id="77037-320">Reportez-vous à la documentation pour plus d’informations sur l’implémentation de **IContextMenu**.</span><span class="sxs-lookup"><span data-stu-id="77037-320">Refer to the documentation for information on how to implement **IContextMenu**.</span></span>

### <a name="iinputobject"></a><span data-ttu-id="77037-321">IInputObject</span><span class="sxs-lookup"><span data-stu-id="77037-321">IInputObject</span></span>

<span data-ttu-id="77037-322">L’interface [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) doit être implémentée si un objet Band accepte une entrée d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="77037-322">The [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) interface must be implemented if a band object accepts user input.</span></span> <span data-ttu-id="77037-323">Internet Explorer implémente [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) et utilise **IInputObject** pour maintenir le focus d’entrée d’utilisateur approprié lorsqu’il a plusieurs fenêtres contenues.</span><span class="sxs-lookup"><span data-stu-id="77037-323">Internet Explorer implements [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) and uses **IInputObject** to maintain proper user input focus when it has more than one contained window.</span></span> <span data-ttu-id="77037-324">Il existe trois méthodes qui doivent être implémentées par une barre d’exploration.</span><span class="sxs-lookup"><span data-stu-id="77037-324">There are three methods that need to be implemented by an Explorer Bar.</span></span>

-   [<span data-ttu-id="77037-325">**IInputObject::UIActivateIO**</span><span class="sxs-lookup"><span data-stu-id="77037-325">**IInputObject::UIActivateIO**</span></span>](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio)
-   [<span data-ttu-id="77037-326">**IInputObject::HasFocusIO**</span><span class="sxs-lookup"><span data-stu-id="77037-326">**IInputObject::HasFocusIO**</span></span>](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio)
-   [<span data-ttu-id="77037-327">**IInputObject::TranslateAcceleratorIO**</span><span class="sxs-lookup"><span data-stu-id="77037-327">**IInputObject::TranslateAcceleratorIO**</span></span>](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio)

<span data-ttu-id="77037-328">Internet Explorer appelle [**UIActivateIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio) pour informer le volet d’exploration qu’il est en cours d’activation ou de désactivation.</span><span class="sxs-lookup"><span data-stu-id="77037-328">Internet Explorer calls [**UIActivateIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio) to inform the Explorer Bar that it is being activated or deactivated.</span></span> <span data-ttu-id="77037-329">Lorsqu’il est activé, l’exemple de volet d’exploration appelle [**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus) pour définir le focus sur sa fenêtre.</span><span class="sxs-lookup"><span data-stu-id="77037-329">When activated, the Explorer Bar sample calls [**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus) to set the focus to its window.</span></span>

<span data-ttu-id="77037-330">Internet Explorer appelle [**HasFocusIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio) lorsqu’il tente de déterminer la fenêtre qui a le focus.</span><span class="sxs-lookup"><span data-stu-id="77037-330">Internet Explorer calls [**HasFocusIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio) when it is attempting to determine which window has focus.</span></span> <span data-ttu-id="77037-331">Si la fenêtre de la barre d’exploration ou l’un de ses descendants a le focus, **HasFocusIO** doit retourner s \_ OK.</span><span class="sxs-lookup"><span data-stu-id="77037-331">If the Explorer Bar's window or one of its descendants has focus, **HasFocusIO** should return S\_OK.</span></span> <span data-ttu-id="77037-332">Si ce n’est pas le cas, elle doit retourner S \_ false.</span><span class="sxs-lookup"><span data-stu-id="77037-332">If not, it should return S\_FALSE.</span></span>

<span data-ttu-id="77037-333">[**TranslateAcceleratorIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio) permet à l’objet de traiter des accélérateurs de clavier.</span><span class="sxs-lookup"><span data-stu-id="77037-333">[**TranslateAcceleratorIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio) allows the object to process keyboard accelerators.</span></span> <span data-ttu-id="77037-334">L’exemple de volet d’exploration n’implémente pas cette méthode. il retourne alors S \_ false.</span><span class="sxs-lookup"><span data-stu-id="77037-334">The Explorer Bar sample does not implement this method, so it returns S\_FALSE.</span></span>

<span data-ttu-id="77037-335">L’implémentation de la barre d’exemple de [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) est la suivante.</span><span class="sxs-lookup"><span data-stu-id="77037-335">The sample bar's implementation of [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) is as follows.</span></span>


```C++
STDMETHODIMP CDeskBand::UIActivateIO(BOOL fActivate, MSG *)
{
    if (fActivate)
    {
        SetFocus(m_hwnd);
    }

    return S_OK;
}

STDMETHODIMP CDeskBand::HasFocusIO()
{
    return m_fHasFocus ? S_OK : S_FALSE;
}

STDMETHODIMP CDeskBand::TranslateAcceleratorIO(MSG *)
{
    return S_FALSE;
};
```



### <a name="clsid-registration"></a><span data-ttu-id="77037-336">Inscription du CLSID</span><span class="sxs-lookup"><span data-stu-id="77037-336">CLSID Registration</span></span>

<span data-ttu-id="77037-337">Comme pour tous les objets COM, le CLSID de la barre d’exploration doit être enregistré.</span><span class="sxs-lookup"><span data-stu-id="77037-337">As with all COM objects, the Explorer Bar's CLSID must be registered.</span></span> <span data-ttu-id="77037-338">Pour que l’objet fonctionne correctement avec Internet Explorer, il doit également être inscrit pour la catégorie de composant appropriée (CATID \_ InfoBand).</span><span class="sxs-lookup"><span data-stu-id="77037-338">For the object to function properly with Internet Explorer, it must also be registered for the appropriate component category (CATID\_InfoBand).</span></span> <span data-ttu-id="77037-339">La section de code appropriée pour le volet d’exploration est présentée dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="77037-339">The relevant code section for the Explorer Bar is shown in the following code example.</span></span>


```C++
HRESULT RegisterServer()
{
    WCHAR szCLSID[MAX_PATH];
    StringFromGUID2(CLSID_DeskBandSample, szCLSID, ARRAYSIZE(szCLSID));

    WCHAR szSubkey[MAX_PATH];
    HKEY hKey;

    HRESULT hr = StringCchPrintfW(szSubkey, ARRAYSIZE(szSubkey), L"CLSID\\%s", szCLSID);
    if (SUCCEEDED(hr))
    {
        hr = E_FAIL;
        if (ERROR_SUCCESS == RegCreateKeyExW(HKEY_CLASSES_ROOT,
                                             szSubkey,
                                             0,
                                             NULL,
                                             REG_OPTION_NON_VOLATILE,
                                             KEY_WRITE,
                                             NULL,
                                             &hKey,
                                             NULL))
        {
            WCHAR const szName[] = L"DeskBand Sample";
            if (ERROR_SUCCESS == RegSetValueExW(hKey,
                                                NULL,
                                                0,
                                                REG_SZ,
                                                (LPBYTE) szName,
                                                sizeof(szName)))
            {
                hr = S_OK;
            }

            RegCloseKey(hKey);
        }
    }

    if (SUCCEEDED(hr))
    {
        hr = StringCchPrintfW(szSubkey, ARRAYSIZE(szSubkey), L"CLSID\\%s\\InprocServer32", szCLSID);
        if (SUCCEEDED(hr))
        {
            hr = HRESULT_FROM_WIN32(RegCreateKeyExW(HKEY_CLASSES_ROOT, szSubkey,
                 0, NULL, REG_OPTION_NON_VOLATILE, KEY_WRITE, NULL, &hKey, NULL));
            if (SUCCEEDED(hr))
            {
                WCHAR szModule[MAX_PATH];
                if (GetModuleFileNameW(g_hInst, szModule, ARRAYSIZE(szModule)))
                {
                    DWORD cch = lstrlen(szModule);
                    hr = HRESULT_FROM_WIN32(RegSetValueExW(hKey, NULL, 0, REG_SZ, (LPBYTE) szModule, cch * sizeof(szModule[0])));
                }

                if (SUCCEEDED(hr))
                {
                    WCHAR const szModel[] = L"Apartment";
                    hr = HRESULT_FROM_WIN32(RegSetValueExW(hKey, L"ThreadingModel", 0,  REG_SZ, (LPBYTE) szModel, sizeof(szModel)));
                }

                RegCloseKey(hKey);
            }
        }
    }

    return hr;
}
```



<span data-ttu-id="77037-340">L’inscription des objets Band dans l’exemple utilise des procédures COM normales.</span><span class="sxs-lookup"><span data-stu-id="77037-340">Registration of band objects in the sample uses normal COM procedures.</span></span>

<span data-ttu-id="77037-341">En plus du CLSID, le serveur d’objets de bande doit également être inscrit pour une ou plusieurs catégories de composants.</span><span class="sxs-lookup"><span data-stu-id="77037-341">In addition to the CLSID, the band object server must also be registered for one or more component categories.</span></span> <span data-ttu-id="77037-342">Il s’agit en fait de la principale différence d’implémentation entre les exemples de barres d’exploration verticales et horizontales.</span><span class="sxs-lookup"><span data-stu-id="77037-342">This is actually the main difference in implementation between the vertical and horizontal Explorer Bar samples.</span></span> <span data-ttu-id="77037-343">Ce processus est géré en créant un objet gestionnaire de catégories de composants (CLSID \_ StdComponentCategoriesMgr) et en utilisant la méthode [**ICatRegister :: RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories) pour inscrire le serveur d’objets de bande.</span><span class="sxs-lookup"><span data-stu-id="77037-343">This process is handled by creating a component categories manager object (CLSID\_StdComponentCategoriesMgr) and using the [**ICatRegister::RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories) method to register the band object server.</span></span> <span data-ttu-id="77037-344">Dans cet exemple, l’inscription de catégorie de composant est gérée en passant le CLSID de l’exemple de volet d’exploration et le CATID à une fonction privée (**RegisterComCat**), comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="77037-344">In this example, component category registration is handled by passing the Explorer Bar sample's CLSID and CATID to a private function—**RegisterComCat**—as shown in the following code example.</span></span>


```C++
HRESULT RegisterComCat()
{
    ICatRegister *pcr;
    HRESULT hr = CoCreateInstance(CLSID_StdComponentCategoriesMgr, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pcr));
    if (SUCCEEDED(hr))
    {
        CATID catid = CATID_DeskBand;
        hr = pcr->RegisterClassImplCategories(CLSID_DeskBandSample, 1, &catid);
        pcr->Release();
    }
    return hr;
}
```



### <a name="the-window-procedure"></a><span data-ttu-id="77037-345">La procédure de fenêtre</span><span class="sxs-lookup"><span data-stu-id="77037-345">The Window Procedure</span></span>

<span data-ttu-id="77037-346">Comme un objet de bande utilise une fenêtre enfant pour son affichage, il doit implémenter une procédure de fenêtre pour gérer Windows Messaging.</span><span class="sxs-lookup"><span data-stu-id="77037-346">Because a band object uses a child window for its display, it must implement a window procedure to handle Windows messaging.</span></span> <span data-ttu-id="77037-347">L’exemple de bande a des fonctionnalités minimales, donc la procédure de fenêtre gère uniquement cinq messages :</span><span class="sxs-lookup"><span data-stu-id="77037-347">The band sample has minimal functionality, so its window procedure only handles five messages:</span></span>

-   [<span data-ttu-id="77037-348">**\_NCCREATE WM**</span><span class="sxs-lookup"><span data-stu-id="77037-348">**WM\_NCCREATE**</span></span>](../winmsg/wm-nccreate.md)
-   [<span data-ttu-id="77037-349">**\_peinture WM**</span><span class="sxs-lookup"><span data-stu-id="77037-349">**WM\_PAINT**</span></span>](../gdi/wm-paint.md)
-   [<span data-ttu-id="77037-350">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="77037-350">**WM\_COMMAND**</span></span>](../menurc/wm-command.md)
-   [<span data-ttu-id="77037-351">**WM \_ SetFocus**</span><span class="sxs-lookup"><span data-stu-id="77037-351">**WM\_SETFOCUS**</span></span>](../inputdev/wm-setfocus.md)
-   [<span data-ttu-id="77037-352">**\_KILLFOCUS WM**</span><span class="sxs-lookup"><span data-stu-id="77037-352">**WM\_KILLFOCUS**</span></span>](../inputdev/wm-killfocus.md)

<span data-ttu-id="77037-353">La procédure peut facilement être développée pour accueillir des messages supplémentaires afin de prendre en charge davantage de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="77037-353">The procedure can easily be expanded to accommodate additional messages to support more features.</span></span>


```C++
LRESULT CALLBACK CDeskBand::WndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    LRESULT lResult = 0;

    CDeskBand *pDeskBand = reinterpret_cast<CDeskBand *>(GetWindowLongPtr(hwnd, GWLP_USERDATA));

    switch (uMsg)
    {
    case WM_CREATE:
        pDeskBand = reinterpret_cast<CDeskBand *>(reinterpret_cast<CREATESTRUCT *>(lParam)->lpCreateParams);
        pDeskBand->m_hwnd = hwnd;
        SetWindowLongPtr(hwnd, GWLP_USERDATA, reinterpret_cast<LONG_PTR>(pDeskBand));
        break;

    case WM_SETFOCUS:
        pDeskBand->OnFocus(TRUE);
        break;

    case WM_KILLFOCUS:
        pDeskBand->OnFocus(FALSE);
        break;

    case WM_PAINT:
        pDeskBand->OnPaint(NULL);
        break;

    case WM_PRINTCLIENT:
        pDeskBand->OnPaint(reinterpret_cast<HDC>(wParam));
        break;

    case WM_ERASEBKGND:
        if (pDeskBand->m_fCompositionEnabled)
        {
            lResult = 1;
        }
        break;
    }

    if (uMsg != WM_ERASEBKGND)
    {
        lResult = DefWindowProc(hwnd, uMsg, wParam, lParam);
    }

    return lResult;
}
```



<span data-ttu-id="77037-354">Le \_ Gestionnaire de commandes WM retourne simplement zéro.</span><span class="sxs-lookup"><span data-stu-id="77037-354">The WM\_COMMAND handler simply returns zero.</span></span> <span data-ttu-id="77037-355">Le \_ Gestionnaire de peinture WM crée l’affichage de texte simple présenté dans l’exemple du volet d’exploration de l’introduction.</span><span class="sxs-lookup"><span data-stu-id="77037-355">The WM\_PAINT handler creates the simple text display shown in the Explorer Bar example in the introduction.</span></span>


```C++
void CDeskBand::OnPaint(const HDC hdcIn)
{
    HDC hdc = hdcIn;
    PAINTSTRUCT ps;
    static WCHAR szContent[] = L"DeskBand Sample";
    static WCHAR szContentGlass[] = L"DeskBand Sample (Glass)";

    if (!hdc)
    {
        hdc = BeginPaint(m_hwnd, &ps);
    }

    if (hdc)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        SIZE size;

        if (m_fCompositionEnabled)
        {
            HTHEME hTheme = OpenThemeData(NULL, L"BUTTON");
            if (hTheme)
            {
                HDC hdcPaint = NULL;
                HPAINTBUFFER hBufferedPaint = BeginBufferedPaint(hdc, &rc, BPBF_TOPDOWNDIB, NULL, &hdcPaint);

                DrawThemeParentBackground(m_hwnd, hdcPaint, &rc);

                GetTextExtentPointW(hdc, szContentGlass, ARRAYSIZE(szContentGlass), &size);
                RECT rcText;
                rcText.left   = (RECTWIDTH(rc) - size.cx) / 2;
                rcText.top    = (RECTHEIGHT(rc) - size.cy) / 2;
                rcText.right  = rcText.left + size.cx;
                rcText.bottom = rcText.top + size.cy;

                DTTOPTS dttOpts = {sizeof(dttOpts)};
                dttOpts.dwFlags = DTT_COMPOSITED | DTT_TEXTCOLOR | DTT_GLOWSIZE;
                dttOpts.crText = RGB(255, 255, 0);
                dttOpts.iGlowSize = 10;
                DrawThemeTextEx(hTheme, hdcPaint, 0, 0, szContentGlass, -1, 0, &rcText, &dttOpts);

                EndBufferedPaint(hBufferedPaint, TRUE);

                CloseThemeData(hTheme);
            }
        }
        else
        {
            SetBkColor(hdc, RGB(255, 255, 0));
            GetTextExtentPointW(hdc, szContent, ARRAYSIZE(szContent), &size);
            TextOutW(hdc,
                     (RECTWIDTH(rc) - size.cx) / 2,
                     (RECTHEIGHT(rc) - size.cy) / 2,
                     szContent,
                     ARRAYSIZE(szContent));
        }
    }

    if (!hdcIn)
    {
        EndPaint(m_hwnd, &ps);
    }
}
```



<span data-ttu-id="77037-356">Les \_ gestionnaires WM SetFocus et WM \_ KILLFOCUS informent le site d’une modification de focus en appelant la méthode [**IInputObjectSite :: OnFocusChangeIS**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinputobjectsite-onfocuschangeis) du site.</span><span class="sxs-lookup"><span data-stu-id="77037-356">The WM\_SETFOCUS and WM\_KILLFOCUS handlers inform the site of a focus change by calling the site's [**IInputObjectSite::OnFocusChangeIS**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinputobjectsite-onfocuschangeis) method.</span></span>


```C++
void CDeskBand::OnFocus(const BOOL fFocus)
{
    m_fHasFocus = fFocus;

    if (m_pSite)
    {
        m_pSite->OnFocusChangeIS(static_cast<IOleWindow*>(this), m_fHasFocus);
    }
}
```



<span data-ttu-id="77037-357">Les objets Band offrent un moyen flexible et puissant d’étendre les fonctionnalités d’Internet Explorer en créant des barres d’exploration personnalisées.</span><span class="sxs-lookup"><span data-stu-id="77037-357">Band objects provide a flexible and powerful way to extend the capabilities of Internet Explorer by creating custom Explorer Bars.</span></span> <span data-ttu-id="77037-358">L’implémentation d’une bande de bureau vous permet d’étendre les fonctionnalités des fenêtres normales.</span><span class="sxs-lookup"><span data-stu-id="77037-358">Implementing a desk band enables you to extend the capabilities of normal windows.</span></span> <span data-ttu-id="77037-359">Bien que certaines programmations COM soient nécessaires, elle sert en fin de vue de fournir une fenêtre enfant pour votre interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="77037-359">Although some COM programming is required, it ultimately serves to provide a child window for your user interface.</span></span> <span data-ttu-id="77037-360">À partir de là, la majeure partie de l’implémentation peut utiliser des techniques de programmation Windows familières.</span><span class="sxs-lookup"><span data-stu-id="77037-360">From there, the bulk of the implementation can use familiar Windows programming techniques.</span></span> <span data-ttu-id="77037-361">Bien que l’exemple présenté ici ait uniquement des fonctionnalités limitées, il illustre toutes les fonctionnalités nécessaires d’un objet Band et peut être facilement étendu pour créer une interface utilisateur unique et puissante.</span><span class="sxs-lookup"><span data-stu-id="77037-361">While the example discussed here has only limited functionality, it illustrates all the necessary features of a band object and it can be readily extended to create a unique and powerful user interface.</span></span>

 

 

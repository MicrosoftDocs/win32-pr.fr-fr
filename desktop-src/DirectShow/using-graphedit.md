---
description: Utilisation de GraphEdit
ms.assetid: 91a8f111-fce4-4284-afa2-e3ea0ec35bff
title: Utilisation de GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e78118253d86a88231456b72dc8c42ed2a674f5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529523"
---
# <a name="using-graphedit"></a><span data-ttu-id="63224-103">Utilisation de GraphEdit</span><span class="sxs-lookup"><span data-stu-id="63224-103">Using GraphEdit</span></span>

<span data-ttu-id="63224-104">GraphEdit est disponible dans le kit de développement logiciel (SDK) Microsoft Windows ( <https://go.microsoft.com/fwlink/p/?linkid=62332> ).</span><span class="sxs-lookup"><span data-stu-id="63224-104">GraphEdit is available in the Microsoft Windows Software Development Kit (SDK) (<https://go.microsoft.com/fwlink/p/?linkid=62332>).</span></span>

<span data-ttu-id="63224-105">Le nom de l’application GraphEdit est « graphedt.exe ».</span><span class="sxs-lookup"><span data-stu-id="63224-105">The name of the GraphEdit application is "graphedt.exe".</span></span> <span data-ttu-id="63224-106">Une fois que vous avez installé le kit de développement logiciel (SDK), « graphedt.exe » se trouve dans le répertoire suivant : \[ Program Files \] \\ Microsoft SDK \\ Windows \\ \[ version \] \\ bin \\ .</span><span class="sxs-lookup"><span data-stu-id="63224-106">After you install the SDK, "graphedt.exe" is located in the following directory: \[Program Files\]\\Microsoft SDKs\\Windows\\\[version\]\\Bin\\.</span></span>

<span data-ttu-id="63224-107">Avant d’exécuter GraphEdit, utilisez l’utilitaire regsvr32 pour inscrire les dll suivantes, qui se trouvent dans le même répertoire :</span><span class="sxs-lookup"><span data-stu-id="63224-107">Before running GraphEdit, use the regsvr32 utility to register the following DLLs, which are located in the same directory:</span></span>

-   <span data-ttu-id="63224-108">proppage.dll</span><span class="sxs-lookup"><span data-stu-id="63224-108">proppage.dll</span></span>
-   <span data-ttu-id="63224-109">evrprop.dll</span><span class="sxs-lookup"><span data-stu-id="63224-109">evrprop.dll</span></span>

<span data-ttu-id="63224-110">Ces dll permettent à GraphEdit d’afficher des pages de propriétés pour certains des filtres DirectShow intégrés.</span><span class="sxs-lookup"><span data-stu-id="63224-110">These DLLs enable GraphEdit to display property pages for some of the built-in DirectShow filters.</span></span>

## <a name="build-a-file-playback-graph"></a><span data-ttu-id="63224-111">Créer un graphique de lecture de fichier</span><span class="sxs-lookup"><span data-stu-id="63224-111">Build a File Playback Graph</span></span>

<span data-ttu-id="63224-112">GraphEdit peut générer un graphique de filtre pour la lecture de fichiers.</span><span class="sxs-lookup"><span data-stu-id="63224-112">GraphEdit can build a filter graph for file playback.</span></span> <span data-ttu-id="63224-113">Cette fonctionnalité est équivalente à l’appel de la méthode [**IGraphBuilder :: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) dans une application.</span><span class="sxs-lookup"><span data-stu-id="63224-113">This feature is equivalent to calling the [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) method in an application.</span></span> <span data-ttu-id="63224-114">Dans le menu **fichier** , cliquez sur **afficher le fichier multimédia**.</span><span class="sxs-lookup"><span data-stu-id="63224-114">From the **File** menu, click **Render Media File**.</span></span> <span data-ttu-id="63224-115">GraphEdit affiche une boîte de dialogue **ouvrir un fichier** .</span><span class="sxs-lookup"><span data-stu-id="63224-115">GraphEdit displays an **Open File** dialog box.</span></span> <span data-ttu-id="63224-116">Sélectionnez un fichier multimédia, puis cliquez sur **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="63224-116">Select a multimedia file and click **Open**.</span></span> <span data-ttu-id="63224-117">GraphEdit crée un graphique de filtre pour lire le fichier que vous avez sélectionné.</span><span class="sxs-lookup"><span data-stu-id="63224-117">GraphEdit builds a filter graph to play the file you've selected.</span></span>

<span data-ttu-id="63224-118">Vous pouvez également afficher un fichier multimédia situé dans une URL.</span><span class="sxs-lookup"><span data-stu-id="63224-118">You can also render a media file located at a URL.</span></span> <span data-ttu-id="63224-119">Dans le menu **fichier** , cliquez sur **afficher l’URL**.</span><span class="sxs-lookup"><span data-stu-id="63224-119">From the **File** menu, click **Render URL**.</span></span> <span data-ttu-id="63224-120">GraphEdit affiche une boîte de dialogue dans laquelle vous pouvez taper l’URL.</span><span class="sxs-lookup"><span data-stu-id="63224-120">GraphEdit displays a dialog box in which to type the URL.</span></span>

## <a name="build-a-filter-graph"></a><span data-ttu-id="63224-121">Créer un graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="63224-121">Build a Filter Graph</span></span>

<span data-ttu-id="63224-122">GraphEdit peut créer un graphique de filtre personnalisé à l’aide de n’importe quel filtre enregistré sur votre système.</span><span class="sxs-lookup"><span data-stu-id="63224-122">GraphEdit can build a custom filter graph, using any of the filters registered on your system.</span></span> <span data-ttu-id="63224-123">Dans le menu **graphique** , cliquez sur **Insérer des filtres**.</span><span class="sxs-lookup"><span data-stu-id="63224-123">From the **Graph** menu, click **Insert Filters**.</span></span> <span data-ttu-id="63224-124">Une boîte de dialogue s’affiche avec une liste des filtres sur votre système, organisés par catégorie de filtre.</span><span class="sxs-lookup"><span data-stu-id="63224-124">A dialog box appears with a list of the filters on your system, organized by filter category.</span></span> <span data-ttu-id="63224-125">GraphEdit génère cette liste à partir des informations du Registre.</span><span class="sxs-lookup"><span data-stu-id="63224-125">GraphEdit builds this list from information in the registry.</span></span> <span data-ttu-id="63224-126">L’illustration suivante montre la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="63224-126">The following illustration shows the dialog box.</span></span>

![Quels filtres voulez-vous insérer ?](images/gedit12.png)

<span data-ttu-id="63224-128">Pour ajouter un filtre au graphique, sélectionnez le nom du filtre, cliquez sur le bouton **Insérer des filtres** ou double-cliquez sur le nom du filtre.</span><span class="sxs-lookup"><span data-stu-id="63224-128">To add a filter to the graph, select the name of the filter and click the **Insert Filters** button, or double-click the filter name.</span></span> <span data-ttu-id="63224-129">Une fois que vous avez ajouté les filtres, vous pouvez connecter deux filtres en faisant glisser la souris de la broche de sortie d’un filtre vers la broche d’entrée d’un autre filtre.</span><span class="sxs-lookup"><span data-stu-id="63224-129">After you have added the filters, you can connect two filters by dragging the mouse from one filter's output pin to another filter's input pin.</span></span> <span data-ttu-id="63224-130">Si les codes confidentiels acceptent la connexion, GraphEdit dessine une flèche les connectant.</span><span class="sxs-lookup"><span data-stu-id="63224-130">If the pins accept the connection, GraphEdit draws an arrow connecting them.</span></span>

![connexion de deux filtres](images/gedit-connect.png)

## <a name="run-the-graph"></a><span data-ttu-id="63224-132">Exécuter le graphique</span><span class="sxs-lookup"><span data-stu-id="63224-132">Run the Graph</span></span>

<span data-ttu-id="63224-133">Une fois que vous avez créé un graphique de filtre dans la modification de graphique, vous pouvez exécuter le graphique pour voir s’il fonctionne comme prévu.</span><span class="sxs-lookup"><span data-stu-id="63224-133">Once you have built a filter graph in Graph Edit, you can run the graph to see whether it works as you expect.</span></span> <span data-ttu-id="63224-134">Le menu **graphique** contient les commandes de menu **lecture**, **Pause** et **arrêt**.</span><span class="sxs-lookup"><span data-stu-id="63224-134">The **Graph** menu contains the menu commands **Play**, **Pause**, and **Stop**.</span></span> <span data-ttu-id="63224-135">Ces commandes appellent respectivement les [](/windows/desktop/api/Control/nn-control-imediacontrol) méthodes IMediaControl [**exécuter**](/windows/desktop/api/Control/nf-control-imediacontrol-run), [**suspendre**](/windows/desktop/api/Control/nf-control-imediacontrol-pause)et [**arrêter**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).</span><span class="sxs-lookup"><span data-stu-id="63224-135">These commands invoke to the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) methods [**Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), [**Pause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause), and [**Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop), respectively.</span></span> <span data-ttu-id="63224-136">La barre d’outils GraphEdit contient également des boutons pour ces commandes :</span><span class="sxs-lookup"><span data-stu-id="63224-136">The GraphEdit toolbar has buttons for these commands, as well:</span></span>

![boutons suspendre, lire et arrêter](images/gedit-toolbar.png)

> [!Note]  
> <span data-ttu-id="63224-138">La commande GraphEdit **Stop** interrompt d’abord le graphique et cherche à l’heure zéro (en supposant que le graphique est recherché).</span><span class="sxs-lookup"><span data-stu-id="63224-138">The GraphEdit **Stop** command first pauses the graph and seeks to time zero (assuming the graph is seekable).</span></span> <span data-ttu-id="63224-139">Pour la lecture de fichier, cette action réinitialise la fenêtre vidéo sur le premier frame.</span><span class="sxs-lookup"><span data-stu-id="63224-139">For file playback, this action resets the video window to the first frame.</span></span> <span data-ttu-id="63224-140">GraphEdit appelle [**IMediaControl :: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).</span><span class="sxs-lookup"><span data-stu-id="63224-140">Then GraphEdit calls [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).</span></span>

 

<span data-ttu-id="63224-141">Si le graphique est recherché, vous pouvez le Rechercher en faisant glisser la barre de curseur qui apparaît sous la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="63224-141">If the graph is seekable, you can seek it by dragging the slider bar that appears below the toolbar.</span></span> <span data-ttu-id="63224-142">Si vous faites glisser la barre du curseur, la méthode [**IMediaSeeking :: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) est appelée.</span><span class="sxs-lookup"><span data-stu-id="63224-142">Dragging the slider bar invokes the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span>

## <a name="view-property-pages"></a><span data-ttu-id="63224-143">Afficher les pages de propriétés</span><span class="sxs-lookup"><span data-stu-id="63224-143">View Property Pages</span></span>

<span data-ttu-id="63224-144">Certains filtres prennent en charge des pages de propriétés personnalisées, qui fournissent une interface utilisateur pour définir des propriétés sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="63224-144">Some filters support custom property pages, which provide a user interface for setting properties on the filter.</span></span> <span data-ttu-id="63224-145">Pour afficher la page de propriétés d’un filtre dans GraphEdit, cliquez avec le bouton droit sur le filtre et sélectionnez **Propriétés** dans la fenêtre contextuelle.</span><span class="sxs-lookup"><span data-stu-id="63224-145">To view a filter's property page in GraphEdit, right-click the filter and select **Properties** from the pop-up window.</span></span> <span data-ttu-id="63224-146">GraphEdit affiche une page de propriétés qui contient les feuilles de propriétés définies par le filtre (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="63224-146">GraphEdit displays a property page that contains the property sheets defined by the filter (if any).</span></span> <span data-ttu-id="63224-147">En outre, GraphEdit comprend une feuille de propriétés pour chaque code confidentiel sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="63224-147">In addition, GraphEdit includes a property sheet for each pin on the filter.</span></span> <span data-ttu-id="63224-148">Les feuilles de propriétés de code confidentiel sont définies par GraphEdit, et non par le filtre.</span><span class="sxs-lookup"><span data-stu-id="63224-148">The pin property sheets are defined by GraphEdit, not by the filter.</span></span> <span data-ttu-id="63224-149">Si le code PIN est connecté, la feuille de propriétés du code confidentiel affiche le type de média pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="63224-149">If the pin is connected, the pin property sheet displays the media type for the connection.</span></span> <span data-ttu-id="63224-150">Dans le cas contraire, elle répertorie les types de média préférés du pin.</span><span class="sxs-lookup"><span data-stu-id="63224-150">Otherwise, it lists the pin's preferred media types.</span></span>

> [!Note]  
> <span data-ttu-id="63224-151">Pour utiliser les pages de propriétés intégrées de GraphEdit, vous devez inscrire proppage.dll.</span><span class="sxs-lookup"><span data-stu-id="63224-151">To use GraphEdit's built-in property pages, you must register proppage.dll.</span></span> <span data-ttu-id="63224-152">Cette DLL est disponible dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="63224-152">This DLL is available in the Windows SDK.</span></span> <span data-ttu-id="63224-153">La DLL contient également des pages de propriétés supplémentaires pour certains filtres DirectShow.</span><span class="sxs-lookup"><span data-stu-id="63224-153">The DLL also contains additional property pages for some DirectShow filters.</span></span> <span data-ttu-id="63224-154">Ces pages de propriétés sont fournies à des fins de débogage uniquement.</span><span class="sxs-lookup"><span data-stu-id="63224-154">These property pages are provided for debugging purposes only.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="63224-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="63224-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63224-156">Simulation de la génération de graphiques avec GraphEdit</span><span class="sxs-lookup"><span data-stu-id="63224-156">Simulating Graph Building with GraphEdit</span></span>](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 




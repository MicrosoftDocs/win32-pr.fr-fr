---
description: Illustre une barre d’outils miniatures, un contrôle de barre d’outils actif incorporé dans la miniature d’une fenêtre, utilisé pour fournir l’accès aux commandes clés d’une fenêtre sans effectuer la restauration de l’utilisateur ou activer la fenêtre de l’application.
title: Barre d’outils de miniatures de barre des tâches, exemple
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4936FF67-19EE-4963-BE4C-3D40350C64A9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e61208f15772a43138e6cd7a38fd6327445bdfa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973534"
---
# <a name="taskbar-thumbnail-toolbar-sample"></a><span data-ttu-id="1f0fd-103">Barre d’outils de miniatures de barre des tâches, exemple</span><span class="sxs-lookup"><span data-stu-id="1f0fd-103">Taskbar Thumbnail Toolbar Sample</span></span>

<span data-ttu-id="1f0fd-104">Illustre une barre d’outils miniatures, un contrôle de barre d’outils actif incorporé dans la miniature d’une fenêtre, utilisé pour fournir l’accès aux commandes clés d’une fenêtre sans effectuer la restauration de l’utilisateur ou activer la fenêtre de l’application.</span><span class="sxs-lookup"><span data-stu-id="1f0fd-104">Demonstrates a thumbnail toolbar, an active toolbar control embedded in a window's thumbnail preview, used to provide access to a window's key commands without making the user restore or activate the application's window.</span></span>

<span data-ttu-id="1f0fd-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="1f0fd-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="1f0fd-106">Description</span><span class="sxs-lookup"><span data-stu-id="1f0fd-106">Description</span></span>](#description)
-   [<span data-ttu-id="1f0fd-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f0fd-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="1f0fd-108">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="1f0fd-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="1f0fd-109">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="1f0fd-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="1f0fd-110">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="1f0fd-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="1f0fd-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1f0fd-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="1f0fd-112">Description</span><span class="sxs-lookup"><span data-stu-id="1f0fd-112">Description</span></span>

<span data-ttu-id="1f0fd-113">Cet exemple montre comment fournir une barre d’outils simple à un aperçu miniature de la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="1f0fd-113">This sample shows how to provide a simple toolbar to a taskbar thumbnail preview.</span></span> <span data-ttu-id="1f0fd-114">La barre d’outils se compose de trois boutons.</span><span class="sxs-lookup"><span data-stu-id="1f0fd-114">The toolbar consists of three buttons.</span></span> <span data-ttu-id="1f0fd-115">En cliquant sur un bouton, une fenêtre s’affiche pour confirmer que le bouton a été activé.</span><span class="sxs-lookup"><span data-stu-id="1f0fd-115">Clicking a button displays a window to confirm that the button was activated.</span></span> <span data-ttu-id="1f0fd-116">Les API suivantes sont illustrées :</span><span class="sxs-lookup"><span data-stu-id="1f0fd-116">The following APIs are demonstrated:</span></span>

-   [<span data-ttu-id="1f0fd-117">**ITaskbarList3 :: ThumbBarAddButtons**</span><span class="sxs-lookup"><span data-stu-id="1f0fd-117">**ITaskbarList3::ThumbBarAddButtons**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbaraddbuttons)
-   [<span data-ttu-id="1f0fd-118">**ITaskbarList3 :: ThumbBarSetImageList**</span><span class="sxs-lookup"><span data-stu-id="1f0fd-118">**ITaskbarList3::ThumbBarSetImageList**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarsetimagelist)
-   <span data-ttu-id="1f0fd-119">[**ThumbButton**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton) , structure</span><span class="sxs-lookup"><span data-stu-id="1f0fd-119">[**THUMBBUTTON**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton) structure</span></span>

## <a name="requirements"></a><span data-ttu-id="1f0fd-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1f0fd-120">Requirements</span></span>



| <span data-ttu-id="1f0fd-121">Produit</span><span class="sxs-lookup"><span data-stu-id="1f0fd-121">Product</span></span>                                | <span data-ttu-id="1f0fd-122">Version minimale du produit</span><span class="sxs-lookup"><span data-stu-id="1f0fd-122">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="1f0fd-123">Windows</span><span class="sxs-lookup"><span data-stu-id="1f0fd-123">Windows</span></span>                                | <span data-ttu-id="1f0fd-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1f0fd-124">Windows 7</span></span>               |
| <span data-ttu-id="1f0fd-125">Kit de développement logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="1f0fd-125">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="1f0fd-126">7.0</span><span class="sxs-lookup"><span data-stu-id="1f0fd-126">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="1f0fd-127">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="1f0fd-127">Downloading the Sample</span></span>

| <span data-ttu-id="1f0fd-128">Emplacement</span><span class="sxs-lookup"><span data-stu-id="1f0fd-128">Location</span></span>      | <span data-ttu-id="1f0fd-129">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="1f0fd-129">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f0fd-130">GitHub</span><span class="sxs-lookup"><span data-stu-id="1f0fd-130">GitHub</span></span>  | [<span data-ttu-id="1f0fd-131">Exemple TaskbarThumbnailToolbar</span><span class="sxs-lookup"><span data-stu-id="1f0fd-131">TaskbarThumbnailToolbar sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TaskbarThumbnailToolbar) |

## <a name="building-the-sample"></a><span data-ttu-id="1f0fd-132">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="1f0fd-132">Building the Sample</span></span>

<span data-ttu-id="1f0fd-133">Pour générer l’exemple à partir de l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="1f0fd-133">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="1f0fd-134">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **TaskbarThumbnailToolbar** .</span><span class="sxs-lookup"><span data-stu-id="1f0fd-134">Open the command prompt window and navigate to the **TaskbarThumbnailToolbar** project directory.</span></span>
2.  <span data-ttu-id="1f0fd-135">Entrez `msbuild ThumbnailToolbar.sln`.</span><span class="sxs-lookup"><span data-stu-id="1f0fd-135">Enter `msbuild ThumbnailToolbar.sln`.</span></span>

<span data-ttu-id="1f0fd-136">Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :</span><span class="sxs-lookup"><span data-stu-id="1f0fd-136">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="1f0fd-137">Ouvrez l’Explorateur Windows et accédez au répertoire du projet **TaskbarThumbnailToolbar** .</span><span class="sxs-lookup"><span data-stu-id="1f0fd-137">Open Windows Explorer and navigate to the **TaskbarThumbnailToolbar** project directory.</span></span>
2.  <span data-ttu-id="1f0fd-138">Double-cliquez sur l’icône du fichier ThumbnailToolbar. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="1f0fd-138">Double-click the icon for the ThumbnailToolbar.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="1f0fd-139">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="1f0fd-139">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="1f0fd-140">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="1f0fd-140">Running the Sample</span></span>

1.  <span data-ttu-id="1f0fd-141">Accédez au répertoire qui contient le nouveau fichier exécutable (par exemple,) à l' `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarThumbnailToolbar\Debug` aide de l’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="1f0fd-141">Navigate to the directory that contains the new executable file (for instance, `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarThumbnailToolbar\Debug`), using the command prompt or Windows Explorer.</span></span>

    -   <span data-ttu-id="1f0fd-142">Si vous utilisez la ligne de commande, entrez `ThumbnailToolbar.exe` .</span><span class="sxs-lookup"><span data-stu-id="1f0fd-142">If using the command line, enter `ThumbnailToolbar.exe`.</span></span>
    -   <span data-ttu-id="1f0fd-143">Si vous utilisez l’Explorateur Windows, double-cliquez sur l’icône de ThumbnailToolbar.exe.</span><span class="sxs-lookup"><span data-stu-id="1f0fd-143">If using Windows Explorer, double-click the icon for ThumbnailToolbar.exe.</span></span>

    <span data-ttu-id="1f0fd-144">Une nouvelle fenêtre s’ouvre, avec un bouton de barre des tâches associé.</span><span class="sxs-lookup"><span data-stu-id="1f0fd-144">A new window will open, with an associated taskbar button.</span></span>

2.  <span data-ttu-id="1f0fd-145">Placez le curseur sur le bouton **ThumbnailToolbar** de la barre des tâches pour afficher l’aperçu.</span><span class="sxs-lookup"><span data-stu-id="1f0fd-145">Hover the cursor over the **ThumbnailToolbar** taskbar button so that the preview displays.</span></span> <span data-ttu-id="1f0fd-146">Cliquez sur l’un des trois boutons (vert, jaune, rouge) affichés dans la barre d’outils de l’aperçu.</span><span class="sxs-lookup"><span data-stu-id="1f0fd-146">Click one of the three buttons (green, yellow, red) shown in the preview's toolbar.</span></span>
3.  <span data-ttu-id="1f0fd-147">Choisissez **quitter** dans le menu **fichier** de la fenêtre pour mettre fin au programme.</span><span class="sxs-lookup"><span data-stu-id="1f0fd-147">Choose **Exit** from the window's **File** menu to end the program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f0fd-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1f0fd-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f0fd-149">Extensions de la barre des tâches</span><span class="sxs-lookup"><span data-stu-id="1f0fd-149">Taskbar Extensions</span></span>](taskbar-extensions.md)
</dt> </dl>

 

 




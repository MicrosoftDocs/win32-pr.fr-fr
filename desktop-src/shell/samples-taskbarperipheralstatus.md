---
description: Présente les superpositions d’icône de barre des tâches et les barres de progression.
title: État du périphérique de barre des tâches, exemple
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E4B693FB-EE7D-47d0-A5D8-91205AD4A3DC
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 793c09853e3174f426b7b41685f2593daaae9b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991745"
---
# <a name="taskbar-peripheral-status-sample"></a><span data-ttu-id="25e17-103">État du périphérique de barre des tâches, exemple</span><span class="sxs-lookup"><span data-stu-id="25e17-103">Taskbar Peripheral Status Sample</span></span>

<span data-ttu-id="25e17-104">Présente les superpositions d’icône de barre des tâches et les barres de progression.</span><span class="sxs-lookup"><span data-stu-id="25e17-104">Demonstrates taskbar icon overlays and progress bars.</span></span>

<span data-ttu-id="25e17-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="25e17-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="25e17-106">Description</span><span class="sxs-lookup"><span data-stu-id="25e17-106">Description</span></span>](#description)
-   [<span data-ttu-id="25e17-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25e17-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="25e17-108">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="25e17-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="25e17-109">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="25e17-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="25e17-110">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="25e17-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="25e17-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="25e17-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="25e17-112">Description</span><span class="sxs-lookup"><span data-stu-id="25e17-112">Description</span></span>

<span data-ttu-id="25e17-113">Cet exemple crée un exemple de bouton de la barre des tâches sur lequel il illustre l’utilisation de [**ITaskbarList3 :: SetOverlayIcon**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setoverlayicon) en vous permettant d’appliquer plusieurs superpositions choisies à partir d’un menu.</span><span class="sxs-lookup"><span data-stu-id="25e17-113">This sample creates an example taskbar button on which it demonstrates the use of [**ITaskbarList3::SetOverlayIcon**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setoverlayicon) by allowing you to apply various overlays chosen from a menu.</span></span>

<span data-ttu-id="25e17-114">L’exemple offre également la possibilité de simuler un indicateur de progression sur le bouton, en illustrant l’utilisation de [**ITaskbarList3 :: SetProgressState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressstate) et [**ITaskbarList3 :: SetProgressValue**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue) en affichant au début un indicateur de progression indéterminé (TBPF \_ indéterminé), puis un indicateur proportionnel normal (TBPF \_ normal).</span><span class="sxs-lookup"><span data-stu-id="25e17-114">The sample also provides the option of simulating a progress indicator on the button, demonstrating the use of [**ITaskbarList3::SetProgressState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressstate) and [**ITaskbarList3::SetProgressValue**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue) by showing at first an indeterminate progress indicator (TBPF\_INDETERMINATE), and then a normal proportional indicator (TBPF\_NORMAL).</span></span>

## <a name="requirements"></a><span data-ttu-id="25e17-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="25e17-115">Requirements</span></span>



| <span data-ttu-id="25e17-116">Produit</span><span class="sxs-lookup"><span data-stu-id="25e17-116">Product</span></span>                                | <span data-ttu-id="25e17-117">Version minimale du produit</span><span class="sxs-lookup"><span data-stu-id="25e17-117">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="25e17-118">Windows</span><span class="sxs-lookup"><span data-stu-id="25e17-118">Windows</span></span>                                | <span data-ttu-id="25e17-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="25e17-119">Windows 7</span></span>               |
| <span data-ttu-id="25e17-120">Kit de développement logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="25e17-120">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="25e17-121">7.0</span><span class="sxs-lookup"><span data-stu-id="25e17-121">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="25e17-122">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="25e17-122">Downloading the Sample</span></span>

| <span data-ttu-id="25e17-123">Emplacement</span><span class="sxs-lookup"><span data-stu-id="25e17-123">Location</span></span>      | <span data-ttu-id="25e17-124">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="25e17-124">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25e17-125">GitHub</span><span class="sxs-lookup"><span data-stu-id="25e17-125">GitHub</span></span>  | [<span data-ttu-id="25e17-126">Exemple TaskBarPeripheralStatus</span><span class="sxs-lookup"><span data-stu-id="25e17-126">TaskBarPeripheralStatus sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TaskbarPeripheralStatus) |

## <a name="building-the-sample"></a><span data-ttu-id="25e17-127">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="25e17-127">Building the Sample</span></span>

<span data-ttu-id="25e17-128">Pour générer l’exemple à partir de l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="25e17-128">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="25e17-129">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **TaskbarPeripheralStatus** .</span><span class="sxs-lookup"><span data-stu-id="25e17-129">Open the command prompt window and navigate to the **TaskbarPeripheralStatus** project directory.</span></span>
2.  <span data-ttu-id="25e17-130">Entrez `msbuild PeripheralStatus.sln`.</span><span class="sxs-lookup"><span data-stu-id="25e17-130">Enter `msbuild PeripheralStatus.sln`.</span></span>

<span data-ttu-id="25e17-131">Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :</span><span class="sxs-lookup"><span data-stu-id="25e17-131">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="25e17-132">Ouvrez l’Explorateur Windows et accédez au répertoire du projet **TaskbarPeripheralStatus** .</span><span class="sxs-lookup"><span data-stu-id="25e17-132">Open Windows Explorer and navigate to the **TaskbarPeripheralStatus** project directory.</span></span>
2.  <span data-ttu-id="25e17-133">Double-cliquez sur l’icône du fichier PeripheralStatus. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="25e17-133">Double-click the icon for the PeripheralStatus.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="25e17-134">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="25e17-134">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="25e17-135">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="25e17-135">Running the Sample</span></span>

1.  <span data-ttu-id="25e17-136">Accédez au répertoire qui contient le nouveau fichier exécutable (par exemple,) à l' `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarPeripheralStatus\Win32\Debug` aide de l’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="25e17-136">Navigate to the directory that contains the new executable file (for instance, `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarPeripheralStatus\Win32\Debug`), using the command prompt or Windows Explorer.</span></span>

    -   <span data-ttu-id="25e17-137">Si vous utilisez la ligne de commande, entrez `PeripheralStatus.exe` .</span><span class="sxs-lookup"><span data-stu-id="25e17-137">If using the command line, enter `PeripheralStatus.exe`.</span></span>
    -   <span data-ttu-id="25e17-138">Si vous utilisez l’Explorateur Windows, double-cliquez sur l’icône de PeripheralStatus.exe.</span><span class="sxs-lookup"><span data-stu-id="25e17-138">If using Windows Explorer, double-click the icon for PeripheralStatus.exe.</span></span>

    <span data-ttu-id="25e17-139">Une nouvelle fenêtre s’ouvre, avec un bouton de barre des tâches associé.</span><span class="sxs-lookup"><span data-stu-id="25e17-139">A new window will open, with an associated taskbar button.</span></span>

2.  <span data-ttu-id="25e17-140">Pour illustrer les superpositions, choisissez superposition **1** ou **superposition 2** dans le menu **État du périphérique** de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="25e17-140">To demonstrate overlays, choose **Overlay 1** or **Overlay 2** from the window's **Peripheral Status** menu.</span></span> <span data-ttu-id="25e17-141">La superposition choisie s’affiche sur le bouton de la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="25e17-141">The chosen overlay appears on the taskbar button.</span></span> <span data-ttu-id="25e17-142">Pour supprimer la superposition, choisissez **effacer la superposition**.</span><span class="sxs-lookup"><span data-stu-id="25e17-142">To remove the overlay, choose **Clear Overlay**.</span></span>
3.  <span data-ttu-id="25e17-143">Pour illustrer la barre de progression, choisissez **simuler la progression** dans le menu **État du périphérique** de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="25e17-143">To demonstrate the progress bar, choose **Simulate Progress** from the window's **Peripheral Status** menu.</span></span> <span data-ttu-id="25e17-144">Le bouton de la barre des tâches affiche un indicateur de progression indéterminé, puis passe à un indicateur normal.</span><span class="sxs-lookup"><span data-stu-id="25e17-144">The taskbar button will show an indeterminate progress indicator then switch to a normal indicator.</span></span>
4.  <span data-ttu-id="25e17-145">Choisissez **quitter** dans le menu **fichier** de la fenêtre pour mettre fin au programme.</span><span class="sxs-lookup"><span data-stu-id="25e17-145">Choose **Exit** from the window's **File** menu to end the program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="25e17-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="25e17-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25e17-147">Extensions de la barre des tâches</span><span class="sxs-lookup"><span data-stu-id="25e17-147">Taskbar Extensions</span></span>](taskbar-extensions.md)
</dt> </dl>

 

 




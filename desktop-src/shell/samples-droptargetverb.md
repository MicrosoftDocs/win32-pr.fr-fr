---
description: Montre comment implémenter un verbe de Shell à l’aide de la méthode DropTarget.
title: DropTarget, exemple de verbe
ms.topic: article
ms.date: 05/31/2018
ms.assetid: BEAD20C9-B01A-48aa-A85A-B7171383FBDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1f737c951c5bd588760dbb716859c04c0dc062fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973339"
---
# <a name="droptarget-verb-sample"></a><span data-ttu-id="eac71-103">DropTarget, exemple de verbe</span><span class="sxs-lookup"><span data-stu-id="eac71-103">DropTarget Verb Sample</span></span>

<span data-ttu-id="eac71-104">Montre comment implémenter un verbe de Shell à l’aide de la méthode DropTarget.</span><span class="sxs-lookup"><span data-stu-id="eac71-104">Demonstrates how to implement a Shell verb using the DropTarget method.</span></span>

<span data-ttu-id="eac71-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="eac71-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="eac71-106">Description</span><span class="sxs-lookup"><span data-stu-id="eac71-106">Description</span></span>](#description)
-   [<span data-ttu-id="eac71-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eac71-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="eac71-108">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="eac71-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="eac71-109">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="eac71-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="eac71-110">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="eac71-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="eac71-111">Description</span><span class="sxs-lookup"><span data-stu-id="eac71-111">Description</span></span>

<span data-ttu-id="eac71-112">Cet exemple montre comment implémenter un verbe de Shell à l’aide de la méthode DropTarget.</span><span class="sxs-lookup"><span data-stu-id="eac71-112">This sample shows how to implement a Shell verb using the DropTarget method.</span></span> <span data-ttu-id="eac71-113">Cette méthode est recommandée pour les implémentations de verbe qui doivent fonctionner sur Windows XP.</span><span class="sxs-lookup"><span data-stu-id="eac71-113">This method is preferred for verb implementations that must work on Windows XP.</span></span> <span data-ttu-id="eac71-114">Cet exemple implémente un objet COM (Component Object Model) du serveur local autonome, mais il est supposé que l’implémentation du verbe sera intégrée aux applications existantes.</span><span class="sxs-lookup"><span data-stu-id="eac71-114">This sample implements a standalone local server Component Object Model (COM) object but it is expected that the verb implementation will be integrated into existing applications.</span></span> <span data-ttu-id="eac71-115">Pour ce faire, votre objet d’application principal inscrit une fabrique de classe pour elle-même.</span><span class="sxs-lookup"><span data-stu-id="eac71-115">To do so, your main application object registers a class factory for itself.</span></span> <span data-ttu-id="eac71-116">Cet objet implémente [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) pour les verbes de votre application.</span><span class="sxs-lookup"><span data-stu-id="eac71-116">That object implements [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) for your application's verbs.</span></span> <span data-ttu-id="eac71-117">Notez que COM lance votre application si elle n’est pas déjà en cours d’exécution, mais se connecte à une instance en cours d’exécution de votre application, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="eac71-117">Note that COM launches your application if it is not already running but connects to a running instance of your application if one is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="eac71-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="eac71-118">Requirements</span></span>



| <span data-ttu-id="eac71-119">Produit</span><span class="sxs-lookup"><span data-stu-id="eac71-119">Product</span></span>                                | <span data-ttu-id="eac71-120">Version minimale du produit</span><span class="sxs-lookup"><span data-stu-id="eac71-120">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="eac71-121">Windows</span><span class="sxs-lookup"><span data-stu-id="eac71-121">Windows</span></span>                                | <span data-ttu-id="eac71-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eac71-122">Windows Vista</span></span>           |
| <span data-ttu-id="eac71-123">Kit de développement logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="eac71-123">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="eac71-124">7.0</span><span class="sxs-lookup"><span data-stu-id="eac71-124">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="eac71-125">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="eac71-125">Downloading the Sample</span></span>

| <span data-ttu-id="eac71-126">Emplacement</span><span class="sxs-lookup"><span data-stu-id="eac71-126">Location</span></span>      | <span data-ttu-id="eac71-127">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="eac71-127">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eac71-128">GitHub</span><span class="sxs-lookup"><span data-stu-id="eac71-128">GitHub</span></span>  | [<span data-ttu-id="eac71-129">Exemple DropTargetVerb</span><span class="sxs-lookup"><span data-stu-id="eac71-129">DropTargetVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/DropTargetVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="eac71-130">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="eac71-130">Building the Sample</span></span>

<span data-ttu-id="eac71-131">Pour générer l’exemple à partir de l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="eac71-131">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="eac71-132">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **DropTargetVerb** .</span><span class="sxs-lookup"><span data-stu-id="eac71-132">Open the command prompt window and navigate to the **DropTargetVerb** project directory.</span></span>
2.  <span data-ttu-id="eac71-133">Entrez `msbuild DropTargetVerb.sln`.</span><span class="sxs-lookup"><span data-stu-id="eac71-133">Enter `msbuild DropTargetVerb.sln`.</span></span>

<span data-ttu-id="eac71-134">Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :</span><span class="sxs-lookup"><span data-stu-id="eac71-134">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="eac71-135">Ouvrez l’Explorateur Windows et accédez au répertoire du projet **DropTargetVerb** .</span><span class="sxs-lookup"><span data-stu-id="eac71-135">Open Windows Explorer and navigate to the **DropTargetVerb** project directory.</span></span>
2.  <span data-ttu-id="eac71-136">Double-cliquez sur l’icône du fichier DropTargetVerb. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="eac71-136">Double-click the icon for the DropTargetVerb.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="eac71-137">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="eac71-137">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="eac71-138">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="eac71-138">Running the Sample</span></span>

1.  <span data-ttu-id="eac71-139">Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="eac71-139">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="eac71-140">Sur la ligne de commande, entrez `DropTargetVerb.exe` .</span><span class="sxs-lookup"><span data-stu-id="eac71-140">At the command line, enter `DropTargetVerb.exe`.</span></span> <span data-ttu-id="eac71-141">Vous pouvez également, à partir de l’Explorateur Windows, double-cliquer sur l’icône de DropTargetVerb.exe.</span><span class="sxs-lookup"><span data-stu-id="eac71-141">Alternatively, from Windows Explorer double-click the icon for DropTargetVerb.exe.</span></span>
3.  <span data-ttu-id="eac71-142">Suivez les instructions de la boîte de dialogue qui s’affiche</span><span class="sxs-lookup"><span data-stu-id="eac71-142">Follow the instructions in the displayed dialog</span></span>

 

 

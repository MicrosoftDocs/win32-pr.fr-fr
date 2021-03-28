---
description: Montre comment implémenter un verbe de Shell à l’aide de la méthode ExecuteCommand.
title: ExecuteCommand, exemple de verbe
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0418318A-3E62-4690-AFB3-9B4A391C537E
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 2deeb63fc6648d07b3d870888d6d2eabc6fb0490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210957"
---
# <a name="execute-command-verb-sample"></a><span data-ttu-id="3cfb3-103">ExecuteCommand, exemple de verbe</span><span class="sxs-lookup"><span data-stu-id="3cfb3-103">Execute Command Verb Sample</span></span>

<span data-ttu-id="3cfb3-104">Montre comment implémenter un verbe de Shell à l’aide de la méthode ExecuteCommand.</span><span class="sxs-lookup"><span data-stu-id="3cfb3-104">Demonstrates how to implement a Shell verb using the ExecuteCommand method.</span></span>

<span data-ttu-id="3cfb3-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="3cfb3-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3cfb3-106">Description</span><span class="sxs-lookup"><span data-stu-id="3cfb3-106">Description</span></span>](#description)
-   [<span data-ttu-id="3cfb3-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3cfb3-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="3cfb3-108">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="3cfb3-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="3cfb3-109">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="3cfb3-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="3cfb3-110">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="3cfb3-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="3cfb3-111">Description</span><span class="sxs-lookup"><span data-stu-id="3cfb3-111">Description</span></span>

<span data-ttu-id="3cfb3-112">Cette méthode est préférable pour les implémentations de verbe, car elle offre la plus grande souplesse, est simple et prend en charge l’activation hors processus.</span><span class="sxs-lookup"><span data-stu-id="3cfb3-112">This method is preferred for verb implementations because it provides the most flexibility, is simple, and supports out-of-process activation.</span></span> <span data-ttu-id="3cfb3-113">Cet exemple implémente un objet COM (Component Object Model) de serveur local autonome, mais il est supposé que l’implémentation du verbe sera intégrée aux applications existantes.</span><span class="sxs-lookup"><span data-stu-id="3cfb3-113">This sample implements a standalone, local server Component Object Model (COM) object, but it is expected that the verb implementation will be integrated into existing applications.</span></span> <span data-ttu-id="3cfb3-114">Pour ce faire, votre objet d’application principal doit inscrire une fabrique de classe pour elle-même.</span><span class="sxs-lookup"><span data-stu-id="3cfb3-114">To do so, your main application object must register a class factory for itself.</span></span> <span data-ttu-id="3cfb3-115">Cet objet implémente [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) pour les verbes de votre application.</span><span class="sxs-lookup"><span data-stu-id="3cfb3-115">That object implements [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) for your application's verbs.</span></span> <span data-ttu-id="3cfb3-116">Notez que COM lance votre application si elle n’est pas déjà en cours d’exécution, mais se connecte à une instance en cours d’exécution de votre application, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="3cfb3-116">Note that COM launches your application if it is not already running but connects to a running instance of your application if one is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cfb3-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3cfb3-117">Requirements</span></span>



| <span data-ttu-id="3cfb3-118">Produit</span><span class="sxs-lookup"><span data-stu-id="3cfb3-118">Product</span></span>                                | <span data-ttu-id="3cfb3-119">Version minimale du produit</span><span class="sxs-lookup"><span data-stu-id="3cfb3-119">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="3cfb3-120">Windows</span><span class="sxs-lookup"><span data-stu-id="3cfb3-120">Windows</span></span>                                | <span data-ttu-id="3cfb3-121">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3cfb3-121">Windows 7</span></span>               |
| <span data-ttu-id="3cfb3-122">Kit de développement logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="3cfb3-122">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="3cfb3-123">7.0</span><span class="sxs-lookup"><span data-stu-id="3cfb3-123">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="3cfb3-124">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="3cfb3-124">Downloading the Sample</span></span>

| <span data-ttu-id="3cfb3-125">Emplacement</span><span class="sxs-lookup"><span data-stu-id="3cfb3-125">Location</span></span>      | <span data-ttu-id="3cfb3-126">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="3cfb3-126">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cfb3-127">GitHub</span><span class="sxs-lookup"><span data-stu-id="3cfb3-127">GitHub</span></span>  | [<span data-ttu-id="3cfb3-128">Exemple ExecuteCommandVerb</span><span class="sxs-lookup"><span data-stu-id="3cfb3-128">ExecuteCommandVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/ExecuteCommandVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="3cfb3-129">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="3cfb3-129">Building the Sample</span></span>

<span data-ttu-id="3cfb3-130">Pour générer l’exemple à partir de l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="3cfb3-130">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="3cfb3-131">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **ExecuteCommandVerb** .</span><span class="sxs-lookup"><span data-stu-id="3cfb3-131">Open the command prompt window and navigate to the **ExecuteCommandVerb** project directory.</span></span>
2.  <span data-ttu-id="3cfb3-132">Entrez `msbuild ExecuteCommand.sln`.</span><span class="sxs-lookup"><span data-stu-id="3cfb3-132">Enter `msbuild ExecuteCommand.sln`.</span></span>

<span data-ttu-id="3cfb3-133">Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :</span><span class="sxs-lookup"><span data-stu-id="3cfb3-133">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="3cfb3-134">Ouvrez l’Explorateur Windows et accédez au répertoire du projet **ExecuteCommandVerb** .</span><span class="sxs-lookup"><span data-stu-id="3cfb3-134">Open Windows Explorer and navigate to the **ExecuteCommandVerb** project directory.</span></span>
2.  <span data-ttu-id="3cfb3-135">Double-cliquez sur l’icône du fichier ExecuteCommand. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3cfb3-135">Double-click the icon for the ExecuteCommand.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="3cfb3-136">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="3cfb3-136">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="3cfb3-137">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="3cfb3-137">Running the Sample</span></span>

1.  <span data-ttu-id="3cfb3-138">Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="3cfb3-138">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="3cfb3-139">Sur la ligne de commande, entrez `ExecuteCommand.exe` .</span><span class="sxs-lookup"><span data-stu-id="3cfb3-139">At the command line, enter `ExecuteCommand.exe`.</span></span> <span data-ttu-id="3cfb3-140">Vous pouvez également, à partir de l’Explorateur Windows, double-cliquer sur l’icône de ExecuteCommand.exe.</span><span class="sxs-lookup"><span data-stu-id="3cfb3-140">Alternatively, from Windows Explorer double-click the icon for ExecuteCommand.exe.</span></span>
3.  <span data-ttu-id="3cfb3-141">Suivez les instructions de la boîte de dialogue qui s’affiche</span><span class="sxs-lookup"><span data-stu-id="3cfb3-141">Follow the instructions in the displayed dialog</span></span>

 

 

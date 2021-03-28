---
description: Montre comment écouter les notifications de modification de l’interpréteur de commandes sur un dossier ou un élément dans l’espace de noms de l’Explorateur Windows.
title: Observateur de notification de changement, exemple
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 02A7C5B4-94F2-4c35-9290-4C816E5CF63A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5d0ac6ccb2dd2328d81b77d03bffc68dfa9a70cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204046"
---
# <a name="change-notify-watcher-sample"></a><span data-ttu-id="4aad6-103">Observateur de notification de changement, exemple</span><span class="sxs-lookup"><span data-stu-id="4aad6-103">Change Notify Watcher Sample</span></span>

<span data-ttu-id="4aad6-104">Montre comment écouter les notifications de modification de l’interpréteur de commandes sur un dossier ou un élément dans l’espace de noms de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="4aad6-104">Demonstrates how to listen to Shell change notifications on a folder or item in the Windows Explorer namespace.</span></span>

<span data-ttu-id="4aad6-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="4aad6-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="4aad6-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4aad6-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="4aad6-107">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="4aad6-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="4aad6-108">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="4aad6-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="4aad6-109">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="4aad6-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="4aad6-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4aad6-110">Requirements</span></span>



| <span data-ttu-id="4aad6-111">Produit</span><span class="sxs-lookup"><span data-stu-id="4aad6-111">Product</span></span>                                | <span data-ttu-id="4aad6-112">Version minimale du produit</span><span class="sxs-lookup"><span data-stu-id="4aad6-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="4aad6-113">Windows</span><span class="sxs-lookup"><span data-stu-id="4aad6-113">Windows</span></span>                                | <span data-ttu-id="4aad6-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4aad6-114">Windows Vista</span></span>           |
| <span data-ttu-id="4aad6-115">Kit de développement logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="4aad6-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="4aad6-116">7.0</span><span class="sxs-lookup"><span data-stu-id="4aad6-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="4aad6-117">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="4aad6-117">Downloading the Sample</span></span>

| <span data-ttu-id="4aad6-118">Emplacement</span><span class="sxs-lookup"><span data-stu-id="4aad6-118">Location</span></span>      | <span data-ttu-id="4aad6-119">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="4aad6-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4aad6-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="4aad6-120">GitHub</span></span>  | [<span data-ttu-id="4aad6-121">Exemple ChangeNotifyWatcher</span><span class="sxs-lookup"><span data-stu-id="4aad6-121">ChangeNotifyWatcher sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/ChangeNotifyWatcher) |

## <a name="building-the-sample"></a><span data-ttu-id="4aad6-122">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="4aad6-122">Building the Sample</span></span>

<span data-ttu-id="4aad6-123">Pour générer l’exemple à partir de l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="4aad6-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="4aad6-124">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **ChangeNotifyWatcher** .</span><span class="sxs-lookup"><span data-stu-id="4aad6-124">Open the command prompt window and navigate to the **ChangeNotifyWatcher** project directory.</span></span>
2.  <span data-ttu-id="4aad6-125">Entrez `msbuild ChangeNotifyWatcher.sln`.</span><span class="sxs-lookup"><span data-stu-id="4aad6-125">Enter `msbuild ChangeNotifyWatcher.sln`.</span></span>

<span data-ttu-id="4aad6-126">Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :</span><span class="sxs-lookup"><span data-stu-id="4aad6-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="4aad6-127">Ouvrez l’Explorateur Windows et accédez au répertoire du projet **ChangeNotifyWatcher** .</span><span class="sxs-lookup"><span data-stu-id="4aad6-127">Open Windows Explorer and navigate to the **ChangeNotifyWatcher** project directory.</span></span>
2.  <span data-ttu-id="4aad6-128">Double-cliquez sur l’icône du fichier ChangeNotifyWatcher. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="4aad6-128">Double-click the icon for the ChangeNotifyWatcher.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="4aad6-129">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="4aad6-129">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="4aad6-130">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="4aad6-130">Running the Sample</span></span>

1.  <span data-ttu-id="4aad6-131">Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="4aad6-131">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="4aad6-132">À l'invite de commandes, entrez `ChangeNotifyWatcher.exe`.</span><span class="sxs-lookup"><span data-stu-id="4aad6-132">At the command prompt, enter `ChangeNotifyWatcher.exe`.</span></span> <span data-ttu-id="4aad6-133">Vous pouvez également, à partir de l’Explorateur Windows, double-cliquer sur l’icône de ChangeNotifyWatcher.exe.</span><span class="sxs-lookup"><span data-stu-id="4aad6-133">Alternatively, from Windows Explorer double-click the icon for ChangeNotifyWatcher.exe.</span></span>
3.  <span data-ttu-id="4aad6-134">Pour illustrer l’effet, les ID de modèle d’utilisateur de l’application (AppUserModelIDs) sélectionnent un dossier à surveiller en cliquant sur **« Pick... »** ou en utilisant le glisser-déplacer sur un dossier à partir d’une fenêtre de l’Explorateur Windows dans l’affichage de liste de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="4aad6-134">To demonstrate the effect, Application User Model IDs (AppUserModelIDs) select a folder to watch by either clicking **"Pick..."** or by using drag-and-drop on a folder from a Windows Explorer window into the sample's list view.</span></span>

 

 




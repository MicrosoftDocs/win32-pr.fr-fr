---
description: Montre comment déterminer l’état de l’appartenance à un groupe résidentiel, comment énumérer les éléments de niveau supérieur dans le dossier de Shell du groupe résidentiel et comment lancer l’Assistant partage du groupe résidentiel.
title: HomeGroup, exemple
ms.topic: article
ms.date: 05/31/2018
ms.assetid: FDEFF261-BF86-4fbb-8567-892F79F23D92
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c22ea84431f464ef8fcae6bfad0d90a45ba310d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034676"
---
# <a name="homegroup-sample"></a><span data-ttu-id="3a0b9-103">HomeGroup, exemple</span><span class="sxs-lookup"><span data-stu-id="3a0b9-103">HomeGroup Sample</span></span>

<span data-ttu-id="3a0b9-104">Montre comment déterminer l’état de l’appartenance à un groupe résidentiel, comment énumérer les éléments de niveau supérieur dans le dossier de Shell du **groupe résidentiel** et comment lancer l' **Assistant partage du groupe résidentiel**.</span><span class="sxs-lookup"><span data-stu-id="3a0b9-104">Demonstrates how to determine HomeGroup membership status, enumerate top-level items in the **HomeGroup** Shell folder, and launch the **HomeGroup Sharing Wizard**.</span></span>

<span data-ttu-id="3a0b9-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="3a0b9-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3a0b9-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a0b9-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="3a0b9-107">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="3a0b9-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="3a0b9-108">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="3a0b9-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="3a0b9-109">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="3a0b9-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="3a0b9-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3a0b9-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="3a0b9-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3a0b9-111">Requirements</span></span>



| <span data-ttu-id="3a0b9-112">Produit</span><span class="sxs-lookup"><span data-stu-id="3a0b9-112">Product</span></span>                                | <span data-ttu-id="3a0b9-113">Version minimale du produit</span><span class="sxs-lookup"><span data-stu-id="3a0b9-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="3a0b9-114">Windows</span><span class="sxs-lookup"><span data-stu-id="3a0b9-114">Windows</span></span>                                | <span data-ttu-id="3a0b9-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3a0b9-115">Windows 7</span></span>               |
| <span data-ttu-id="3a0b9-116">Kit de développement logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="3a0b9-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="3a0b9-117">7.0</span><span class="sxs-lookup"><span data-stu-id="3a0b9-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="3a0b9-118">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="3a0b9-118">Downloading the Sample</span></span>

| <span data-ttu-id="3a0b9-119">Emplacement</span><span class="sxs-lookup"><span data-stu-id="3a0b9-119">Location</span></span>      | <span data-ttu-id="3a0b9-120">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="3a0b9-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a0b9-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="3a0b9-121">GitHub</span></span>  | [<span data-ttu-id="3a0b9-122">Exemple de groupe résidentiel</span><span class="sxs-lookup"><span data-stu-id="3a0b9-122">HomeGroup sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/HomeGroup) |

## <a name="building-the-sample"></a><span data-ttu-id="3a0b9-123">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="3a0b9-123">Building the Sample</span></span>

<span data-ttu-id="3a0b9-124">Pour générer l’exemple à partir de l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="3a0b9-124">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="3a0b9-125">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet de **groupe résidentiel** .</span><span class="sxs-lookup"><span data-stu-id="3a0b9-125">Open the command prompt window and navigate to the **HomeGroup** project directory.</span></span>
2.  <span data-ttu-id="3a0b9-126">Entrez `msbuild HomeGroup.sln`.</span><span class="sxs-lookup"><span data-stu-id="3a0b9-126">Enter `msbuild HomeGroup.sln`.</span></span>

<span data-ttu-id="3a0b9-127">Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :</span><span class="sxs-lookup"><span data-stu-id="3a0b9-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="3a0b9-128">Ouvrez l’Explorateur Windows et accédez au répertoire du projet de **groupe résidentiel** .</span><span class="sxs-lookup"><span data-stu-id="3a0b9-128">Open Windows Explorer and navigate to the **HomeGroup** project directory.</span></span>
2.  <span data-ttu-id="3a0b9-129">Double-cliquez sur l’icône du fichier de groupe résidentiel. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3a0b9-129">Double-click the icon for the HomeGroup.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="3a0b9-130">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="3a0b9-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="3a0b9-131">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="3a0b9-131">Running the Sample</span></span>

1.  <span data-ttu-id="3a0b9-132">Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="3a0b9-132">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="3a0b9-133">Sur la ligne de commande, entrez `HomeGroup.exe` .</span><span class="sxs-lookup"><span data-stu-id="3a0b9-133">At the command line, enter `HomeGroup.exe`.</span></span> <span data-ttu-id="3a0b9-134">Vous pouvez également, à partir de l’Explorateur Windows, double-cliquer sur l’icône de HomeGroup.exe.</span><span class="sxs-lookup"><span data-stu-id="3a0b9-134">Alternatively, from Windows Explorer double-click the icon for HomeGroup.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a0b9-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3a0b9-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a0b9-136">**IHomeGroup**</span><span class="sxs-lookup"><span data-stu-id="3a0b9-136">**IHomeGroup**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihomegroup)
</dt> <dt>

[<span data-ttu-id="3a0b9-137">**KNOWNFOLDERID**</span><span class="sxs-lookup"><span data-stu-id="3a0b9-137">**KNOWNFOLDERID**</span></span>](knownfolderid.md)
</dt> </dl>

 

 




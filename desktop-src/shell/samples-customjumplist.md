---
description: Montre comment créer une liste de raccourcis personnalisée pour une application, y compris l’ajout d’une catégorie et de tâches personnalisées.
title: Liste de raccourcis personnalisée, exemple
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 60DEDB01-8F8F-4c25-8FCC-8EAC461A99B7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c20592e508a24985e0f8283993482c7bd61af232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204044"
---
# <a name="custom-jump-list-sample"></a><span data-ttu-id="91ee4-103">Liste de raccourcis personnalisée, exemple</span><span class="sxs-lookup"><span data-stu-id="91ee4-103">Custom Jump List Sample</span></span>

<span data-ttu-id="91ee4-104">Montre comment créer une liste de raccourcis personnalisée pour une application, y compris l’ajout d’une catégorie et de tâches personnalisées.</span><span class="sxs-lookup"><span data-stu-id="91ee4-104">Demonstrates how to create a custom Jump List for an application, including adding a custom category and tasks.</span></span>

<span data-ttu-id="91ee4-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="91ee4-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="91ee4-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91ee4-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="91ee4-107">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="91ee4-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="91ee4-108">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="91ee4-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="91ee4-109">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="91ee4-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="91ee4-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="91ee4-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="91ee4-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="91ee4-111">Requirements</span></span>



| <span data-ttu-id="91ee4-112">Produit</span><span class="sxs-lookup"><span data-stu-id="91ee4-112">Product</span></span>                                | <span data-ttu-id="91ee4-113">Version minimale du produit</span><span class="sxs-lookup"><span data-stu-id="91ee4-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="91ee4-114">Windows</span><span class="sxs-lookup"><span data-stu-id="91ee4-114">Windows</span></span>                                | <span data-ttu-id="91ee4-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="91ee4-115">Windows 7</span></span>               |
| <span data-ttu-id="91ee4-116">Kit de développement logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="91ee4-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="91ee4-117">7.0</span><span class="sxs-lookup"><span data-stu-id="91ee4-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="91ee4-118">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="91ee4-118">Downloading the Sample</span></span>

| <span data-ttu-id="91ee4-119">Emplacement</span><span class="sxs-lookup"><span data-stu-id="91ee4-119">Location</span></span>      | <span data-ttu-id="91ee4-120">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="91ee4-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91ee4-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="91ee4-121">GitHub</span></span>  | [<span data-ttu-id="91ee4-122">Exemple CustomJumpList</span><span class="sxs-lookup"><span data-stu-id="91ee4-122">CustomJumpList sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CustomJumpList) |

## <a name="building-the-sample"></a><span data-ttu-id="91ee4-123">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="91ee4-123">Building the Sample</span></span>

<span data-ttu-id="91ee4-124">Pour générer l’exemple à partir de l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="91ee4-124">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="91ee4-125">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **CustomJumpList** .</span><span class="sxs-lookup"><span data-stu-id="91ee4-125">Open the command prompt window and navigate to the **CustomJumpList** project directory.</span></span>
2.  <span data-ttu-id="91ee4-126">Entrez `msbuild CustomJumpListSample.sln`.</span><span class="sxs-lookup"><span data-stu-id="91ee4-126">Enter `msbuild CustomJumpListSample.sln`.</span></span>

<span data-ttu-id="91ee4-127">Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :</span><span class="sxs-lookup"><span data-stu-id="91ee4-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="91ee4-128">Ouvrez l’Explorateur Windows et accédez au répertoire du projet **CustomJumpList** .</span><span class="sxs-lookup"><span data-stu-id="91ee4-128">Open Windows Explorer and navigate to the **CustomJumpList** project directory.</span></span>
2.  <span data-ttu-id="91ee4-129">Double-cliquez sur l’icône du fichier CustomJumpListSample. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="91ee4-129">Double-click the icon for the CustomJumpListSample.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="91ee4-130">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="91ee4-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="91ee4-131">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="91ee4-131">Running the Sample</span></span>

1.  <span data-ttu-id="91ee4-132">Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="91ee4-132">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="91ee4-133">Sur la ligne de commande, entrez `CustomJumpListSample.exe` .</span><span class="sxs-lookup"><span data-stu-id="91ee4-133">At the command line, enter `CustomJumpListSample.exe`.</span></span> <span data-ttu-id="91ee4-134">Vous pouvez également, à partir de l’Explorateur Windows, double-cliquer sur l’icône de CustomJumpListSample.exe.</span><span class="sxs-lookup"><span data-stu-id="91ee4-134">Alternatively, from Windows Explorer double-click the icon for CustomJumpListSample.exe.</span></span>
3.  <span data-ttu-id="91ee4-135">Cet exemple doit être exécuté en tant qu’administrateur la première fois qu’il est exécuté afin de pouvoir installer les inscriptions de types de fichiers nécessaires.</span><span class="sxs-lookup"><span data-stu-id="91ee4-135">This sample must be run as an administrator the first time it is run so that it can install the necessary file type registrations.</span></span> <span data-ttu-id="91ee4-136">Une fois les types de fichiers enregistrés, l’exemple peut s’exécuter en tant qu’utilisateur standard.</span><span class="sxs-lookup"><span data-stu-id="91ee4-136">After the file types have been registered, the sample can run as a standard user.</span></span>
4.  <span data-ttu-id="91ee4-137">Sélectionnez des options dans le menu de l’exemple d’application pour voir comment elles affectent la liste de raccourcis de l’application dans la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="91ee4-137">Select options from the menu in the sample application to see how they affect the application's Jump List in the taskbar.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91ee4-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="91ee4-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91ee4-139">ID de modèle d’utilisateur d’application (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="91ee4-139">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> </dl>

 

 




---
description: Montre comment ajouter des éléments à la liste de raccourcis automatique pour une application, y compris le basculement entre l’affichage des catégories fréquentes et récentes.
title: Liste de raccourcis automatique, exemple
ms.topic: article
ms.date: 05/31/2018
ms.assetid: C33152FE-1322-42f8-A656-3D5FAF4B612D
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ce0b6520163fcb07bb990b7a5a9fe742d976a899
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485561"
---
# <a name="automatic-jump-list-sample"></a><span data-ttu-id="21cb6-103">Liste de raccourcis automatique, exemple</span><span class="sxs-lookup"><span data-stu-id="21cb6-103">Automatic Jump List Sample</span></span>

<span data-ttu-id="21cb6-104">Montre comment ajouter des éléments à la liste de raccourcis automatique pour une application, y compris le basculement entre l’affichage des catégories fréquentes et récentes.</span><span class="sxs-lookup"><span data-stu-id="21cb6-104">Demonstrates how to add items to the automatic Jump List for an application, including switching between the display of the Frequent and Recent categories.</span></span>

<span data-ttu-id="21cb6-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="21cb6-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="21cb6-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21cb6-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="21cb6-107">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="21cb6-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="21cb6-108">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="21cb6-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="21cb6-109">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="21cb6-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="21cb6-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="21cb6-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="21cb6-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="21cb6-111">Requirements</span></span>



| <span data-ttu-id="21cb6-112">Produit</span><span class="sxs-lookup"><span data-stu-id="21cb6-112">Product</span></span>                                | <span data-ttu-id="21cb6-113">Version minimale du produit</span><span class="sxs-lookup"><span data-stu-id="21cb6-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="21cb6-114">Windows</span><span class="sxs-lookup"><span data-stu-id="21cb6-114">Windows</span></span>                                | <span data-ttu-id="21cb6-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="21cb6-115">Windows 7</span></span>               |
| <span data-ttu-id="21cb6-116">Kit de développement logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="21cb6-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="21cb6-117">7.0</span><span class="sxs-lookup"><span data-stu-id="21cb6-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="21cb6-118">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="21cb6-118">Downloading the Sample</span></span>

| <span data-ttu-id="21cb6-119">Emplacement</span><span class="sxs-lookup"><span data-stu-id="21cb6-119">Location</span></span>      | <span data-ttu-id="21cb6-120">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="21cb6-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21cb6-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="21cb6-121">GitHub</span></span>  | [<span data-ttu-id="21cb6-122">Exemple AutomaticJumpList</span><span class="sxs-lookup"><span data-stu-id="21cb6-122">AutomaticJumpList sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AutomaticJumpList) |

## <a name="building-the-sample"></a><span data-ttu-id="21cb6-123">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="21cb6-123">Building the Sample</span></span>

<span data-ttu-id="21cb6-124">Pour générer l’exemple à partir de l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="21cb6-124">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="21cb6-125">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **AutomaticJumpList** .</span><span class="sxs-lookup"><span data-stu-id="21cb6-125">Open the command prompt window and navigate to the **AutomaticJumpList** project directory.</span></span>
2.  <span data-ttu-id="21cb6-126">Entrez `msbuild AutomaticJumpListSample.sln`.</span><span class="sxs-lookup"><span data-stu-id="21cb6-126">Enter `msbuild AutomaticJumpListSample.sln`.</span></span>

<span data-ttu-id="21cb6-127">Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :</span><span class="sxs-lookup"><span data-stu-id="21cb6-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="21cb6-128">Ouvrez l’Explorateur Windows et accédez au répertoire du projet **AutomaticJumpList** .</span><span class="sxs-lookup"><span data-stu-id="21cb6-128">Open Windows Explorer and navigate to the **AutomaticJumpList** project directory.</span></span>
2.  <span data-ttu-id="21cb6-129">Double-cliquez sur l’icône du fichier AutomaticJumpListSample. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="21cb6-129">Double-click the icon for the AutomaticJumpListSample.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="21cb6-130">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="21cb6-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="21cb6-131">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="21cb6-131">Running the Sample</span></span>

1.  <span data-ttu-id="21cb6-132">Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="21cb6-132">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="21cb6-133">Sur la ligne de commande, entrez `AutomaticJumpListSample.exe` .</span><span class="sxs-lookup"><span data-stu-id="21cb6-133">At the command line, enter `AutomaticJumpListSample.exe`.</span></span> <span data-ttu-id="21cb6-134">Vous pouvez également, à partir de l’Explorateur Windows, double-cliquer sur l’icône de AutomaticJumpListSample.exe.</span><span class="sxs-lookup"><span data-stu-id="21cb6-134">Alternatively, from Windows Explorer double-click the icon for AutomaticJumpListSample.exe.</span></span>
3.  <span data-ttu-id="21cb6-135">Cet exemple doit être exécuté en tant qu’administrateur la première fois qu’il est exécuté afin de pouvoir installer les inscriptions de types de fichiers nécessaires.</span><span class="sxs-lookup"><span data-stu-id="21cb6-135">This sample must be run as an administrator the first time it is run so that it can install the necessary file type registrations.</span></span> <span data-ttu-id="21cb6-136">Une fois les types de fichiers enregistrés, l’exemple peut s’exécuter en tant qu’utilisateur standard.</span><span class="sxs-lookup"><span data-stu-id="21cb6-136">After the file types have been registered, the sample can run as a standard user.</span></span>
4.  <span data-ttu-id="21cb6-137">Sélectionnez des options dans le menu de l’exemple d’application, notamment la sélection des documents. txt ou. doc via la boîte de dialogue **ouvrir** pour voir comment ils affectent la liste de raccourcis de l’application dans la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="21cb6-137">Select options from the menu in the sample application, including the selection of .txt or .doc documents through the **Open** dialog to see how they affect the application's Jump List in the taskbar.</span></span>

## <a name="related-topics"></a><span data-ttu-id="21cb6-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="21cb6-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21cb6-139">ID de modèle d’utilisateur d’application (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="21cb6-139">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> </dl>

 

 




---
description: Montre comment créer un verbe qui fonctionne sur un élément de Shell ou un conteneur sélectionné pour créer une sélection.
title: Créateur de playlist, exemple
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B35B7A18-2163-4860-BC50-8918056C9F4A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5c5e4f6570faff459126a32ea4680d41a3b8302e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973834"
---
# <a name="playlist-creator-sample"></a><span data-ttu-id="6f8c0-103">Créateur de playlist, exemple</span><span class="sxs-lookup"><span data-stu-id="6f8c0-103">Playlist Creator Sample</span></span>

<span data-ttu-id="6f8c0-104">Montre comment créer un verbe qui fonctionne sur un élément de Shell ou un conteneur sélectionné pour créer une sélection.</span><span class="sxs-lookup"><span data-stu-id="6f8c0-104">Demonstrates how to create a verb that operates on a selected Shell item or container to create a playlist.</span></span>

<span data-ttu-id="6f8c0-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="6f8c0-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="6f8c0-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f8c0-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="6f8c0-107">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="6f8c0-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="6f8c0-108">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="6f8c0-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="6f8c0-109">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="6f8c0-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="6f8c0-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6f8c0-110">Requirements</span></span>



| <span data-ttu-id="6f8c0-111">Produit</span><span class="sxs-lookup"><span data-stu-id="6f8c0-111">Product</span></span>                                | <span data-ttu-id="6f8c0-112">Version minimale du produit</span><span class="sxs-lookup"><span data-stu-id="6f8c0-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="6f8c0-113">Windows</span><span class="sxs-lookup"><span data-stu-id="6f8c0-113">Windows</span></span>                                | <span data-ttu-id="6f8c0-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f8c0-114">Windows Vista</span></span>           |
| <span data-ttu-id="6f8c0-115">Kit de développement logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="6f8c0-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="6f8c0-116">7.0</span><span class="sxs-lookup"><span data-stu-id="6f8c0-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="6f8c0-117">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="6f8c0-117">Downloading the Sample</span></span>

| <span data-ttu-id="6f8c0-118">Emplacement</span><span class="sxs-lookup"><span data-stu-id="6f8c0-118">Location</span></span>      | <span data-ttu-id="6f8c0-119">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="6f8c0-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f8c0-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="6f8c0-120">GitHub</span></span>  | [<span data-ttu-id="6f8c0-121">Exemple PlaylistCreator</span><span class="sxs-lookup"><span data-stu-id="6f8c0-121">PlaylistCreator sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/PlaylistCreator) |

## <a name="building-the-sample"></a><span data-ttu-id="6f8c0-122">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="6f8c0-122">Building the Sample</span></span>

<span data-ttu-id="6f8c0-123">Pour générer l’exemple à partir de l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="6f8c0-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="6f8c0-124">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **PlaylistCreator** .</span><span class="sxs-lookup"><span data-stu-id="6f8c0-124">Open the command prompt window and navigate to the **PlaylistCreator** project directory.</span></span>
2.  <span data-ttu-id="6f8c0-125">Entrez `msbuild PlaylistCreator.sln`.</span><span class="sxs-lookup"><span data-stu-id="6f8c0-125">Enter `msbuild PlaylistCreator.sln`.</span></span>

<span data-ttu-id="6f8c0-126">Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :</span><span class="sxs-lookup"><span data-stu-id="6f8c0-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

> [!Note]  
> <span data-ttu-id="6f8c0-127">Cet exemple peut également être utilisé avec l’édition Visual C++ Express si la version complète de Visual Studio n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="6f8c0-127">This sample can also be used with the Visual C++ Express Edition if the full Visual Studio is not available.</span></span>

 

1.  <span data-ttu-id="6f8c0-128">Ouvrez l’Explorateur Windows et accédez au répertoire du projet **PlaylistCreator** .</span><span class="sxs-lookup"><span data-stu-id="6f8c0-128">Open Windows Explorer and navigate to the **PlaylistCreator** project directory.</span></span>
2.  <span data-ttu-id="6f8c0-129">Double-cliquez sur l’icône du fichier PlaylistCreator. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="6f8c0-129">Double-click the icon for the PlaylistCreator.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="6f8c0-130">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="6f8c0-130">From the **Build** menu, select **Build Solution**.</span></span>
    > [!Note]  
    > <span data-ttu-id="6f8c0-131">Si vous compilez 64 bits à l’aide de l’édition Visual C++ Express, vous devez utiliser le compilateur croisé x64 fourni avec le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="6f8c0-131">If you are compiling 64-bit using the Visual C++ Express Edition, you must to use the x64 cross-compiler supplied with the Windows SDK.</span></span>

     

## <a name="running-the-sample"></a><span data-ttu-id="6f8c0-132">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="6f8c0-132">Running the Sample</span></span>

1.  <span data-ttu-id="6f8c0-133">Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="6f8c0-133">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="6f8c0-134">Sur la ligne de commande, entrez `PlaylistCreator.exe` .</span><span class="sxs-lookup"><span data-stu-id="6f8c0-134">At the command line, enter `PlaylistCreator.exe`.</span></span> <span data-ttu-id="6f8c0-135">Vous pouvez également, à partir de l’Explorateur Windows, double-cliquer sur l’icône de PlaylistCreator.exe.</span><span class="sxs-lookup"><span data-stu-id="6f8c0-135">Alternatively, from Windows Explorer double-click the icon for PlaylistCreator.exe.</span></span>
3.  <span data-ttu-id="6f8c0-136">Cliquez avec le bouton droit sur un fichier ou un dossier musical contenant des fichiers musicaux dans l’Explorateur Windows pour créer une sélection et afficher le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="6f8c0-136">Right-click any music file or folder containing music files in Windows Explorer to create a playlist to bring up the context menu</span></span>
4.  <span data-ttu-id="6f8c0-137">Vous pouvez créer une sélection. m3u ou. wpl.</span><span class="sxs-lookup"><span data-stu-id="6f8c0-137">You can create a .m3u or .wpl playlist.</span></span> <span data-ttu-id="6f8c0-138">Les sélections sont créées dans le `%userprofile%\Music\Playlists` dossier.</span><span class="sxs-lookup"><span data-stu-id="6f8c0-138">Playlists are created in the `%userprofile%\Music\Playlists` folder.</span></span>
    > [!Note]  
    > <span data-ttu-id="6f8c0-139">Vous pouvez trouver de nouveaux verbes dans le menu contextuel dans le dossier **musique** , les piles musicales, les piles de la **Médiathèque** et les collections de fichiers musicaux.</span><span class="sxs-lookup"><span data-stu-id="6f8c0-139">New verbs in the context menu can be found in the **Music** folder, music stacks, stacks in the **Music Library**, and collections of music files.</span></span>

     

 

 




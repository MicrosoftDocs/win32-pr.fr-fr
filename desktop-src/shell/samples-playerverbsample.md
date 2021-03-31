---
description: Montre comment créer un verbe qui fonctionne sur des éléments de Shell et des conteneurs qui lit des éléments ou ajoute des éléments à une file d’attente.
title: Player, exemple de verbe
ms.topic: article
ms.date: 05/31/2018
ms.assetid: ABD905DD-F216-495e-A052-E43D93DD3D6B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b8346d54bfb99c5f1870812775b31097d850025f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203258"
---
# <a name="player-verb-sample"></a><span data-ttu-id="2c47e-103">Player, exemple de verbe</span><span class="sxs-lookup"><span data-stu-id="2c47e-103">Player Verb Sample</span></span>

<span data-ttu-id="2c47e-104">Montre comment créer un verbe qui fonctionne sur des éléments de Shell et des conteneurs qui lit des éléments ou ajoute des éléments à une file d’attente.</span><span class="sxs-lookup"><span data-stu-id="2c47e-104">Demonstrates how to create a verb that operates on Shell items and containers which plays items or adds items to a queue.</span></span> <span data-ttu-id="2c47e-105">Cet exemple est particulièrement utile pour les applications multimédias.</span><span class="sxs-lookup"><span data-stu-id="2c47e-105">This sample is particularly useful for media applications.</span></span>

<span data-ttu-id="2c47e-106">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="2c47e-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="2c47e-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c47e-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="2c47e-108">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="2c47e-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="2c47e-109">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="2c47e-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="2c47e-110">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="2c47e-110">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="2c47e-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2c47e-111">Requirements</span></span>



| <span data-ttu-id="2c47e-112">Produit</span><span class="sxs-lookup"><span data-stu-id="2c47e-112">Product</span></span>                                | <span data-ttu-id="2c47e-113">Version minimale du produit</span><span class="sxs-lookup"><span data-stu-id="2c47e-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="2c47e-114">Windows</span><span class="sxs-lookup"><span data-stu-id="2c47e-114">Windows</span></span>                                | <span data-ttu-id="2c47e-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c47e-115">Windows Vista</span></span>           |
| <span data-ttu-id="2c47e-116">Kit de développement logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="2c47e-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="2c47e-117">7.0</span><span class="sxs-lookup"><span data-stu-id="2c47e-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="2c47e-118">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="2c47e-118">Downloading the Sample</span></span>

| <span data-ttu-id="2c47e-119">Emplacement</span><span class="sxs-lookup"><span data-stu-id="2c47e-119">Location</span></span>      | <span data-ttu-id="2c47e-120">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="2c47e-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c47e-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="2c47e-121">GitHub</span></span>  | [<span data-ttu-id="2c47e-122">Exemple PlayerVerb</span><span class="sxs-lookup"><span data-stu-id="2c47e-122">PlayerVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/PlayerVerbSample) |

## <a name="building-the-sample"></a><span data-ttu-id="2c47e-123">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="2c47e-123">Building the Sample</span></span>

<span data-ttu-id="2c47e-124">Pour générer l’exemple à partir de l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="2c47e-124">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="2c47e-125">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **PlayerVerbSample** .</span><span class="sxs-lookup"><span data-stu-id="2c47e-125">Open the command prompt window and navigate to the **PlayerVerbSample** project directory.</span></span>
2.  <span data-ttu-id="2c47e-126">Entrez `msbuild PlayerVerbSample.sln`.</span><span class="sxs-lookup"><span data-stu-id="2c47e-126">Enter `msbuild PlayerVerbSample.sln`.</span></span>

<span data-ttu-id="2c47e-127">Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :</span><span class="sxs-lookup"><span data-stu-id="2c47e-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="2c47e-128">Ouvrez l’Explorateur Windows et accédez au répertoire du projet **PlayerVerbSample** .</span><span class="sxs-lookup"><span data-stu-id="2c47e-128">Open Windows Explorer and navigate to the **PlayerVerbSample** project directory.</span></span>
2.  <span data-ttu-id="2c47e-129">Double-cliquez sur l’icône du fichier PlayerVerbSample. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="2c47e-129">Double-click the icon for the PlayerVerbSample.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="2c47e-130">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="2c47e-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="2c47e-131">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="2c47e-131">Running the Sample</span></span>

1.  <span data-ttu-id="2c47e-132">Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="2c47e-132">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="2c47e-133">Sur la ligne de commande, entrez `PlayerVerbSample.exe` .</span><span class="sxs-lookup"><span data-stu-id="2c47e-133">At the command line, enter `PlayerVerbSample.exe`.</span></span> <span data-ttu-id="2c47e-134">Vous pouvez également, à partir de l’Explorateur Windows, double-cliquer sur l’icône de PlayerVerbSample.exe.</span><span class="sxs-lookup"><span data-stu-id="2c47e-134">Alternatively, from Windows Explorer double-click the icon for PlayerVerbSample.exe.</span></span>
3.  <span data-ttu-id="2c47e-135">Sélectionnez `Register Verbs` dans la boîte de dialogue **exemple de verbe de joueur** .</span><span class="sxs-lookup"><span data-stu-id="2c47e-135">Select `Register Verbs` in the **Player Verb Sample** dialog.</span></span>
4.  <span data-ttu-id="2c47e-136">Cliquez avec le bouton droit sur les éléments d’image (fichier, dossier ou pile) dans l’Explorateur Windows pour les ajouter à une file d’attente ou les lire dans l’exemple d’application.</span><span class="sxs-lookup"><span data-stu-id="2c47e-136">Right-click picture items (file, folder, or stack) in Windows Explorer to add them to a queue or play them in the sample application.</span></span> <span data-ttu-id="2c47e-137">Utilisez des éléments musicaux lorsque vous modifiez l’exemple pour utiliser de la musique.</span><span class="sxs-lookup"><span data-stu-id="2c47e-137">Use music items when you change the sample to work with music.</span></span>

 

 




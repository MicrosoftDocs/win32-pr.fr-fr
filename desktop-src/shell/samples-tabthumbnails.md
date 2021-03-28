---
description: Montre comment une application peut exposer plusieurs cibles de commutateur (comme pour les onglets) sur un TaskBand et comment fournir leurs miniatures.
title: TabThumbnails, exemple
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 3F48EAA2-98A3-4530-9FC6-A395987157B7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 323604d104be3432a5fc251901c4308bfc989f90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973746"
---
# <a name="tabthumbnails-sample"></a><span data-ttu-id="4ab95-103">TabThumbnails, exemple</span><span class="sxs-lookup"><span data-stu-id="4ab95-103">TabThumbnails Sample</span></span>

<span data-ttu-id="4ab95-104">Montre comment une application peut exposer plusieurs cibles de commutateur (comme pour les onglets) sur un TaskBand et comment fournir leurs miniatures.</span><span class="sxs-lookup"><span data-stu-id="4ab95-104">Demonstrates how an application can expose multiple switch targets (as for tabs) on a taskband and how to provide their thumbnails.</span></span>

<span data-ttu-id="4ab95-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="4ab95-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="4ab95-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4ab95-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="4ab95-107">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="4ab95-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="4ab95-108">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="4ab95-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="4ab95-109">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="4ab95-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="4ab95-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4ab95-110">Requirements</span></span>



| <span data-ttu-id="4ab95-111">Produit</span><span class="sxs-lookup"><span data-stu-id="4ab95-111">Product</span></span>                                | <span data-ttu-id="4ab95-112">Version minimale du produit</span><span class="sxs-lookup"><span data-stu-id="4ab95-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="4ab95-113">Windows</span><span class="sxs-lookup"><span data-stu-id="4ab95-113">Windows</span></span>                                | <span data-ttu-id="4ab95-114">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4ab95-114">Windows 7</span></span>               |
| <span data-ttu-id="4ab95-115">Kit de développement logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="4ab95-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="4ab95-116">7.0</span><span class="sxs-lookup"><span data-stu-id="4ab95-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="4ab95-117">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="4ab95-117">Downloading the Sample</span></span>

| <span data-ttu-id="4ab95-118">Emplacement</span><span class="sxs-lookup"><span data-stu-id="4ab95-118">Location</span></span>      | <span data-ttu-id="4ab95-119">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="4ab95-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ab95-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="4ab95-120">GitHub</span></span>  | [<span data-ttu-id="4ab95-121">Exemple TabThumbnails</span><span class="sxs-lookup"><span data-stu-id="4ab95-121">TabThumbnails sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TabThumbnails) |

## <a name="building-the-sample"></a><span data-ttu-id="4ab95-122">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="4ab95-122">Building the Sample</span></span>

<span data-ttu-id="4ab95-123">Pour générer l’exemple à partir de l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="4ab95-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="4ab95-124">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **TabThumbnails** .</span><span class="sxs-lookup"><span data-stu-id="4ab95-124">Open the command prompt window and navigate to the **TabThumbnails** project directory.</span></span>
2.  <span data-ttu-id="4ab95-125">Entrez `msbuild TabThumbnails.sln`.</span><span class="sxs-lookup"><span data-stu-id="4ab95-125">Enter `msbuild TabThumbnails.sln`.</span></span>

<span data-ttu-id="4ab95-126">Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :</span><span class="sxs-lookup"><span data-stu-id="4ab95-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="4ab95-127">Ouvrez l’Explorateur Windows et accédez au répertoire du projet **TabThumbnails** .</span><span class="sxs-lookup"><span data-stu-id="4ab95-127">Open Windows Explorer and navigate to the **TabThumbnails** project directory.</span></span>
2.  <span data-ttu-id="4ab95-128">Double-cliquez sur l’icône du fichier TabThumbnails. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="4ab95-128">Double-click the icon for the TabThumbnails.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="4ab95-129">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="4ab95-129">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="4ab95-130">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="4ab95-130">Running the Sample</span></span>

1.  <span data-ttu-id="4ab95-131">Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="4ab95-131">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="4ab95-132">Sur la ligne de commande, entrez `TabThumbnails.exe` .</span><span class="sxs-lookup"><span data-stu-id="4ab95-132">At the command line, enter `TabThumbnails.exe`.</span></span> <span data-ttu-id="4ab95-133">Vous pouvez également, à partir de l’Explorateur Windows, double-cliquer sur l’icône de TabThumbnails.exe.</span><span class="sxs-lookup"><span data-stu-id="4ab95-133">Alternatively, from Windows Explorer double-click the icon for TabThumbnails.exe.</span></span>

 

 




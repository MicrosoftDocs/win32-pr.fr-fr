---
description: L’exemple de code DSearch montre comment créer une classe pour une application console statique afin d’interroger Windows Search à l’aide de l’assembly Microsoft. Search. Interop pour ISearchQueryHelper.
ms.assetid: 9c09b1fe-c63e-4c6e-9c8b-f5e29cf0fe9e
title: DSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4285596a8109361accd6b3adecf80ea98074e55e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544626"
---
# <a name="dsearch"></a><span data-ttu-id="6decc-103">DSearch</span><span class="sxs-lookup"><span data-stu-id="6decc-103">DSearch</span></span>

<span data-ttu-id="6decc-104">L’exemple de code DSearch montre comment créer une classe pour une application console statique afin d’interroger Windows Search à l’aide de l’assembly Microsoft. Search. Interop pour [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper).</span><span class="sxs-lookup"><span data-stu-id="6decc-104">The DSearch code sample demonstrates how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper).</span></span>

<span data-ttu-id="6decc-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="6decc-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="6decc-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6decc-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="6decc-107">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="6decc-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="6decc-108">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="6decc-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="6decc-109">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="6decc-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="6decc-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6decc-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="6decc-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6decc-111">Requirements</span></span>

| <span data-ttu-id="6decc-112">Produit</span><span class="sxs-lookup"><span data-stu-id="6decc-112">Product</span></span>     | <span data-ttu-id="6decc-113">Version du produit</span><span class="sxs-lookup"><span data-stu-id="6decc-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="6decc-114">Windows</span><span class="sxs-lookup"><span data-stu-id="6decc-114">Windows</span></span>     | <span data-ttu-id="6decc-115">Windows 7, 8.1 ou 10</span><span class="sxs-lookup"><span data-stu-id="6decc-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="6decc-116">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="6decc-116">Windows SDK</span></span> | <span data-ttu-id="6decc-117">7,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="6decc-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="6decc-118">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="6decc-118">Downloading the Sample</span></span>

<span data-ttu-id="6decc-119">Cet exemple est disponible à l’emplacement suivant.</span><span class="sxs-lookup"><span data-stu-id="6decc-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="6decc-120">Emplacement</span><span class="sxs-lookup"><span data-stu-id="6decc-120">Location</span></span>      | <span data-ttu-id="6decc-121">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="6decc-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="6decc-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="6decc-122">GitHub</span></span>        | [<span data-ttu-id="6decc-123">Exemple DSearch</span><span class="sxs-lookup"><span data-stu-id="6decc-123">DSearch sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/DSearch)         |

> [!NOTE]  
> <span data-ttu-id="6decc-124">Pour toutes les versions de Windows, y compris Windows 7, nous vous recommandons de télécharger les exemples directement à partir de GitHub pour obtenir la version la plus récente.</span><span class="sxs-lookup"><span data-stu-id="6decc-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="6decc-125">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="6decc-125">Building the Sample</span></span>

1. <span data-ttu-id="6decc-126">Ouvrez l’Explorateur Windows et accédez au répertoire du projet **DSearch** .</span><span class="sxs-lookup"><span data-stu-id="6decc-126">Open Windows Explorer and navigate to the **DSearch** project directory.</span></span>
2. <span data-ttu-id="6decc-127">Double-cliquez sur l’icône du fichier DSearch. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="6decc-127">Double-click the icon for the DSearch.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="6decc-128">Le fichier sln a été créé sous une version antérieure de Visual Studio. par conséquent, la mise à niveau est requise si vous exécutez Visual Studio 2012 ou une version plus récente.</span><span class="sxs-lookup"><span data-stu-id="6decc-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="6decc-129">Cela n’aura pas d’impact sur le comportement de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="6decc-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="6decc-130">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="6decc-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="6decc-131">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="6decc-131">Running the Sample</span></span>

1. <span data-ttu-id="6decc-132">Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de la fenêtre d’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="6decc-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="6decc-133">À l’invite de commandes, entrez `DSearch.exe` , ou à partir de l’Explorateur Windows, double-cliquez sur l’icône de DSearch.exe.</span><span class="sxs-lookup"><span data-stu-id="6decc-133">At the command prompt, enter `DSearch.exe`, or from Windows Explorer, double-click the icon for DSearch.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6decc-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6decc-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="6decc-135">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="6decc-135">Reference</span></span>

[<span data-ttu-id="6decc-136">**ISearchQueryHelper**</span><span class="sxs-lookup"><span data-stu-id="6decc-136">**ISearchQueryHelper**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)

[<span data-ttu-id="6decc-137">**ISearchCatalogManager**</span><span class="sxs-lookup"><span data-stu-id="6decc-137">**ISearchCatalogManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[<span data-ttu-id="6decc-138">**ISearchCatalogManager2**</span><span class="sxs-lookup"><span data-stu-id="6decc-138">**ISearchCatalogManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

### <a name="other-samples"></a><span data-ttu-id="6decc-139">Autres exemples</span><span class="sxs-lookup"><span data-stu-id="6decc-139">Other Samples</span></span>

[<span data-ttu-id="6decc-140">Rechercher des exemples de code</span><span class="sxs-lookup"><span data-stu-id="6decc-140">Search Code Samples</span></span>](-search-samples-ovw.md)

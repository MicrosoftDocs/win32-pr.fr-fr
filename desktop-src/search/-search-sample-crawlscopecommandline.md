---
description: L’exemple de code CrawlScopeCommandLine montre comment définir des options de ligne de commande pour les opérations d’indexation du gestionnaire de portée d’analyse (CSM).
ms.assetid: 8c82fe18-8676-43d2-a3da-027a733ee0a4
title: CrawlScopeCommandLine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eb770c44f82af320e2b39fe679b632cf03825e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513191"
---
# <a name="crawlscopecommandline"></a><span data-ttu-id="cdca6-103">CrawlScopeCommandLine</span><span class="sxs-lookup"><span data-stu-id="cdca6-103">CrawlScopeCommandLine</span></span>

<span data-ttu-id="cdca6-104">L’exemple de code CrawlScopeCommandLine montre comment définir des options de ligne de commande pour les opérations d’indexation du gestionnaire de portée d’analyse (CSM).</span><span class="sxs-lookup"><span data-stu-id="cdca6-104">The CrawlScopeCommandLine code sample demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.</span></span>

<span data-ttu-id="cdca6-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="cdca6-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="cdca6-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cdca6-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="cdca6-107">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="cdca6-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="cdca6-108">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="cdca6-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="cdca6-109">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="cdca6-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="cdca6-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cdca6-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="cdca6-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cdca6-111">Requirements</span></span>

| <span data-ttu-id="cdca6-112">Produit</span><span class="sxs-lookup"><span data-stu-id="cdca6-112">Product</span></span>     | <span data-ttu-id="cdca6-113">Version du produit</span><span class="sxs-lookup"><span data-stu-id="cdca6-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="cdca6-114">Windows</span><span class="sxs-lookup"><span data-stu-id="cdca6-114">Windows</span></span>     | <span data-ttu-id="cdca6-115">Windows 7, 8.1 ou 10</span><span class="sxs-lookup"><span data-stu-id="cdca6-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="cdca6-116">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="cdca6-116">Windows SDK</span></span> | <span data-ttu-id="cdca6-117">7,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="cdca6-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="cdca6-118">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="cdca6-118">Downloading the Sample</span></span>

<span data-ttu-id="cdca6-119">Cet exemple est disponible à l’emplacement suivant.</span><span class="sxs-lookup"><span data-stu-id="cdca6-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="cdca6-120">Emplacement</span><span class="sxs-lookup"><span data-stu-id="cdca6-120">Location</span></span> | <span data-ttu-id="cdca6-121">Chemin d’accès ou URL</span><span class="sxs-lookup"><span data-stu-id="cdca6-121">Path or URL</span></span>                                                                |
|----------|----------------------------------------------------------------------------|
| <span data-ttu-id="cdca6-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="cdca6-122">GitHub</span></span>   |    [<span data-ttu-id="cdca6-123">Exemple CrawlScopeCommandLine</span><span class="sxs-lookup"><span data-stu-id="cdca6-123">CrawlScopeCommandLine sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/CrawlScopeCommandLine)|

> [!NOTE]  
> <span data-ttu-id="cdca6-124">Pour toutes les versions de Windows, y compris Windows 7, nous vous recommandons de télécharger les exemples directement à partir de GitHub pour obtenir la version la plus récente.</span><span class="sxs-lookup"><span data-stu-id="cdca6-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="cdca6-125">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="cdca6-125">Building the Sample</span></span>

1. <span data-ttu-id="cdca6-126">Ouvrez l’Explorateur Windows et accédez au répertoire du projet **CrawlScopeCommandLine** .</span><span class="sxs-lookup"><span data-stu-id="cdca6-126">Open Windows Explorer and navigate to the **CrawlScopeCommandLine** project directory.</span></span>
2. <span data-ttu-id="cdca6-127">Double-cliquez sur l’icône du fichier csmcmd. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="cdca6-127">Double-click the icon for the csmcmd.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="cdca6-128">Le fichier sln a été créé sous une version antérieure de Visual Studio. par conséquent, la mise à niveau est requise si vous exécutez Visual Studio 2012 ou une version plus récente.</span><span class="sxs-lookup"><span data-stu-id="cdca6-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="cdca6-129">Cela n’aura pas d’impact sur le comportement de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="cdca6-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="cdca6-130">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="cdca6-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="cdca6-131">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="cdca6-131">Running the Sample</span></span>

1. <span data-ttu-id="cdca6-132">Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de la fenêtre d’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="cdca6-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="cdca6-133">À l’invite de commandes, entrez `csmcmd.exe` , ou à partir de l’Explorateur Windows, double-cliquez sur l’icône de csmcmd.exe.</span><span class="sxs-lookup"><span data-stu-id="cdca6-133">At the command prompt, enter `csmcmd.exe`, or from Windows Explorer, double-click the icon for csmcmd.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cdca6-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cdca6-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="cdca6-135">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="cdca6-135">Reference</span></span>

[<span data-ttu-id="cdca6-136">**IEnumSearchRoots**</span><span class="sxs-lookup"><span data-stu-id="cdca6-136">**IEnumSearchRoots**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots)

[<span data-ttu-id="cdca6-137">**IEnumSearchScopeRules**</span><span class="sxs-lookup"><span data-stu-id="cdca6-137">**IEnumSearchScopeRules**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchscoperules)

[<span data-ttu-id="cdca6-138">**ISearchCrawlScopeManager**</span><span class="sxs-lookup"><span data-stu-id="cdca6-138">**ISearchCrawlScopeManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)

[<span data-ttu-id="cdca6-139">**ISearchCrawlScopeManager2**</span><span class="sxs-lookup"><span data-stu-id="cdca6-139">**ISearchCrawlScopeManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2)

[<span data-ttu-id="cdca6-140">**ISearchRoot**</span><span class="sxs-lookup"><span data-stu-id="cdca6-140">**ISearchRoot**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)

[<span data-ttu-id="cdca6-141">**ISearchScopeRule**</span><span class="sxs-lookup"><span data-stu-id="cdca6-141">**ISearchScopeRule**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule)

[<span data-ttu-id="cdca6-142">**ISearchCatalogManager**</span><span class="sxs-lookup"><span data-stu-id="cdca6-142">**ISearchCatalogManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[<span data-ttu-id="cdca6-143">**ISearchCatalogManager2**</span><span class="sxs-lookup"><span data-stu-id="cdca6-143">**ISearchCatalogManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[<span data-ttu-id="cdca6-144">**ISearchManager**</span><span class="sxs-lookup"><span data-stu-id="cdca6-144">**ISearchManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

### <a name="other-samples"></a><span data-ttu-id="cdca6-145">Autres exemples</span><span class="sxs-lookup"><span data-stu-id="cdca6-145">Other Samples</span></span>

[<span data-ttu-id="cdca6-146">Rechercher des exemples de code</span><span class="sxs-lookup"><span data-stu-id="cdca6-146">Search Code Samples</span></span>](-search-samples-ovw.md)

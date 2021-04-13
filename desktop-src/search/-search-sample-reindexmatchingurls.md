---
description: 'L’exemple de code ReindexMatchingUrls montre comment fournir trois manières de spécifier les fichiers à réindexer : les URL qui correspondent à un type de fichier, un type MIME ou une clause WHERE spécifiée.'
ms.assetid: f7b3a8a6-b464-46d4-a99c-fc56eea9b1ec
title: ReindexMatchingUrls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a7bb6ae3148f6969fc5349e1ebdf666a527282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484417"
---
# <a name="reindexmatchingurls"></a><span data-ttu-id="7cb81-103">ReindexMatchingUrls</span><span class="sxs-lookup"><span data-stu-id="7cb81-103">ReindexMatchingUrls</span></span>

<span data-ttu-id="7cb81-104">L’exemple de code ReindexMatchingUrls montre comment fournir trois manières de spécifier les fichiers à réindexer : les URL qui correspondent à un type de fichier, un type MIME ou une clause WHERE spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7cb81-104">The ReindexMatchingUrls code sample demonstrates how to provide three ways to specify the files to re-index: URLs that match a file type, mime type, or a specified WHERE clause.</span></span>

<span data-ttu-id="7cb81-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="7cb81-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="7cb81-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7cb81-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="7cb81-107">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="7cb81-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="7cb81-108">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="7cb81-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="7cb81-109">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="7cb81-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="7cb81-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7cb81-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="7cb81-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7cb81-111">Requirements</span></span>

| <span data-ttu-id="7cb81-112">Produit</span><span class="sxs-lookup"><span data-stu-id="7cb81-112">Product</span></span>     | <span data-ttu-id="7cb81-113">Version du produit</span><span class="sxs-lookup"><span data-stu-id="7cb81-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="7cb81-114">Windows</span><span class="sxs-lookup"><span data-stu-id="7cb81-114">Windows</span></span>     | <span data-ttu-id="7cb81-115">Windows 7, 8.1 ou 10</span><span class="sxs-lookup"><span data-stu-id="7cb81-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="7cb81-116">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="7cb81-116">Windows SDK</span></span> | <span data-ttu-id="7cb81-117">7,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="7cb81-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="7cb81-118">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="7cb81-118">Downloading the Sample</span></span>

<span data-ttu-id="7cb81-119">Cet exemple est disponible à l’emplacement suivant.</span><span class="sxs-lookup"><span data-stu-id="7cb81-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="7cb81-120">Emplacement</span><span class="sxs-lookup"><span data-stu-id="7cb81-120">Location</span></span>      | <span data-ttu-id="7cb81-121">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="7cb81-121">Path URL</span></span>                                                                      |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="7cb81-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="7cb81-122">GitHub</span></span>  | [<span data-ttu-id="7cb81-123">Exemple ReindexMatchingUrls</span><span class="sxs-lookup"><span data-stu-id="7cb81-123">ReindexMatchingUrls sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/ReindexMatchingUrls) |

> [!NOTE]  
> <span data-ttu-id="7cb81-124">Pour toutes les versions de Windows, y compris Windows 7, nous vous recommandons de télécharger les exemples directement à partir de GitHub pour obtenir la version la plus récente.</span><span class="sxs-lookup"><span data-stu-id="7cb81-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="7cb81-125">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="7cb81-125">Building the Sample</span></span>

1. <span data-ttu-id="7cb81-126">Ouvrez l’Explorateur Windows et accédez au répertoire du projet **ReindexMatchingUrls** .</span><span class="sxs-lookup"><span data-stu-id="7cb81-126">Open Windows Explorer and navigate to the **ReindexMatchingUrls** project directory.</span></span> <span data-ttu-id="7cb81-127">Par exemple, le chemin d’installation complet par défaut est `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\ReindexMatchingUrls` .</span><span class="sxs-lookup"><span data-stu-id="7cb81-127">For example, the full default installation path is `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\ReindexMatchingUrls`.</span></span>
2. <span data-ttu-id="7cb81-128">Double-cliquez sur l’icône du fichier REINDEX. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7cb81-128">Double-click the icon for the Reindex.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="7cb81-129">Le fichier sln a été créé sous une version antérieure de Visual Studio. par conséquent, la mise à niveau est requise si vous exécutez Visual Studio 2012 ou une version plus récente.</span><span class="sxs-lookup"><span data-stu-id="7cb81-129">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="7cb81-130">Cela n’aura pas d’impact sur le comportement de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="7cb81-130">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="7cb81-131">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="7cb81-131">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="7cb81-132">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="7cb81-132">Running the Sample</span></span>

1. <span data-ttu-id="7cb81-133">Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de la fenêtre d’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="7cb81-133">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="7cb81-134">À l’invite de commandes, entrez `Reindex.exe` , ou à partir de l’Explorateur Windows, double-cliquez sur l’icône de Reindex.exe.</span><span class="sxs-lookup"><span data-stu-id="7cb81-134">At the command prompt, enter `Reindex.exe`, or from Windows Explorer, double-click the icon for Reindex.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7cb81-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7cb81-135">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="7cb81-136">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="7cb81-136">Reference</span></span>

[<span data-ttu-id="7cb81-137">**ISearchCatalogManager**</span><span class="sxs-lookup"><span data-stu-id="7cb81-137">**ISearchCatalogManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[<span data-ttu-id="7cb81-138">**ISearchCatalogManager2**</span><span class="sxs-lookup"><span data-stu-id="7cb81-138">**ISearchCatalogManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[<span data-ttu-id="7cb81-139">**ISearchManager**</span><span class="sxs-lookup"><span data-stu-id="7cb81-139">**ISearchManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

[<span data-ttu-id="7cb81-140">**ISearchPersistentItemsChangedSink**</span><span class="sxs-lookup"><span data-stu-id="7cb81-140">**ISearchPersistentItemsChangedSink**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink)

[<span data-ttu-id="7cb81-141">**ISearchViewChangedSink**</span><span class="sxs-lookup"><span data-stu-id="7cb81-141">**ISearchViewChangedSink**</span></span>](/windows/desktop/api/searchapi/nn-searchapi-isearchviewchangedsink)

[<span data-ttu-id="7cb81-142">**définir la priorité des \_ indicateurs**</span><span class="sxs-lookup"><span data-stu-id="7cb81-142">**PRIORITIZE\_FLAGS**</span></span>](/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags)

### <a name="other-samples"></a><span data-ttu-id="7cb81-143">Autres exemples</span><span class="sxs-lookup"><span data-stu-id="7cb81-143">Other Samples</span></span>

[<span data-ttu-id="7cb81-144">Rechercher des exemples de code</span><span class="sxs-lookup"><span data-stu-id="7cb81-144">Search Code Samples</span></span>](-search-samples-ovw.md)

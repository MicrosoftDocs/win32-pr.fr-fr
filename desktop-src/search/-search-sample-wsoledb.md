---
description: L’exemple de code WSOleDB montre Active Template Library (ATL) OLE DB l’accès aux applications Windows Search et illustre deux méthodes supplémentaires pour récupérer les résultats de la recherche Windows.
ms.assetid: c81bf3af-e023-4384-8c89-0fa9c8f08773
title: WSOleDB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6cecfc308fdfa9af796e64ab8bc6273f9c4d94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862162"
---
# <a name="wsoledb"></a><span data-ttu-id="c30a2-103">WSOleDB</span><span class="sxs-lookup"><span data-stu-id="c30a2-103">WSOleDB</span></span>

<span data-ttu-id="c30a2-104">L’exemple de code WSOleDB montre Active Template Library (ATL) OLE DB l’accès aux applications Windows Search et illustre deux méthodes supplémentaires pour récupérer les résultats de la recherche Windows.</span><span class="sxs-lookup"><span data-stu-id="c30a2-104">The WSOleDB code sample demonstrates Active Template Library (ATL) OLE DB access to Windows Search applications, and demonstrates two additional methods for retrieving results from Windows Search.</span></span>

<span data-ttu-id="c30a2-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="c30a2-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="c30a2-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c30a2-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="c30a2-107">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="c30a2-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="c30a2-108">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="c30a2-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="c30a2-109">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="c30a2-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="c30a2-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c30a2-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="c30a2-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c30a2-111">Requirements</span></span>

| <span data-ttu-id="c30a2-112">Produit</span><span class="sxs-lookup"><span data-stu-id="c30a2-112">Product</span></span>     | <span data-ttu-id="c30a2-113">Version du produit</span><span class="sxs-lookup"><span data-stu-id="c30a2-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="c30a2-114">Windows</span><span class="sxs-lookup"><span data-stu-id="c30a2-114">Windows</span></span>     | <span data-ttu-id="c30a2-115">Windows 7, 8.1 ou 10</span><span class="sxs-lookup"><span data-stu-id="c30a2-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="c30a2-116">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="c30a2-116">Windows SDK</span></span> | <span data-ttu-id="c30a2-117">7,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="c30a2-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="c30a2-118">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="c30a2-118">Downloading the Sample</span></span>

<span data-ttu-id="c30a2-119">Cet exemple est disponible à l’emplacement suivant.</span><span class="sxs-lookup"><span data-stu-id="c30a2-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="c30a2-120">Emplacement</span><span class="sxs-lookup"><span data-stu-id="c30a2-120">Location</span></span>      | <span data-ttu-id="c30a2-121">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="c30a2-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="c30a2-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="c30a2-122">GitHub</span></span>        | [<span data-ttu-id="c30a2-123">Exemple WSOleDB</span><span class="sxs-lookup"><span data-stu-id="c30a2-123">WSOleDB sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSOleDB)         |

> [!NOTE]  
> <span data-ttu-id="c30a2-124">Pour toutes les versions de Windows, y compris Windows 7, nous vous recommandons de télécharger les exemples directement à partir de GitHub pour obtenir la version la plus récente.</span><span class="sxs-lookup"><span data-stu-id="c30a2-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="c30a2-125">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="c30a2-125">Building the Sample</span></span>

1. <span data-ttu-id="c30a2-126">Ouvrez l’Explorateur Windows et accédez au répertoire du projet **WSOleDB** .</span><span class="sxs-lookup"><span data-stu-id="c30a2-126">Open Windows Explorer and navigate to the **WSOleDB** project directory.</span></span>
2. <span data-ttu-id="c30a2-127">Double-cliquez sur l’icône du fichier WSOleDB. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c30a2-127">Double-click the icon for the WSOleDB.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="c30a2-128">Le fichier sln a été créé sous une version antérieure de Visual Studio. par conséquent, la mise à niveau est requise si vous exécutez Visual Studio 2012 ou une version plus récente.</span><span class="sxs-lookup"><span data-stu-id="c30a2-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="c30a2-129">Cela n’aura pas d’impact sur le comportement de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="c30a2-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="c30a2-130">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="c30a2-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="c30a2-131">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="c30a2-131">Running the Sample</span></span>

1. <span data-ttu-id="c30a2-132">Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de la fenêtre d’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="c30a2-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="c30a2-133">À l’invite de commandes, entrez `WSOleDB.exe` , ou à partir de l’Explorateur Windows, double-cliquez sur l’icône de WSOleDB.exe.</span><span class="sxs-lookup"><span data-stu-id="c30a2-133">At the command prompt, enter `WSOleDB.exe`, or from Windows Explorer, double-click the icon for WSOleDB.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c30a2-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c30a2-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="c30a2-135">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="c30a2-135">Reference</span></span>

[<span data-ttu-id="c30a2-136">**ISearchCatalogManager**</span><span class="sxs-lookup"><span data-stu-id="c30a2-136">**ISearchCatalogManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[<span data-ttu-id="c30a2-137">**ISearchCatalogManager2**</span><span class="sxs-lookup"><span data-stu-id="c30a2-137">**ISearchCatalogManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[<span data-ttu-id="c30a2-138">**ISearchManager**</span><span class="sxs-lookup"><span data-stu-id="c30a2-138">**ISearchManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

[<span data-ttu-id="c30a2-139">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="c30a2-139">**IPropertyStore**</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)

### <a name="conceptual"></a><span data-ttu-id="c30a2-140">Conceptuel</span><span class="sxs-lookup"><span data-stu-id="c30a2-140">Conceptual</span></span>

[<span data-ttu-id="c30a2-141">Vue d’ensemble de la programmation OLE DB</span><span class="sxs-lookup"><span data-stu-id="c30a2-141">OLE DB Programming Overview</span></span>](/cpp/data/oledb/ole-db-programming-overview)

### <a name="other-samples"></a><span data-ttu-id="c30a2-142">Autres exemples</span><span class="sxs-lookup"><span data-stu-id="c30a2-142">Other Samples</span></span>

[<span data-ttu-id="c30a2-143">Rechercher des exemples de code</span><span class="sxs-lookup"><span data-stu-id="c30a2-143">Search Code Samples</span></span>](-search-samples-ovw.md)

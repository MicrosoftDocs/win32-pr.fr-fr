---
description: L’exemple de code IFilterSample montre comment créer une classe de base IFilter pour l’implémentation de l’interface IFilter.
ms.assetid: 4c0df747-627d-4937-a117-d43137d5d081
title: IFilterSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10f66bf32c4abe25038aa6b2a3b6d879ba65cf7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516840"
---
# <a name="ifiltersample"></a><span data-ttu-id="a0665-103">IFilterSample</span><span class="sxs-lookup"><span data-stu-id="a0665-103">IFilterSample</span></span>

<span data-ttu-id="a0665-104">L’exemple de code IFilterSample montre comment créer une classe de base IFilter pour l’implémentation de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="a0665-104">The IFilterSample code sample demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>

<span data-ttu-id="a0665-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="a0665-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="a0665-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0665-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="a0665-107">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="a0665-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="a0665-108">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="a0665-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="a0665-109">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="a0665-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="a0665-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a0665-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="a0665-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0665-111">Requirements</span></span>

| <span data-ttu-id="a0665-112">Produit</span><span class="sxs-lookup"><span data-stu-id="a0665-112">Product</span></span>     | <span data-ttu-id="a0665-113">Version du produit</span><span class="sxs-lookup"><span data-stu-id="a0665-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="a0665-114">Windows</span><span class="sxs-lookup"><span data-stu-id="a0665-114">Windows</span></span>     | <span data-ttu-id="a0665-115">Windows 7, 8.1 ou 10</span><span class="sxs-lookup"><span data-stu-id="a0665-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="a0665-116">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="a0665-116">Windows SDK</span></span> | <span data-ttu-id="a0665-117">7,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a0665-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="a0665-118">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="a0665-118">Downloading the Sample</span></span>

<span data-ttu-id="a0665-119">Cet exemple est disponible à l’emplacement suivant.</span><span class="sxs-lookup"><span data-stu-id="a0665-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="a0665-120">Emplacement</span><span class="sxs-lookup"><span data-stu-id="a0665-120">Location</span></span>      | <span data-ttu-id="a0665-121">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="a0665-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="a0665-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="a0665-122">GitHub</span></span>        | [<span data-ttu-id="a0665-123">IFilterSample</span><span class="sxs-lookup"><span data-stu-id="a0665-123">IFilterSample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)          |

> [!NOTE]  
> <span data-ttu-id="a0665-124">Pour toutes les versions de Windows, y compris Windows 7, nous vous recommandons de télécharger les exemples directement à partir de GitHub pour obtenir la version la plus récente.</span><span class="sxs-lookup"><span data-stu-id="a0665-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="a0665-125">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="a0665-125">Building the Sample</span></span>

1. <span data-ttu-id="a0665-126">Ouvrez l’Explorateur Windows et accédez au répertoire du projet **FilterBase** .</span><span class="sxs-lookup"><span data-stu-id="a0665-126">Open Windows Explorer and navigate to the **FilterBase** project directory.</span></span>
2. <span data-ttu-id="a0665-127">Double-cliquez sur l’icône du fichier FilterBase. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a0665-127">Double-click the icon for the FilterBase.sln file to open the project in Visual Studio.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="a0665-128">Le fichier sln a été créé sous une version antérieure de Visual Studio. par conséquent, la mise à niveau est requise si vous exécutez Visual Studio 2012 ou une version plus récente.</span><span class="sxs-lookup"><span data-stu-id="a0665-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="a0665-129">Cela n’aura pas d’impact sur le comportement de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="a0665-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="a0665-130">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="a0665-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="a0665-131">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="a0665-131">Running the Sample</span></span>

1. <span data-ttu-id="a0665-132">Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de la fenêtre d’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="a0665-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="a0665-133">À l’invite de commandes, entrez `FilterBase.exe` , ou à partir de l’Explorateur Windows, double-cliquez sur l’icône de FilterBase.exe.</span><span class="sxs-lookup"><span data-stu-id="a0665-133">At the command prompt, enter `FilterBase.exe`, or from Windows Explorer, double-click the icon for FilterBase.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0665-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a0665-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="a0665-135">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="a0665-135">Reference</span></span>

[<span data-ttu-id="a0665-136">**Filtres**</span><span class="sxs-lookup"><span data-stu-id="a0665-136">**IFilter**</span></span>](/windows/win32/api/filter/nn-filter-ifilter)

### <a name="conceptual"></a><span data-ttu-id="a0665-137">Conceptuel</span><span class="sxs-lookup"><span data-stu-id="a0665-137">Conceptual</span></span>

[<span data-ttu-id="a0665-138">Développement de gestionnaires de filtres</span><span class="sxs-lookup"><span data-stu-id="a0665-138">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)

### <a name="other-samples"></a><span data-ttu-id="a0665-139">Autres exemples</span><span class="sxs-lookup"><span data-stu-id="a0665-139">Other Samples</span></span>

[<span data-ttu-id="a0665-140">Rechercher des exemples de code</span><span class="sxs-lookup"><span data-stu-id="a0665-140">Search Code Samples</span></span>](-search-samples-ovw.md)

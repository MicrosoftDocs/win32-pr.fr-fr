---
description: L’exemple de code StructuredQuerySample montre comment lire des lignes à partir de la console, les analyser à l’aide du schéma système et afficher les arborescences de condition résultantes.
ms.assetid: 9bb56d80-670e-4b2b-bf3f-40d0a75a89b6
title: StructuredQuerySample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64da74b56658f74b056c64c314a2986ddce45ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515213"
---
# <a name="structuredquerysample"></a><span data-ttu-id="e9992-103">StructuredQuerySample</span><span class="sxs-lookup"><span data-stu-id="e9992-103">StructuredQuerySample</span></span>

<span data-ttu-id="e9992-104">L’exemple de code StructuredQuerySample montre comment lire des lignes à partir de la console, les analyser à l’aide du schéma système et afficher les arborescences de condition résultantes.</span><span class="sxs-lookup"><span data-stu-id="e9992-104">The StructuredQuerySample code sample demonstrates how to read lines from the console, parse them using the system schema, and display the resulting condition trees.</span></span>

<span data-ttu-id="e9992-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="e9992-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="e9992-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9992-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="e9992-107">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="e9992-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="e9992-108">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="e9992-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="e9992-109">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="e9992-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="e9992-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e9992-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="e9992-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9992-111">Requirements</span></span>

| <span data-ttu-id="e9992-112">Produit</span><span class="sxs-lookup"><span data-stu-id="e9992-112">Product</span></span>     | <span data-ttu-id="e9992-113">Version du produit</span><span class="sxs-lookup"><span data-stu-id="e9992-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="e9992-114">Windows</span><span class="sxs-lookup"><span data-stu-id="e9992-114">Windows</span></span>     | <span data-ttu-id="e9992-115">Windows 7, 8.1 ou 10</span><span class="sxs-lookup"><span data-stu-id="e9992-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="e9992-116">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="e9992-116">Windows SDK</span></span> | <span data-ttu-id="e9992-117">7,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="e9992-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="e9992-118">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="e9992-118">Downloading the Sample</span></span>

<span data-ttu-id="e9992-119">Cet exemple est disponible à l’emplacement suivant.</span><span class="sxs-lookup"><span data-stu-id="e9992-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="e9992-120">Emplacement</span><span class="sxs-lookup"><span data-stu-id="e9992-120">Location</span></span>      | <span data-ttu-id="e9992-121">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="e9992-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="e9992-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="e9992-122">GitHub</span></span>        | [<span data-ttu-id="e9992-123">StructuredQuerySample</span><span class="sxs-lookup"><span data-stu-id="e9992-123">StructuredQuerySample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/StructuredQuerySample)  |

> [!NOTE]  
> <span data-ttu-id="e9992-124">Pour toutes les versions de Windows, y compris Windows 7, nous vous recommandons de télécharger les exemples directement à partir de GitHub pour obtenir la version la plus récente.</span><span class="sxs-lookup"><span data-stu-id="e9992-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="e9992-125">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="e9992-125">Building the Sample</span></span>

1. <span data-ttu-id="e9992-126">Ouvrez l’Explorateur Windows et accédez au répertoire du projet **StructuredQuerySample** .</span><span class="sxs-lookup"><span data-stu-id="e9992-126">Open Windows Explorer and navigate to the **StructuredQuerySample** project directory.</span></span>
2. <span data-ttu-id="e9992-127">Double-cliquez sur l’icône du fichier StructuredQuerySample. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e9992-127">Double-click the icon for the StructuredQuerySample.sln file to open the project in Visual Studio.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="e9992-128">Le fichier sln a été créé sous une version antérieure de Visual Studio. par conséquent, la mise à niveau est requise si vous exécutez Visual Studio 2012 ou une version plus récente.</span><span class="sxs-lookup"><span data-stu-id="e9992-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="e9992-129">Cela n’aura pas d’impact sur le comportement de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="e9992-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="e9992-130">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="e9992-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="e9992-131">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="e9992-131">Running the Sample</span></span>

1. <span data-ttu-id="e9992-132">Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de la fenêtre d’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="e9992-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="e9992-133">À l’invite de commandes, entrez `StructuredQuerySample.exe` , ou à partir de l’Explorateur Windows, double-cliquez sur l’icône de StructuredQuerySample.exe.</span><span class="sxs-lookup"><span data-stu-id="e9992-133">At the command prompt, enter `StructuredQuerySample.exe`, or from Windows Explorer, double-click the icon for StructuredQuerySample.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9992-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e9992-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="e9992-135">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="e9992-135">Reference</span></span>

[<span data-ttu-id="e9992-136">**ICondition**</span><span class="sxs-lookup"><span data-stu-id="e9992-136">**ICondition**</span></span>](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition)

[<span data-ttu-id="e9992-137">**ICondition2**</span><span class="sxs-lookup"><span data-stu-id="e9992-137">**ICondition2**</span></span>](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition2)

[<span data-ttu-id="e9992-138">**IConditionFactory**</span><span class="sxs-lookup"><span data-stu-id="e9992-138">**IConditionFactory**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory)

[<span data-ttu-id="e9992-139">**IConditionFactory2**</span><span class="sxs-lookup"><span data-stu-id="e9992-139">**IConditionFactory2**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory2)

[<span data-ttu-id="e9992-140">**IConditionGenerator**</span><span class="sxs-lookup"><span data-stu-id="e9992-140">**IConditionGenerator**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator)

[<span data-ttu-id="e9992-141">**IQueryParser**</span><span class="sxs-lookup"><span data-stu-id="e9992-141">**IQueryParser**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser)

[<span data-ttu-id="e9992-142">**IQueryParserManager**</span><span class="sxs-lookup"><span data-stu-id="e9992-142">**IQueryParserManager**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparsermanager)

[<span data-ttu-id="e9992-143">**IQuerySolution**</span><span class="sxs-lookup"><span data-stu-id="e9992-143">**IQuerySolution**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution)

### <a name="other-samples"></a><span data-ttu-id="e9992-144">Autres exemples</span><span class="sxs-lookup"><span data-stu-id="e9992-144">Other Samples</span></span>

[<span data-ttu-id="e9992-145">Rechercher des exemples de code</span><span class="sxs-lookup"><span data-stu-id="e9992-145">Search Code Samples</span></span>](-search-samples-ovw.md)

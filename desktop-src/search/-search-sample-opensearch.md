---
description: L’exemple de code OpenSearch montre comment créer un service de recherche fédéré à l’aide du protocole OpenSearch et un fichier de descripteur OpenSearch (. fichier osdx) (un connecteur de recherche).
ms.assetid: 792884e4-826b-4474-82e1-1680d4d8b602
title: OpenSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8656efec434744d14714529d1e7b0d01a5349ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393459"
---
# <a name="opensearch"></a><span data-ttu-id="ffd28-103">OpenSearch</span><span class="sxs-lookup"><span data-stu-id="ffd28-103">OpenSearch</span></span>

<span data-ttu-id="ffd28-104">L’exemple de code OpenSearch montre comment créer un service de recherche fédéré à l’aide du protocole [OpenSearch](https://github.com/dewitt/opensearch) et un fichier de descripteur OpenSearch (. fichier osdx) (un connecteur de recherche).</span><span class="sxs-lookup"><span data-stu-id="ffd28-104">The OpenSearch code sample demonstrates how to create a federated search service using the [OpenSearch](https://github.com/dewitt/opensearch) protocol, and an OpenSearch Descriptor (.osdx) file (a search connector).</span></span>

<span data-ttu-id="ffd28-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="ffd28-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ffd28-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ffd28-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="ffd28-107">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="ffd28-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="ffd28-108">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="ffd28-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="ffd28-109">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="ffd28-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="ffd28-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ffd28-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="ffd28-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ffd28-111">Requirements</span></span>



| <span data-ttu-id="ffd28-112">Produit</span><span class="sxs-lookup"><span data-stu-id="ffd28-112">Product</span></span>     | <span data-ttu-id="ffd28-113">Version minimale du produit</span><span class="sxs-lookup"><span data-stu-id="ffd28-113">Minimum Product Version</span></span> |
|-------------|-------------------------|
| <span data-ttu-id="ffd28-114">Windows</span><span class="sxs-lookup"><span data-stu-id="ffd28-114">Windows</span></span>     | <span data-ttu-id="ffd28-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ffd28-115">Windows 7</span></span>               |
| <span data-ttu-id="ffd28-116">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="ffd28-116">Windows SDK</span></span> | <span data-ttu-id="ffd28-117">7.0</span><span class="sxs-lookup"><span data-stu-id="ffd28-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="ffd28-118">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="ffd28-118">Downloading the Sample</span></span>

<span data-ttu-id="ffd28-119">Cet exemple est disponible aux emplacements suivants.</span><span class="sxs-lookup"><span data-stu-id="ffd28-119">This sample is available in the following locations.</span></span>



| <span data-ttu-id="ffd28-120">Emplacement</span><span class="sxs-lookup"><span data-stu-id="ffd28-120">Location</span></span>      | <span data-ttu-id="ffd28-121">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="ffd28-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="ffd28-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="ffd28-122">GitHub</span></span>  | [<span data-ttu-id="ffd28-123">OpenSearch, exemple</span><span class="sxs-lookup"><span data-stu-id="ffd28-123">OpenSearch sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/OpenSearch)      |



 

 

> [!Note]  
> <span data-ttu-id="ffd28-124">Pour toutes les versions de Windows, y compris Windows 7, nous vous recommandons de télécharger les exemples directement à partir de GitHub pour obtenir la version la plus récente.</span><span class="sxs-lookup"><span data-stu-id="ffd28-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

 

## <a name="building-the-sample"></a><span data-ttu-id="ffd28-125">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="ffd28-125">Building the Sample</span></span>

<span data-ttu-id="ffd28-126">Pour générer l’exemple à partir de l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="ffd28-126">To build the sample from the Command Prompt:</span></span>

1.  <span data-ttu-id="ffd28-127">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **AdventureSearch** .</span><span class="sxs-lookup"><span data-stu-id="ffd28-127">Open the Command Prompt window and navigate to the **AdventureSearch** project directory.</span></span> 
2.  <span data-ttu-id="ffd28-128">Entrez `msbuild AdventureSearch.sln`.</span><span class="sxs-lookup"><span data-stu-id="ffd28-128">Enter `msbuild AdventureSearch.sln`.</span></span>

<span data-ttu-id="ffd28-129">Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :</span><span class="sxs-lookup"><span data-stu-id="ffd28-129">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="ffd28-130">Ouvrez l’Explorateur Windows et accédez au répertoire du projet **AdventureSearch** .</span><span class="sxs-lookup"><span data-stu-id="ffd28-130">Open Windows Explorer and navigate to the **AdventureSearch** project directory.</span></span>
2.  <span data-ttu-id="ffd28-131">Double-cliquez sur l’icône du fichier AdventureSearch. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="ffd28-131">Double-click the icon for the AdventureSearch.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="ffd28-132">L’extension de nom de fichier. sln n’est pas affichée sous paramètres de dossier par défaut.</span><span class="sxs-lookup"><span data-stu-id="ffd28-132">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="ffd28-133">Dans ce cas, il peut être identifié par son icône unique ou par sa description de type, « Microsoft Visual Studio solution ».</span><span class="sxs-lookup"><span data-stu-id="ffd28-133">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="ffd28-134">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="ffd28-134">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="ffd28-135">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="ffd28-135">Running the Sample</span></span>

1.  <span data-ttu-id="ffd28-136">Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de la fenêtre d’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="ffd28-136">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2.  <span data-ttu-id="ffd28-137">À l’invite de commandes, entrez `AdventureSearch.exe` , ou à partir de l’Explorateur Windows, double-cliquez sur l’icône de AdventureSearch.exe.</span><span class="sxs-lookup"><span data-stu-id="ffd28-137">At the command prompt, enter `AdventureSearch.exe`, or from Windows Explorer, double-click the icon for AdventureSearch.exe.</span></span>
3.  <span data-ttu-id="ffd28-138">À l’invite de commandes, entrez `GetOSDX.exe` , ou à partir de l’Explorateur Windows, double-cliquez sur l’icône de GetOSDX.exe.</span><span class="sxs-lookup"><span data-stu-id="ffd28-138">At the command prompt, enter `GetOSDX.exe`, or from Windows Explorer, double-click the icon for GetOSDX.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ffd28-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ffd28-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ffd28-140">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="ffd28-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ffd28-141">Vue d’ensemble du schéma de description du connecteur de recherche</span><span class="sxs-lookup"><span data-stu-id="ffd28-141">Overview of the Search Connector Description Schema</span></span>](search-sconn-desc-schema-entry.md)
</dt> <dt>

<span data-ttu-id="ffd28-142">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="ffd28-142">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ffd28-143">Recherche fédérée dans Windows</span><span class="sxs-lookup"><span data-stu-id="ffd28-143">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="ffd28-144">Rechercher des exemples de code</span><span class="sxs-lookup"><span data-stu-id="ffd28-144">Search Code Samples</span></span>](-search-samples-ovw.md)
</dt> <dt>

<span data-ttu-id="ffd28-145">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="ffd28-145">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="ffd28-146">Schéma de description de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ffd28-146">Library Description Schema</span></span>](../shell/library-schema-entry.md)
</dt> </dl>

 

 

---
description: L’exemple de code WSSQL montre comment communiquer entre Microsoft OLE DB et Windows Search via langage SQL (SQL).
ms.assetid: 28663608-66b3-4404-9426-5a4b5f52a408
title: WSSQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac8f76b995d21a562f843344d1722cecec433af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862161"
---
# <a name="wssql"></a><span data-ttu-id="2c127-103">WSSQL</span><span class="sxs-lookup"><span data-stu-id="2c127-103">WSSQL</span></span>

<span data-ttu-id="2c127-104">L’exemple de code WSSQL montre comment communiquer entre Microsoft OLE DB et Windows Search via langage SQL (SQL).</span><span class="sxs-lookup"><span data-stu-id="2c127-104">The WSSQL code sample demonstrates how to communicate between Microsoft OLE DB and Windows Search through Structured Query Language (SQL).</span></span>

<span data-ttu-id="2c127-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="2c127-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="2c127-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c127-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="2c127-107">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="2c127-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="2c127-108">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="2c127-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="2c127-109">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="2c127-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="2c127-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2c127-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="2c127-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c127-111">Requirements</span></span>

| <span data-ttu-id="2c127-112">Produit</span><span class="sxs-lookup"><span data-stu-id="2c127-112">Product</span></span>     | <span data-ttu-id="2c127-113">Version du produit</span><span class="sxs-lookup"><span data-stu-id="2c127-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="2c127-114">Windows</span><span class="sxs-lookup"><span data-stu-id="2c127-114">Windows</span></span>     | <span data-ttu-id="2c127-115">Windows 7, 8.1 ou 10</span><span class="sxs-lookup"><span data-stu-id="2c127-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="2c127-116">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="2c127-116">Windows SDK</span></span> | <span data-ttu-id="2c127-117">7,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="2c127-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="2c127-118">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="2c127-118">Downloading the Sample</span></span>

<span data-ttu-id="2c127-119">Cet exemple est disponible à l’emplacement suivant.</span><span class="sxs-lookup"><span data-stu-id="2c127-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="2c127-120">Emplacement</span><span class="sxs-lookup"><span data-stu-id="2c127-120">Location</span></span>      | <span data-ttu-id="2c127-121">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="2c127-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="2c127-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="2c127-122">GitHub</span></span>        | [<span data-ttu-id="2c127-123">Exemple WSSQL</span><span class="sxs-lookup"><span data-stu-id="2c127-123">WSSQL sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSSQL)           |

> [!NOTE]  
> <span data-ttu-id="2c127-124">Pour toutes les versions de Windows, y compris Windows 7, nous vous recommandons de télécharger les exemples directement à partir de GitHub pour obtenir la version la plus récente.</span><span class="sxs-lookup"><span data-stu-id="2c127-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="2c127-125">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="2c127-125">Building the Sample</span></span>

1. <span data-ttu-id="2c127-126">Ouvrez l’Explorateur Windows et accédez au répertoire du projet **WSSQL** .</span><span class="sxs-lookup"><span data-stu-id="2c127-126">Open Windows Explorer and navigate to the **WSSQL** project directory.</span></span>
2. <span data-ttu-id="2c127-127">Double-cliquez sur l’icône du fichier WSSQL. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="2c127-127">Double-click the icon for the WSSQL.sln file to open the project in Visual Studio.</span></span>
    > [!NOTE]  
    > <span data-ttu-id="2c127-128">Le fichier sln a été créé sous une version antérieure de Visual Studio. par conséquent, la mise à niveau est requise si vous exécutez Visual Studio 2012 ou une version plus récente.</span><span class="sxs-lookup"><span data-stu-id="2c127-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="2c127-129">Cela n’aura pas d’impact sur le comportement de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="2c127-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="2c127-130">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="2c127-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="2c127-131">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="2c127-131">Running the Sample</span></span>

1. <span data-ttu-id="2c127-132">Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de la fenêtre d’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="2c127-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="2c127-133">À l’invite de commandes, entrez `WSSQL.exe` , ou à partir de l’Explorateur Windows, double-cliquez sur l’icône de WSSQL.exe.</span><span class="sxs-lookup"><span data-stu-id="2c127-133">At the command prompt, enter `WSSQL.exe`, or from Windows Explorer, double-click the icon for WSSQL.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c127-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2c127-134">Related topics</span></span>

### <a name="conceptual"></a><span data-ttu-id="2c127-135">Conceptuel</span><span class="sxs-lookup"><span data-stu-id="2c127-135">Conceptual</span></span>

[<span data-ttu-id="2c127-136">Utilisation de la syntaxe SQL de Windows Search</span><span class="sxs-lookup"><span data-stu-id="2c127-136">Using Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)

[<span data-ttu-id="2c127-137">Informations générales sur le langage de requête</span><span class="sxs-lookup"><span data-stu-id="2c127-137">General Query Language Information</span></span>](-search-sql-generalqueryinfo.md)

[<span data-ttu-id="2c127-138">Vue d’ensemble de la programmation OLE DB</span><span class="sxs-lookup"><span data-stu-id="2c127-138">OLE DB Programming Overview</span></span>](/cpp/data/oledb/ole-db-programming-overview)

### <a name="other-samples"></a><span data-ttu-id="2c127-139">Autres exemples</span><span class="sxs-lookup"><span data-stu-id="2c127-139">Other Samples</span></span>

[<span data-ttu-id="2c127-140">Rechercher des exemples de code</span><span class="sxs-lookup"><span data-stu-id="2c127-140">Search Code Samples</span></span>](-search-samples-ovw.md)

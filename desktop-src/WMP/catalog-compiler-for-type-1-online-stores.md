---
title: Compilateur de catalogue pour les magasins en ligne de type 1
description: Compilateur de catalogue pour les magasins en ligne de type 1
ms.assetid: 49c03d3b-3381-4663-83c8-5bc8fa70f7c3
keywords:
- Magasins en ligne du lecteur Windows Media, compilateur de catalogue
- magasins en ligne, compilateur de catalogue
- magasins en ligne de type 1, compilateur de catalogue
- Windows Media Player Online stores, catcomp.exe
- magasins en ligne, catcomp.exe
- tapez 1 magasins en ligne, catcomp.exe
- compilateur de catalogue
- catcomp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4c54ffd054c5e72b04ddd32eef12c7fe6b6cc89
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106509428"
---
# <a name="catalog-compiler-for-type-1-online-stores"></a><span data-ttu-id="d8cff-111">Compilateur de catalogue pour les magasins en ligne de type 1</span><span class="sxs-lookup"><span data-stu-id="d8cff-111">Catalog Compiler for Type 1 Online Stores</span></span>

<span data-ttu-id="d8cff-112">Le compilateur de catalogue (catcomp.exe) est un outil de ligne de commande utilisé par les magasins de type 1 en ligne pour compiler l’ensemble de fichiers TSV (valeurs séparées par des tabulations) contenant les données de catalogue du magasin en ligne dans un catalogue compressé qui peut être téléchargé par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d8cff-112">The catalog compiler (catcomp.exe) is a command-line tool used by Type 1 online stores to compile the set of tab-separated-value (TSV) files containing the online store's catalog data into a compressed catalog that can be downloaded by Windows Media Player.</span></span> <span data-ttu-id="d8cff-113">Le compilateur de catalogue compile également les fichiers de mise à jour du catalogue contenant uniquement les informations du catalogue qui ont été modifiées depuis la dernière mise à jour du catalogue.</span><span class="sxs-lookup"><span data-stu-id="d8cff-113">The catalog compiler also compiles catalog update files containing only the catalog information that has changed since the last catalog update.</span></span>

<span data-ttu-id="d8cff-114">Les fichiers de catalogue compressé ou les fichiers de mise à jour de catalogue doivent être fournis au lecteur Windows Media pour téléchargement dans l’implémentation du plug-in de magasin en ligne de [IWMPContentPartner :: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span><span class="sxs-lookup"><span data-stu-id="d8cff-114">The compressed catalog files or catalog update files should be provided to Windows Media Player for download in the online store plug-in's implementation of [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span></span>

<span data-ttu-id="d8cff-115">Tâches courantes</span><span class="sxs-lookup"><span data-stu-id="d8cff-115">Common Tasks</span></span>

-   [<span data-ttu-id="d8cff-116">Compilation d’un catalogue complet à partir de fichiers TSV</span><span class="sxs-lookup"><span data-stu-id="d8cff-116">Compiling a Full Catalog from TSV Files</span></span>](compiling-a-full-catalog-from-tsv-files.md)
-   [<span data-ttu-id="d8cff-117">Compilation d’une mise à jour de catalogue à partir de catalogues complets</span><span class="sxs-lookup"><span data-stu-id="d8cff-117">Compiling a Catalog Update from Full Catalogs</span></span>](compiling-a-catalog-update-from-full-catalogs.md)

<span data-ttu-id="d8cff-118">Tâches de diagnostic</span><span class="sxs-lookup"><span data-stu-id="d8cff-118">Diagnostic Tasks</span></span>

-   [<span data-ttu-id="d8cff-119">Affichage de l’aide</span><span class="sxs-lookup"><span data-stu-id="d8cff-119">Displaying Help</span></span>](displaying-help.md)
-   [<span data-ttu-id="d8cff-120">Récupération des informations de catalogue</span><span class="sxs-lookup"><span data-stu-id="d8cff-120">Retrieving Catalog Information</span></span>](retrieving-catalog-information.md)
-   [<span data-ttu-id="d8cff-121">Application d’une mise à jour à un catalogue</span><span class="sxs-lookup"><span data-stu-id="d8cff-121">Applying an Update To a Catalog</span></span>](applying-an-update-to-a-catalog.md)

 

 





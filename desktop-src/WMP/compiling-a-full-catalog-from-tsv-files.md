---
title: Compilation d’un catalogue complet à partir de fichiers TSV
description: Compilation d’un catalogue complet à partir de fichiers TSV
ms.assetid: fba80b32-dc78-4c4a-a351-e8786f9a7131
keywords:
- Windows Media Player Online stores, compilation des catalogues
- magasins en ligne, compilation de catalogues
- types 1 magasins en ligne, compilation des catalogues
- Windows Media Player Online stores, fichiers TSV
- magasins en ligne, fichiers TSV
- types 1 magasins en ligne, fichiers TSV
- Windows Media Player Online stores, catcomp.exe
- magasins en ligne, catcomp.exe
- tapez 1 magasins en ligne, catcomp.exe
- catcomp.exe
- compilation des catalogues
- fichiers de valeurs séparées par des tabulations (TSV)
- Fichiers TSV (valeurs séparées par des tabulations)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b68af019a5e2302f52f615d5a1dba2180e27cfe5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106517994"
---
# <a name="compiling-a-full-catalog-from-tsv-files"></a><span data-ttu-id="975a6-116">Compilation d’un catalogue complet à partir de fichiers TSV</span><span class="sxs-lookup"><span data-stu-id="975a6-116">Compiling a Full Catalog from TSV Files</span></span>

<span data-ttu-id="975a6-117">De nouveaux catalogues sont créés à partir d’un ensemble de fichiers TSV (valeurs séparées par des tabulations).</span><span class="sxs-lookup"><span data-stu-id="975a6-117">New catalogs are created from a set of tab-separated-value (TSV) files.</span></span> <span data-ttu-id="975a6-118">Les fichiers doivent être au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="975a6-118">The files must be in Unicode format.</span></span> <span data-ttu-id="975a6-119">Placez les fichiers TSV requis listés ci-dessous dans un dossier (l’argument de chemin d’entrée pour catcomp.exe) et appelez catcomp.exe à l’aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="975a6-119">Place the required TSV files listed below into a folder (the input path argument to catcomp.exe), and call catcomp.exe using the following syntax:</span></span>


```C++
catcomp <input path> [version number] [locale ID] [debug]
```



<span data-ttu-id="975a6-120">Si aucun numéro de version n’est fourni, le numéro de version est défini sur 0.</span><span class="sxs-lookup"><span data-stu-id="975a6-120">If a version number is not provided, the version number will be set to 0.</span></span> <span data-ttu-id="975a6-121">Si aucun ID de paramètres régionaux n’est fourni, les paramètres régionaux système sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="975a6-121">If no locale ID is provided, the system locale is used.</span></span> <span data-ttu-id="975a6-122">Si un seul argument numérique facultatif est fourni, il est supposé être le numéro de version.</span><span class="sxs-lookup"><span data-stu-id="975a6-122">If only one numeric optional argument is provided, it is assumed to be the version number.</span></span> <span data-ttu-id="975a6-123">Si debug est spécifié, la sortie à l’écran fournira des informations de diagnostic plus détaillées.</span><span class="sxs-lookup"><span data-stu-id="975a6-123">If debug is specified, the output to the screen will provide more detailed diagnostic information.</span></span>

<span data-ttu-id="975a6-124">Par exemple, le code suivant compile un catalogue à partir des fichiers de C : \\ CatalogData \\ 210 et donne au catalogue le numéro de version 210 :</span><span class="sxs-lookup"><span data-stu-id="975a6-124">For example, the following will compile a catalog from the files in C:\\CatalogData\\210 and give the catalog a version number of 210:</span></span>


```C++
catcomp C:\CatalogData\210 210
```



<span data-ttu-id="975a6-125">Pour afficher des messages d’erreur plus détaillés, l’argument de débogage facultatif peut être ajouté, comme suit :</span><span class="sxs-lookup"><span data-stu-id="975a6-125">To display more detailed error messages, the optional debug argument can be added, as follows:</span></span>


```C++
catcomp C:\CatalogData\210 210 debug
```



## <a name="required-tsv-files"></a><span data-ttu-id="975a6-126">Fichiers TSV requis</span><span class="sxs-lookup"><span data-stu-id="975a6-126">Required TSV Files</span></span>

<span data-ttu-id="975a6-127">Chacun des fichiers suivants doit être présent, mais un fichier vide peut être utilisé s’il n’y a pas de données pour un fichier.</span><span class="sxs-lookup"><span data-stu-id="975a6-127">Each of the following files must be present, but an empty file can be used if there is no data for a file.</span></span> <span data-ttu-id="975a6-128">Par exemple, si votre catalogue ne contient pas de canaux radio, radio.csv peut être vide.</span><span class="sxs-lookup"><span data-stu-id="975a6-128">For instance, if your catalog contains no radio channels, radio.csv can be empty.</span></span> <span data-ttu-id="975a6-129">Les fichiers doivent être nommés exactement comme indiqué.</span><span class="sxs-lookup"><span data-stu-id="975a6-129">The files must be named exactly as listed.</span></span>

[<span data-ttu-id="975a6-130">track.csv</span><span class="sxs-lookup"><span data-stu-id="975a6-130">track.csv</span></span>](track-csv.md)

[<span data-ttu-id="975a6-131">album.csv</span><span class="sxs-lookup"><span data-stu-id="975a6-131">album.csv</span></span>](album-csv.md)

[<span data-ttu-id="975a6-132">artist.csv</span><span class="sxs-lookup"><span data-stu-id="975a6-132">artist.csv</span></span>](artist-csv.md)

[<span data-ttu-id="975a6-133">genre.csv</span><span class="sxs-lookup"><span data-stu-id="975a6-133">genre.csv</span></span>](genre-csv.md)

[<span data-ttu-id="975a6-134">subgenre.csv</span><span class="sxs-lookup"><span data-stu-id="975a6-134">subgenre.csv</span></span>](subgenre-csv.md)

[<span data-ttu-id="975a6-135">list.csv</span><span class="sxs-lookup"><span data-stu-id="975a6-135">list.csv</span></span>](list-csv.md)

[<span data-ttu-id="975a6-136">listitem.csv</span><span class="sxs-lookup"><span data-stu-id="975a6-136">listitem.csv</span></span>](listitem-csv.md)

[<span data-ttu-id="975a6-137">radio.csv</span><span class="sxs-lookup"><span data-stu-id="975a6-137">radio.csv</span></span>](radio-csv.md)

> [!Note]  
> <span data-ttu-id="975a6-138">Bien que les noms de fichiers doivent avoir des extensions. csv, les fichiers ne sont pas au format CSV (valeurs séparées par des virgules).</span><span class="sxs-lookup"><span data-stu-id="975a6-138">Although the file names must have .csv extensions, the files are not in Comma Separated Values (CSV) format.</span></span> <span data-ttu-id="975a6-139">Les fichiers doivent être au format de valeurs séparées par des tabulations (TSV).</span><span class="sxs-lookup"><span data-stu-id="975a6-139">The files must be in Tab Separated Values (TSV) format.</span></span>

 

<span data-ttu-id="975a6-140">Si la compilation réussit, catcomp.exe crée trois fichiers de sortie.</span><span class="sxs-lookup"><span data-stu-id="975a6-140">If compilation is successful, catcomp.exe creates three output files.</span></span>



| <span data-ttu-id="975a6-141">Nom de fichier</span><span class="sxs-lookup"><span data-stu-id="975a6-141">File name</span></span>                   | <span data-ttu-id="975a6-142">Description</span><span class="sxs-lookup"><span data-stu-id="975a6-142">Description</span></span>                                                                                                                                                                         |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="975a6-143">Catalog. WMDB</span><span class="sxs-lookup"><span data-stu-id="975a6-143">catalog.wmdb</span></span>                | <span data-ttu-id="975a6-144">Catalogue compilé non compressé.</span><span class="sxs-lookup"><span data-stu-id="975a6-144">Uncompressed compiled catalog.</span></span>                                                                                                                                                      |
| <span data-ttu-id="975a6-145">Catalog. WMDB. LZ</span><span class="sxs-lookup"><span data-stu-id="975a6-145">catalog.wmdb.lz</span></span>             | <span data-ttu-id="975a6-146">Catalogue au format compressé.</span><span class="sxs-lookup"><span data-stu-id="975a6-146">Catalog in compressed format.</span></span> <span data-ttu-id="975a6-147">Votre plug-in peut fournir l’emplacement de ce fichier au lecteur Windows Media dans [IWMPContentPartner :: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span><span class="sxs-lookup"><span data-stu-id="975a6-147">Your plug-in can give the location of this file to Windows Media Player in [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span></span> |
| <span data-ttu-id="975a6-148">\_words.txt unique \_ compilé</span><span class="sxs-lookup"><span data-stu-id="975a6-148">compiled\_unique\_words.txt</span></span> | <span data-ttu-id="975a6-149">Fichier de sortie intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="975a6-149">An intermediate output file.</span></span> <span data-ttu-id="975a6-150">Non utilisé par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="975a6-150">Not used by Windows Media Player.</span></span>                                                                                                                      |



 

 

 





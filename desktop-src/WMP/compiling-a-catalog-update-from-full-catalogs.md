---
title: Compilation d’une mise à jour de catalogue à partir de catalogues complets
description: Compilation d’une mise à jour de catalogue à partir de catalogues complets
ms.assetid: 046c0a01-0ad7-41b6-bad5-dcab953a3980
keywords:
- Windows Media Player Online stores, compilation des catalogues
- magasins en ligne, compilation de catalogues
- types 1 magasins en ligne, compilation des catalogues
- Windows Media Player Online stores, mises à jour de catalogue
- magasins en ligne, mises à jour de catalogue
- types 1 magasins en ligne, mises à jour de catalogue
- Windows Media Player Online stores, catalogues complets
- magasins en ligne, catalogues complets
- tapez 1 magasins en ligne, catalogues complets
- compilation des catalogues
- mises à jour du catalogue
- catalogues complets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abaa6d1bc0d3dbc4fefaffe1498be03259716a5e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314215"
---
# <a name="compiling-a-catalog-update-from-full-catalogs"></a><span data-ttu-id="64588-115">Compilation d’une mise à jour de catalogue à partir de catalogues complets</span><span class="sxs-lookup"><span data-stu-id="64588-115">Compiling a Catalog Update from Full Catalogs</span></span>

<span data-ttu-id="64588-116">Une mise à jour du catalogue contenant les modifications entre deux versions d’un catalogue compilé peut être créée à l’aide de la syntaxe ci-dessous, où *chemin1* est le répertoire contenant le premier catalogue, *chemin2* le répertoire contenant le deuxième catalogue et le débogage peut être éventuellement inclus pour afficher des informations détaillées sur l’erreur à l’écran.</span><span class="sxs-lookup"><span data-stu-id="64588-116">A catalog update containing the changes between two versions of a compiled catalog can be created by using the syntax below, where *path1* is the directory containing the first catalog, *path2* is the directory containing the second catalog, and debug can be optionally included to display detailed error information on the screen.</span></span> <span data-ttu-id="64588-117">Les fichiers de catalogue doivent être dans un format non compressé : le nom de fichier du catalogue compilé est catalog. WMDB, plutôt que Catalog. WMDB. LZ.</span><span class="sxs-lookup"><span data-stu-id="64588-117">The catalog files must be in uncompressed form—the file name of the compiled catalog would be catalog.wmdb, rather than catalog.wmdb.lz.</span></span>


```C++
catcomp diff <path1> <path2> [debug]
```



<span data-ttu-id="64588-118">Par exemple, si le répertoire C : \\ Catalog210 \\ contient la version 210 d’un catalogue compilé complet et que le répertoire c : \\ Catalog211 \\ contient la version 211, la commande suivante crée un fichier de différences qui contient les modifications entre les deux versions :</span><span class="sxs-lookup"><span data-stu-id="64588-118">For example, if the C:\\Catalog210\\ directory contains version 210 of a full compiled catalog and C:\\Catalog211\\ contains version 211, the following command creates a difference file that contains the changes between the two versions:</span></span>


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\
```



<span data-ttu-id="64588-119">Pour afficher des informations détaillées sur l’erreur, vous pouvez ajouter le paramètre de débogage facultatif comme suit :</span><span class="sxs-lookup"><span data-stu-id="64588-119">To display detailed error information, you can add the optional debug parameter as follows:</span></span>


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\ debug
```



<span data-ttu-id="64588-120">Si la compilation réussit, catcomp.exe crée les fichiers de sortie listés ci-dessous et les enregistre dans le répertoire qui contient le premier catalogue.</span><span class="sxs-lookup"><span data-stu-id="64588-120">If compilation is successful, catcomp.exe creates the output files listed below and saves them in the directory that contains the first catalog.</span></span>



| <span data-ttu-id="64588-121">Nom de fichier</span><span class="sxs-lookup"><span data-stu-id="64588-121">File name</span></span>             | <span data-ttu-id="64588-122">Description</span><span class="sxs-lookup"><span data-stu-id="64588-122">Description</span></span>                                                                                                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64588-123">Catalog. diff</span><span class="sxs-lookup"><span data-stu-id="64588-123">catalog.diff</span></span>          | <span data-ttu-id="64588-124">Fichier de différences compilées non compressées.</span><span class="sxs-lookup"><span data-stu-id="64588-124">Uncompressed compiled difference file.</span></span>                                                                                                                                                           |
| <span data-ttu-id="64588-125">Catalog. diff. LZ</span><span class="sxs-lookup"><span data-stu-id="64588-125">catalog.diff.lz</span></span>       | <span data-ttu-id="64588-126">Version compressée du fichier de mise à jour du catalogue.</span><span class="sxs-lookup"><span data-stu-id="64588-126">Compressed version of catalog update file.</span></span> <span data-ttu-id="64588-127">Votre plug-in peut fournir l’emplacement de ce fichier au lecteur Windows Media dans [IWMPContentPartner :: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span><span class="sxs-lookup"><span data-stu-id="64588-127">Your plug-in can give the location of this file to Windows Media Player in [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span></span> |
| <span data-ttu-id="64588-128">Catalog. WMDB. Delta</span><span class="sxs-lookup"><span data-stu-id="64588-128">catalog.wmdb.delta</span></span>    | <span data-ttu-id="64588-129">Fichier de sortie intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="64588-129">Intermediate output file.</span></span> <span data-ttu-id="64588-130">Non utilisé par le lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="64588-130">Not used by Windows Media Player</span></span>                                                                                                                                       |
| <span data-ttu-id="64588-131">Catalog. WMDB. modified</span><span class="sxs-lookup"><span data-stu-id="64588-131">catalog.wmdb.modified</span></span> | <span data-ttu-id="64588-132">Fichier de sortie intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="64588-132">Intermediate output file.</span></span> <span data-ttu-id="64588-133">Non utilisé par le lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="64588-133">Not used by Windows Media Player</span></span>                                                                                                                                       |



 

 

 





---
description: Lorsqu’une table qui contient uniquement des caractères ASCII est exportée vers un fichier d’archive de texte, le fichier. IDT respecte le format de fichier d’archive de base.
ms.assetid: 105d2b85-c6e1-4719-83b4-1693c14ef4f4
title: Données ASCII dans les fichiers d’archive de texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d43deeb7918b75a71770ab9d09535972f6e8bb4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864465"
---
# <a name="ascii-data-in-text-archive-files"></a><span data-ttu-id="5f554-103">Données ASCII dans les fichiers d’archive de texte</span><span class="sxs-lookup"><span data-stu-id="5f554-103">ASCII Data in Text Archive Files</span></span>

<span data-ttu-id="5f554-104">Lorsqu’une table qui contient uniquement des caractères ASCII est exportée vers un [fichier d’archive de texte](text-archive-files.md), le fichier. IDT respecte le format de fichier d' [Archive](archive-file-format.md)de base.</span><span class="sxs-lookup"><span data-stu-id="5f554-104">When a table that contains only ASCII characters is exported to a [text archive file](text-archive-files.md), the .idt file adheres to the basic [archive file format](archive-file-format.md).</span></span> <span data-ttu-id="5f554-105">Si la table contient des informations non-ASCII, le format du fichier d’archive est étendu pour inclure les informations de la page de codes.</span><span class="sxs-lookup"><span data-stu-id="5f554-105">If the table contains non-ASCII information, the format of the archive file is extended to include code page information.</span></span>

## <a name="text-archive-files-that-contain-only-ascii-characters"></a><span data-ttu-id="5f554-106">Fichiers d’archive de texte qui contiennent uniquement des caractères ASCII</span><span class="sxs-lookup"><span data-stu-id="5f554-106">Text archive files that contain only ASCII characters</span></span>

<span data-ttu-id="5f554-107">Lorsqu’une table qui contient uniquement des caractères ASCII est exportée vers un fichier d’archive, le fichier. IDT est au [format de fichier d’archive](archive-file-format.md)de base.</span><span class="sxs-lookup"><span data-stu-id="5f554-107">When a table that contains only ASCII characters is exported to an archive file, the .idt file is in the basic [archive file format](archive-file-format.md).</span></span> <span data-ttu-id="5f554-108">Chaque flux de la table est exporté sous la forme d’un fichier avec une extension de nom de fichier. IBD.</span><span class="sxs-lookup"><span data-stu-id="5f554-108">Each stream in the table is exported as a file with an .ibd file name extension.</span></span> <span data-ttu-id="5f554-109">Les fichiers. IBD sont stockés dans un dossier portant le même nom que la table.</span><span class="sxs-lookup"><span data-stu-id="5f554-109">The .ibd files are stored in a folder with the same name as the table.</span></span> <span data-ttu-id="5f554-110">Par exemple, considérez l’exportation de la table [binaire](binary-table.md) suivante.</span><span class="sxs-lookup"><span data-stu-id="5f554-110">For example, consider the export of the following [Binary](binary-table.md) table.</span></span>



| <span data-ttu-id="5f554-111">Nom</span><span class="sxs-lookup"><span data-stu-id="5f554-111">Name</span></span>  | <span data-ttu-id="5f554-112">Données</span><span class="sxs-lookup"><span data-stu-id="5f554-112">Data</span></span>      |
|-------|-----------|
| <span data-ttu-id="5f554-113">Livres</span><span class="sxs-lookup"><span data-stu-id="5f554-113">Books</span></span> | <span data-ttu-id="5f554-114">Books. IBD</span><span class="sxs-lookup"><span data-stu-id="5f554-114">Books.ibd</span></span> |
| <span data-ttu-id="5f554-115">Voitures</span><span class="sxs-lookup"><span data-stu-id="5f554-115">Cars</span></span>  | <span data-ttu-id="5f554-116">Cars. IBD</span><span class="sxs-lookup"><span data-stu-id="5f554-116">Cars.ibd</span></span>  |



 

<span data-ttu-id="5f554-117">La structure de répertoire après l’exportation de cette table est la suivante.</span><span class="sxs-lookup"><span data-stu-id="5f554-117">The directory structure after exporting this table is as follows.</span></span> <span data-ttu-id="5f554-118">Les informations de la table de base de données sont exportées vers Binary. IDT.</span><span class="sxs-lookup"><span data-stu-id="5f554-118">The information in the database table is exported to Binary.idt.</span></span> <span data-ttu-id="5f554-119">Les deux flux de données binaires sont exportés vers Book. IBD et cars. IBD enregistrés dans le dossier nommé Binary.</span><span class="sxs-lookup"><span data-stu-id="5f554-119">The two streams of binary data are exported to Book.ibd and Cars.ibd saved in the folder named Binary.</span></span>

``` syntax
Binary.idt
[Binary]
    Books.ibd
    Cars.ibd
```

<span data-ttu-id="5f554-120">Le fichier d’archive binaire. IDT est au [format de fichier d’archive](archive-file-format.md) de base et se présente comme suit.</span><span class="sxs-lookup"><span data-stu-id="5f554-120">The Binary.idt archive file is in the basic [archive file format](archive-file-format.md) and would look as follows.</span></span>

``` syntax
Name Data
s72 v0
Binary  Name
Books   Books.ibd
Cars    Cars.ibd
```

## <a name="text-archive-files-that-contain-non--ascii-characters"></a><span data-ttu-id="5f554-121">Fichiers d’archive de texte contenant des caractères non-ASCII</span><span class="sxs-lookup"><span data-stu-id="5f554-121">Text archive files that contain non- ASCII characters</span></span>

<span data-ttu-id="5f554-122">Si le fichier contient des données non-ASCII, le [format de fichier d’archive](archive-file-format.md) de base du fichier. IDT est étendu pour inclure les informations de la page de codes.</span><span class="sxs-lookup"><span data-stu-id="5f554-122">If the file contains non-ASCII data, the basic [archive file format](archive-file-format.md) of the .idt file is extended to include code page information.</span></span> <span data-ttu-id="5f554-123">La troisième ligne de la table. IDT est la page de codes numérique suivie du nom de la table et des noms de colonne de clé primaire séparés par des tabulations.</span><span class="sxs-lookup"><span data-stu-id="5f554-123">The third row in the .idt table is the numeric code page followed by the table name and primary key column names separated by tabs.</span></span>

> [!Note]  
> <span data-ttu-id="5f554-124">Un fichier. IDT qui contient des informations non-ASCII doit être enregistré au format ASCII.</span><span class="sxs-lookup"><span data-stu-id="5f554-124">An .idt file that contains non-ASCII information should be saved in the ASCII format.</span></span> <span data-ttu-id="5f554-125">Par exemple, un fichier d’archive de texte peut contenir les noms de colonne et de table encodés au format UTF-8, mais le fichier d’archive lui-même doit être au format ASCII.</span><span class="sxs-lookup"><span data-stu-id="5f554-125">For example, a text archive file can contain the column and table names encoded as UTF-8, but the archive file itself should be ASCII.</span></span>

 

<span data-ttu-id="5f554-126">La table ActionText suivante localisée en français contient des informations non-ASCII.</span><span class="sxs-lookup"><span data-stu-id="5f554-126">The following ActionText table localized into French would contain non-ASCII information.</span></span> <span data-ttu-id="5f554-127">La page de codes numérique utilisée pour les chaînes françaises est 1252.</span><span class="sxs-lookup"><span data-stu-id="5f554-127">The numeric code page used for French strings is 1252.</span></span>



| <span data-ttu-id="5f554-128">Action</span><span class="sxs-lookup"><span data-stu-id="5f554-128">Action</span></span>    | <span data-ttu-id="5f554-129">Description</span><span class="sxs-lookup"><span data-stu-id="5f554-129">Description</span></span>                                  | <span data-ttu-id="5f554-130">Modèle</span><span class="sxs-lookup"><span data-stu-id="5f554-130">Template</span></span> |
|-----------|----------------------------------------------|----------|
| <span data-ttu-id="5f554-131">PUBLIER</span><span class="sxs-lookup"><span data-stu-id="5f554-131">ADVERTISE</span></span> | <span data-ttu-id="5f554-132">Publication d’infos sur l’application</span><span class="sxs-lookup"><span data-stu-id="5f554-132">Publication d'informations sur l'application</span></span> |          |



 

<span data-ttu-id="5f554-133">Le fichier d’archive exporté, ActionText. IDT, est le suivant.</span><span class="sxs-lookup"><span data-stu-id="5f554-133">The exported archive file, ActionText.idt, would be as follows.</span></span>

``` syntax
Action   Description Template
s72 L0  L0
1252    ActionText  Action
Advertise   Publication d'informations sur l'application
```

> [!Note]  
> <span data-ttu-id="5f554-134">Si un fichier d’archive de texte contient des données non-ASCII, le fichier d’archive inclut des informations sur la page de codes.</span><span class="sxs-lookup"><span data-stu-id="5f554-134">If a text archive file contains non-ASCII data, the archive file includes code page information.</span></span> <span data-ttu-id="5f554-135">Les fichiers d’archive avec les informations de page de codes peuvent être réimportés uniquement dans une base de données de la page de codes exacte ou dans une base de données indépendante de la langue.</span><span class="sxs-lookup"><span data-stu-id="5f554-135">Archive files with code page information can only be imported back into a database of that exact code page or into a language neutral database.</span></span> <span data-ttu-id="5f554-136">Dans le cas d’une base de données indépendante de la langue, la page de codes est définie sur la page de codes du fichier d’archive.</span><span class="sxs-lookup"><span data-stu-id="5f554-136">In the case of a language neutral database, the code page is set to the code page of the archive file.</span></span> <span data-ttu-id="5f554-137">Pour plus d’informations sur la façon dont Windows Installer gère les pages de codes, consultez la section [gestion des pages de codes (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="5f554-137">For more information about how Windows Installer handles code pages see the section [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span>

 

 

 




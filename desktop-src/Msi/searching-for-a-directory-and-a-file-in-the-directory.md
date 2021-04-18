---
description: Pendant une installation Windows Installer, le programme d’installation peut rechercher un répertoire et un fichier dans ce répertoire.
ms.assetid: ddf624f9-6f85-4ef6-8dfc-8635a25915d0
title: Recherche d’un répertoire et d’un fichier dans le répertoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b4821a53ef0c3f063e943f1f5821b043791dd44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519951"
---
# <a name="searching-for-a-directory-and-a-file-in-the-directory"></a><span data-ttu-id="aacf7-103">Recherche d’un répertoire et d’un fichier dans le répertoire</span><span class="sxs-lookup"><span data-stu-id="aacf7-103">Searching for a Directory and a File in the Directory</span></span>

<span data-ttu-id="aacf7-104">**Pour rechercher un répertoire, puis un fichier dans ce répertoire**</span><span class="sxs-lookup"><span data-stu-id="aacf7-104">**To search for a directory and then a file in that directory**</span></span>

1.  <span data-ttu-id="aacf7-105">Commencez par Rechercher le répertoire.</span><span class="sxs-lookup"><span data-stu-id="aacf7-105">First search for the directory.</span></span>

    <span data-ttu-id="aacf7-106">AppDir doit être défini comme signature valide du répertoire.</span><span class="sxs-lookup"><span data-stu-id="aacf7-106">AppDir must be defined as the valid signature of the directory.</span></span> <span data-ttu-id="aacf7-107">Si AppDir n’est pas défini comme une signature valide, AppSearch n’a pas d’emplacement pour rechercher le fichier, par exemple, si la recherche est pour c : \\ MyDir \\MyApp.exe, appdir doit être défini comme c : \\ mydir.</span><span class="sxs-lookup"><span data-stu-id="aacf7-107">If AppDir is not defined as a valid signature, AppSearch does not have a place to find the file, for example, if the search is for c:\\MyDir\\MyApp.exe, AppDir should be defined as c:\\MyDir.</span></span> <span data-ttu-id="aacf7-108">AppDir peut être défini en incluant un enregistrement dans la [table DrLocator](drlocator-table.md), ou par une autre méthode.</span><span class="sxs-lookup"><span data-stu-id="aacf7-108">AppDir might be defined by including a record in the [DrLocator Table](drlocator-table.md), or by some other method.</span></span> <span data-ttu-id="aacf7-109">Aucun enregistrement n’est inclus dans la [table de signatures](signature-table.md) pour la recherche dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="aacf7-109">No record is included in the [Signature Table](signature-table.md) for the directory search.</span></span> <span data-ttu-id="aacf7-110">Pour la recherche de fichiers, répertoriez la signature et le nom de fichier dans la table de signatures.</span><span class="sxs-lookup"><span data-stu-id="aacf7-110">For the file search, list the file signature and name in the Signature Table.</span></span> <span data-ttu-id="aacf7-111">Les champs restants de cet enregistrement peuvent avoir la valeur null pour rechercher n’importe quelle version de MyApp.exe.</span><span class="sxs-lookup"><span data-stu-id="aacf7-111">The remaining fields in this record can be null to search for any version of MyApp.exe.</span></span>

    <span data-ttu-id="aacf7-112">[Table de signature](signature-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="aacf7-112">[Signature Table](signature-table.md) (partial)</span></span>

    

    | <span data-ttu-id="aacf7-113">Signature</span><span class="sxs-lookup"><span data-stu-id="aacf7-113">Signature</span></span>          | <span data-ttu-id="aacf7-114">Nom de fichier</span><span class="sxs-lookup"><span data-stu-id="aacf7-114">File Name</span></span>            |
    |--------------------|----------------------|
    | <span data-ttu-id="aacf7-115">AppFile</span><span class="sxs-lookup"><span data-stu-id="aacf7-115">AppFile</span></span><br/> | <span data-ttu-id="aacf7-116">MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="aacf7-116">MyApp.exe</span></span><br/> |

    

     

2.  <span data-ttu-id="aacf7-117">Utilisez la [table AppSearch](appsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="aacf7-117">Use the [AppSearch Table](appsearch-table.md).</span></span>

    <span data-ttu-id="aacf7-118">Entrez la propriété que le programme d’installation doit définir si le répertoire avec la signature AppDir est installé.</span><span class="sxs-lookup"><span data-stu-id="aacf7-118">Enter the property that the Installer is to set if the directory with the signature AppDir is installed.</span></span> <span data-ttu-id="aacf7-119">Si le programme d’installation détecte que ce répertoire est installé, il définit MYDIR sur le chemin d’accès au répertoire.</span><span class="sxs-lookup"><span data-stu-id="aacf7-119">If the Installer finds this directory is installed, it sets MYDIR to the directory path.</span></span> <span data-ttu-id="aacf7-120">Entrez la propriété que le programme d’installation doit définir si MyApp.exe est installé.</span><span class="sxs-lookup"><span data-stu-id="aacf7-120">Enter the property that the Installer is to set if MyApp.exe is installed.</span></span>

    <span data-ttu-id="aacf7-121">[Table AppSearch](appsearch-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="aacf7-121">[AppSearch Table](appsearch-table.md) (partial)</span></span>

    

    | <span data-ttu-id="aacf7-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="aacf7-122">Property</span></span>         | <span data-ttu-id="aacf7-123">Signature</span><span class="sxs-lookup"><span data-stu-id="aacf7-123">Signature</span></span>          |
    |------------------|--------------------|
    | <span data-ttu-id="aacf7-124">MYDIR</span><span class="sxs-lookup"><span data-stu-id="aacf7-124">MYDIR</span></span><br/> | <span data-ttu-id="aacf7-125">AppDir</span><span class="sxs-lookup"><span data-stu-id="aacf7-125">AppDir</span></span><br/>  |
    | <span data-ttu-id="aacf7-126">MYAPP</span><span class="sxs-lookup"><span data-stu-id="aacf7-126">MYAPP</span></span><br/> | <span data-ttu-id="aacf7-127">AppFile</span><span class="sxs-lookup"><span data-stu-id="aacf7-127">AppFile</span></span><br/> |

    

     

3.  <span data-ttu-id="aacf7-128">Utilisez la [table DrLocator](drlocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="aacf7-128">Use the [DrLocator Table](drlocator-table.md).</span></span>

    <span data-ttu-id="aacf7-129">Entrez dans la colonne parent la signature, AppDir, qui est définie en tant que chemin d’accès du répertoire.</span><span class="sxs-lookup"><span data-stu-id="aacf7-129">Enter in the Parent column the signature, AppDir, that is defined as the path of the directory.</span></span> <span data-ttu-id="aacf7-130">Spécifiez dans la colonne profondeur le nombre de niveaux de sous-répertoires à rechercher dans ce répertoire.</span><span class="sxs-lookup"><span data-stu-id="aacf7-130">Specify in the Depth column the number of subdirectory levels to search in this directory.</span></span> <span data-ttu-id="aacf7-131">AppDir doit être défini comme signature de répertoire.</span><span class="sxs-lookup"><span data-stu-id="aacf7-131">AppDir must be defined as the directory signature.</span></span> <span data-ttu-id="aacf7-132">AppDir peut être défini en incluant un enregistrement comme indiqué ici ou par une autre méthode.</span><span class="sxs-lookup"><span data-stu-id="aacf7-132">AppDir may be defined by including a record as shown here or by another method.</span></span>

    [<span data-ttu-id="aacf7-133">Table DrLocator</span><span class="sxs-lookup"><span data-stu-id="aacf7-133">DrLocator Table</span></span>](drlocator-table.md)

    

    | <span data-ttu-id="aacf7-134">Signature</span><span class="sxs-lookup"><span data-stu-id="aacf7-134">Signature</span></span> | <span data-ttu-id="aacf7-135">Parent</span><span class="sxs-lookup"><span data-stu-id="aacf7-135">Parent</span></span> | <span data-ttu-id="aacf7-136">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="aacf7-136">Path</span></span>      | <span data-ttu-id="aacf7-137">Profondeur</span><span class="sxs-lookup"><span data-stu-id="aacf7-137">Depth</span></span> |
    |-----------|--------|-----------|-------|
    | <span data-ttu-id="aacf7-138">AppDir</span><span class="sxs-lookup"><span data-stu-id="aacf7-138">AppDir</span></span>    |        | <span data-ttu-id="aacf7-139">C : \\ mydir</span><span class="sxs-lookup"><span data-stu-id="aacf7-139">C:\\MyDir</span></span> | <span data-ttu-id="aacf7-140">0</span><span class="sxs-lookup"><span data-stu-id="aacf7-140">0</span></span>     |
    | <span data-ttu-id="aacf7-141">AppFile</span><span class="sxs-lookup"><span data-stu-id="aacf7-141">AppFile</span></span>   | <span data-ttu-id="aacf7-142">AppDir</span><span class="sxs-lookup"><span data-stu-id="aacf7-142">AppDir</span></span> |           | <span data-ttu-id="aacf7-143">0</span><span class="sxs-lookup"><span data-stu-id="aacf7-143">0</span></span>     |

    

     

4.  <span data-ttu-id="aacf7-144">Inclure l’action AppSearch dans la séquence d’action.</span><span class="sxs-lookup"><span data-stu-id="aacf7-144">Include the AppSearch action in the action sequence.</span></span>

    <span data-ttu-id="aacf7-145">Si MyApp.exe est trouvé pour être installé dans AppDir, le programme d’installation définit la propriété MYAPP sur l’emplacement du fichier.</span><span class="sxs-lookup"><span data-stu-id="aacf7-145">If MyApp.exe is found to be installed in AppDir, the Installer sets the property MYAPP to the location of file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aacf7-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aacf7-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aacf7-147">Recherche d’applications, de fichiers, d’entrées de registre ou d’entrées de fichier. ini existants</span><span class="sxs-lookup"><span data-stu-id="aacf7-147">Searching for Existing Applications, Files, Registry Entries or .ini File Entries</span></span>](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
</dt> </dl>

 

 





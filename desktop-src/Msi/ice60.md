---
description: ICE60 valide la table de fichiers d’une base de données Windows Installer.
ms.assetid: 95d9b8b4-0b65-451a-8629-f0b276d6e35d
title: ICE60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26c6f296fd514f582a699a5f839a7e145169e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521838"
---
# <a name="ice60"></a><span data-ttu-id="5e7b9-103">ICE60</span><span class="sxs-lookup"><span data-stu-id="5e7b9-103">ICE60</span></span>

<span data-ttu-id="5e7b9-104">ICE60 vérifie que les fichiers de la [table de fichiers](file-table.md) remplissent les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="5e7b9-104">ICE60 checks that files in the [File table](file-table.md) meet the following condition:</span></span>

-   <span data-ttu-id="5e7b9-105">Si le fichier n’est pas une police et a une version, il doit avoir une langue.</span><span class="sxs-lookup"><span data-stu-id="5e7b9-105">If the file is not a font and has a version, then it must have a language.</span></span>
-   <span data-ttu-id="5e7b9-106">ICE60 vérifie qu’aucun fichier avec version n’est répertorié dans la [table MsiFileHash](msifilehash-table.md).</span><span class="sxs-lookup"><span data-stu-id="5e7b9-106">ICE60 checks that no versioned files are listed in the [MsiFileHash table](msifilehash-table.md).</span></span>

<span data-ttu-id="5e7b9-107">Si vous ne corrigez pas un avertissement signalé par ICE60, il est généralement possible de réinstaller un fichier en cas de réparation d’un produit.</span><span class="sxs-lookup"><span data-stu-id="5e7b9-107">Failure to fix a warning reported by ICE60 generally leads to a file being needlessly reinstalled when a product repair is done.</span></span> <span data-ttu-id="5e7b9-108">Cela est dû au fait que le fichier à installer dans la réparation et le fichier existant sur le disque ont la même version (il s’agit du même fichier) mais des langues différentes.</span><span class="sxs-lookup"><span data-stu-id="5e7b9-108">This happens because the file to be installed in the repair and the existing file on disk have the same version (they are the same file) but different languages.</span></span> <span data-ttu-id="5e7b9-109">La table file indique la langue comme étant null, mais le fichier lui-même a une valeur Language dans la ressource.</span><span class="sxs-lookup"><span data-stu-id="5e7b9-109">The file table lists the language as null, but the file itself has a language value in the resource.</span></span> <span data-ttu-id="5e7b9-110">En fonction des [règles](file-versioning-rules.md)de contrôle de version des fichiers, le programme d’installation privilégie le fichier à installer, de sorte qu’il est recopié inutilement.</span><span class="sxs-lookup"><span data-stu-id="5e7b9-110">Based on the [file versioning rules](file-versioning-rules.md), the installer favors the file to be installed, so it is recopied needlessly.</span></span>

## <a name="result"></a><span data-ttu-id="5e7b9-111">Résultats</span><span class="sxs-lookup"><span data-stu-id="5e7b9-111">Result</span></span>

<span data-ttu-id="5e7b9-112">ICE60 publie un avertissement ou une erreur si un fichier de la [table de fichiers](file-table.md) qui n’est pas une police et a une version n’a pas de langue.</span><span class="sxs-lookup"><span data-stu-id="5e7b9-112">ICE60 posts a warning or an error if a file in the [File table](file-table.md) that is not a font and has a version, does not have a language.</span></span>

<span data-ttu-id="5e7b9-113">ICE60 publie l’erreur suivante si la version d’un fichier figurant dans la table MsiFileHash est gérée.</span><span class="sxs-lookup"><span data-stu-id="5e7b9-113">ICE60 posts the following error if a file listed in the MsiFileHash table is versioned.</span></span>

``` syntax
ERROR: "The file [1] is Versioned. It cannot be hashed"
```

## <a name="example"></a><span data-ttu-id="5e7b9-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="5e7b9-114">Example</span></span>

<span data-ttu-id="5e7b9-115">ICE60 signale l’erreur et l’avertissement suivants pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="5e7b9-115">ICE60 reports the following error and warning for the example shown.</span></span> <span data-ttu-id="5e7b9-116">(Le fichier B est une police ; les autres fichiers ne le sont pas.)</span><span class="sxs-lookup"><span data-stu-id="5e7b9-116">(File B is a font; the other files are not.)</span></span>

``` syntax
WARNING: The file FileE is not a Font, and its version is not a companion file reference. It should have a language specified in the Language column.
```

<span data-ttu-id="5e7b9-117">Filea a une version et une langue ; par conséquent, aucun avertissement ou erreur n’est généré.</span><span class="sxs-lookup"><span data-stu-id="5e7b9-117">FileA has both a version and a language; therefore no warning or error is generated.</span></span>

<span data-ttu-id="5e7b9-118">FileB a une version, mais pas de langue.</span><span class="sxs-lookup"><span data-stu-id="5e7b9-118">FileB has a version but no language.</span></span> <span data-ttu-id="5e7b9-119">Toutefois, aucun avertissement ou erreur n’est généré, car il s’agit d’une police.</span><span class="sxs-lookup"><span data-stu-id="5e7b9-119">No warning or error is generated, however, because it is a font.</span></span>

<span data-ttu-id="5e7b9-120">FileC est une référence complémentaire, il n’est donc pas nécessaire de disposer d’un langage.</span><span class="sxs-lookup"><span data-stu-id="5e7b9-120">FileC is a companion reference, so it does not have to have a language.</span></span> <span data-ttu-id="5e7b9-121">Aucun avertissement ou erreur n’est généré.</span><span class="sxs-lookup"><span data-stu-id="5e7b9-121">No warning or error is generated.</span></span>

<span data-ttu-id="5e7b9-122">Le dépôt n’a pas de version, il n’est donc pas nécessaire de disposer d’une langue.</span><span class="sxs-lookup"><span data-stu-id="5e7b9-122">FileD has no version, so it does not need to have a language.</span></span> <span data-ttu-id="5e7b9-123">Aucun avertissement ou erreur n’est généré.</span><span class="sxs-lookup"><span data-stu-id="5e7b9-123">No warning or error is generated.</span></span>

<span data-ttu-id="5e7b9-124">La version de fichier est sans langue.</span><span class="sxs-lookup"><span data-stu-id="5e7b9-124">FileE has a version but no language.</span></span> <span data-ttu-id="5e7b9-125">Par conséquent, un avertissement est généré.</span><span class="sxs-lookup"><span data-stu-id="5e7b9-125">Therefore a warning is generated.</span></span>

<span data-ttu-id="5e7b9-126">Pour résoudre cet avertissement, ajoutez une langue à fichier.</span><span class="sxs-lookup"><span data-stu-id="5e7b9-126">To fix this warning, add a language to FileE.</span></span>

<span data-ttu-id="5e7b9-127">Chaque fois que cela est possible, les fichiers doivent avoir des valeurs de langue stockées dans la ressource de version.</span><span class="sxs-lookup"><span data-stu-id="5e7b9-127">Files should have language values stored in the version resource whenever possible.</span></span> <span data-ttu-id="5e7b9-128">Si un fichier est indépendant de la langue, utilisez l' [ID](column-data-types.md) de langue 0.</span><span class="sxs-lookup"><span data-stu-id="5e7b9-128">If a file is language neutral, use the [LANGID](column-data-types.md) 0.</span></span>

<span data-ttu-id="5e7b9-129">[Table de fichiers](file-table.md) (fileB est une police ; les autres fichiers ne sont pas.)</span><span class="sxs-lookup"><span data-stu-id="5e7b9-129">[File Table](file-table.md) (FileB is a font; the other files are not.)</span></span>



| <span data-ttu-id="5e7b9-130">Fichier</span><span class="sxs-lookup"><span data-stu-id="5e7b9-130">File</span></span>  | <span data-ttu-id="5e7b9-131">Version</span><span class="sxs-lookup"><span data-stu-id="5e7b9-131">Version</span></span> | <span data-ttu-id="5e7b9-132">Language</span><span class="sxs-lookup"><span data-stu-id="5e7b9-132">Language</span></span> |
|-------|---------|----------|
| <span data-ttu-id="5e7b9-133">Filea</span><span class="sxs-lookup"><span data-stu-id="5e7b9-133">FileA</span></span> | <span data-ttu-id="5e7b9-134">1.0</span><span class="sxs-lookup"><span data-stu-id="5e7b9-134">1.0</span></span>     | <span data-ttu-id="5e7b9-135">1033</span><span class="sxs-lookup"><span data-stu-id="5e7b9-135">1033</span></span>     |
| <span data-ttu-id="5e7b9-136">FileB</span><span class="sxs-lookup"><span data-stu-id="5e7b9-136">FileB</span></span> | <span data-ttu-id="5e7b9-137">1.0</span><span class="sxs-lookup"><span data-stu-id="5e7b9-137">1.0</span></span>     |          |
| <span data-ttu-id="5e7b9-138">FileC</span><span class="sxs-lookup"><span data-stu-id="5e7b9-138">FileC</span></span> | <span data-ttu-id="5e7b9-139">Filea</span><span class="sxs-lookup"><span data-stu-id="5e7b9-139">FileA</span></span>   |          |
| <span data-ttu-id="5e7b9-140">Classer</span><span class="sxs-lookup"><span data-stu-id="5e7b9-140">FileD</span></span> |         |          |
| <span data-ttu-id="5e7b9-141">Fichier</span><span class="sxs-lookup"><span data-stu-id="5e7b9-141">FileE</span></span> | <span data-ttu-id="5e7b9-142">1.0</span><span class="sxs-lookup"><span data-stu-id="5e7b9-142">1.0</span></span>     |          |



 

[<span data-ttu-id="5e7b9-143">Tableau des polices</span><span class="sxs-lookup"><span data-stu-id="5e7b9-143">Font Table</span></span>](font-table.md)



| <span data-ttu-id="5e7b9-144">Fichier</span><span class="sxs-lookup"><span data-stu-id="5e7b9-144">File</span></span>  | <span data-ttu-id="5e7b9-145">FontTitle</span><span class="sxs-lookup"><span data-stu-id="5e7b9-145">FontTitle</span></span>  |
|-------|------------|
| <span data-ttu-id="5e7b9-146">FileB</span><span class="sxs-lookup"><span data-stu-id="5e7b9-146">FileB</span></span> | <span data-ttu-id="5e7b9-147">Titre de la police</span><span class="sxs-lookup"><span data-stu-id="5e7b9-147">Font Title</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="5e7b9-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5e7b9-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e7b9-149">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="5e7b9-149">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




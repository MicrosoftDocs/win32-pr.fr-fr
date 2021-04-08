---
description: Une table de fichiers est requise dans chaque module de fusion et doit avoir un enregistrement pour chaque fichier qui est remis au package d’installation cible par le module de fusion.
ms.assetid: 436933c7-6e5d-4b4e-9147-c60a26871dbe
title: Création de tables de fichier de module de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e2687ed69c1a0362f96db896a5fdf4237ac4681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034406"
---
# <a name="authoring-merge-module-file-tables"></a><span data-ttu-id="a941c-103">Création de tables de fichier de module de fusion</span><span class="sxs-lookup"><span data-stu-id="a941c-103">Authoring Merge Module File Tables</span></span>

<span data-ttu-id="a941c-104">Une [table de fichiers](file-table.md) est requise dans chaque module de fusion et doit avoir un enregistrement pour chaque fichier qui est remis au package d’installation cible par le module de fusion.</span><span class="sxs-lookup"><span data-stu-id="a941c-104">A [File Table](file-table.md) is required in every merge module, and should have a record for each file that is being delivered to the target installation package by the merge module.</span></span> <span data-ttu-id="a941c-105">Lorsque le module de fusion est fusionné dans un fichier. msi, chaque fichier de la table de fichiers du module de fusion est stocké dans un [*fichier CAB*](c-gly.md) dans le fichier. msm.</span><span class="sxs-lookup"><span data-stu-id="a941c-105">When the merge module is merged into a .msi file, every file in the merge module File Table is stored inside a [*cabinet file*](c-gly.md) in the .msm file.</span></span> <span data-ttu-id="a941c-106">Le nom du fichier cab dans un module de fusion est toujours le suivant : MergeModule.CABinet.</span><span class="sxs-lookup"><span data-stu-id="a941c-106">The name of the cabinet in a merge module is always the following: MergeModule.CABinet.</span></span>

<span data-ttu-id="a941c-107">Pour plus d’informations, consultez [génération de fichiers CAB inet MergeModule.CAB](generating-mergemodule-cabinet-cabinet-files.md).</span><span class="sxs-lookup"><span data-stu-id="a941c-107">For more information, see [Generating MergeModule.CABinet Cabinet Files](generating-mergemodule-cabinet-cabinet-files.md).</span></span>

-   <span data-ttu-id="a941c-108">Étant donné que les fichiers d’un module de fusion sont toujours stockés dans un fichier CAB, il n’est pas nécessaire de définir les indicateurs de bits **msidbFileAttributesNoncompressed** ou **msidbFileAttributesCompressed** dans la colonne attributs de la [table file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="a941c-108">Because the files of a merge module are always stored inside a cabinet file, it is not necessary to set the **msidbFileAttributesNoncompressed** or **msidbFileAttributesCompressed** bit flags in the Attributes column of the [File Table](file-table.md).</span></span>
-   <span data-ttu-id="a941c-109">Les noms des fichiers dans MergeModule.CABinet doivent correspondre à la clé primaire de la table de [fichiers](file-table.md)du module de fusion.</span><span class="sxs-lookup"><span data-stu-id="a941c-109">The names of files in MergeModule.CABinet must match the primary key in the merge module's [File Table](file-table.md).</span></span>

    <span data-ttu-id="a941c-110">La colonne de fichier est la clé primaire de la [table de fichiers](file-table.md) et les entrées de ce champ doivent respecter la convention décrite dans [nommage des clés primaires dans les bases de données de module de fusion](naming-primary-keys-in-merge-module-databases.md).</span><span class="sxs-lookup"><span data-stu-id="a941c-110">The File column is the primary key of the [File Table](file-table.md) and the entries in this field must follow the convention that is described in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span>

-   <span data-ttu-id="a941c-111">Les numéros de séquence de fichiers sont spécifiés dans la colonne séquence de la [table file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="a941c-111">File sequence numbers are specified in the Sequence column of the [File Table](file-table.md).</span></span>

    <span data-ttu-id="a941c-112">Les fichiers doivent être répertoriés dans la [table de fichiers](file-table.md) du module de fusion dans l’ordre dans lequel ils sont stockés dans MergeModule.CABinet.</span><span class="sxs-lookup"><span data-stu-id="a941c-112">Files must be listed in the merge module's [File Table](file-table.md) in the same sequence that they are stored in MergeModule.CABinet.</span></span> <span data-ttu-id="a941c-113">Les numéros de séquence des fichiers n’ont pas besoin d’être consécutifs, mais ils doivent suivre la même séquence que les fichiers qui sont stockés dans le fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="a941c-113">The sequence numbers of files do not need to be consecutive, but they must follow the same sequence as the files that are stored inside the cabinet.</span></span> <span data-ttu-id="a941c-114">Par exemple, les premier, deuxième et troisième fichiers stockés dans le fichier CAB peuvent avoir les numéros de séquence 100, 200 et 300.</span><span class="sxs-lookup"><span data-stu-id="a941c-114">For example, the first, second, and third files stored in the cabinet can have the sequence numbers 100, 200, and 300.</span></span>

-   <span data-ttu-id="a941c-115">Le programme d’installation ignore les fichiers supplémentaires inclus dans MergeModule.CABinet qui ne sont pas répertoriés dans la [table de fichiers](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="a941c-115">The Installer skips extra files included in MergeModule.CABinet that are not listed in the [File Table](file-table.md).</span></span>

    <span data-ttu-id="a941c-116">Un fichier CAB peut contenir tous les fichiers nécessaires pour un module de fusion qui prend en charge plusieurs langues à l’aide de transformations.</span><span class="sxs-lookup"><span data-stu-id="a941c-116">One cabinet file can contain all the files necessary for a merge module that supports multiple languages using transforms.</span></span> <span data-ttu-id="a941c-117">Tous les fichiers de langue peuvent recevoir un numéro de séquence unique dans le fichier CAB, puis une transformation peut ajouter ou supprimer des fichiers dans la [table de fichiers](file-table.md) si nécessaire pour une langue spécifique.</span><span class="sxs-lookup"><span data-stu-id="a941c-117">All the language files can be given a unique sequence number in the cabinet, and then a transform can add or remove files from the [File Table](file-table.md) when needed for a specific language.</span></span> <span data-ttu-id="a941c-118">Pour plus d’informations, consultez [création de modules de fusion multilingues](authoring-multiple-language-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="a941c-118">For more information, see [Authoring Multiple Language Merge Modules](authoring-multiple-language-merge-modules.md).</span></span>

<span data-ttu-id="a941c-119">Pour plus d’informations, consultez [table file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="a941c-119">For more information, see [File Table](file-table.md).</span></span>

 

 




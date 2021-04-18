---
description: Le groupe de fichiers des tables contient toutes les tables de Windows Installer liées aux fichiers.
ms.assetid: 8f56328e-ed58-41a1-94b6-266e9c117246
title: Groupe de tables de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2667a1b9fe2bd9d2f8260523e2386bf7751dce8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533796"
---
# <a name="file-tables-group"></a><span data-ttu-id="47a8e-103">Groupe de tables de fichiers</span><span class="sxs-lookup"><span data-stu-id="47a8e-103">File Tables Group</span></span>

![Groupe de tables de fichiers](images/filegrp.png)

<span data-ttu-id="47a8e-105">Pour plus d’informations sur ce diagramme, consultez la [légende diagramme de relation d’entité](entity-relationship-diagram-legend.md).</span><span class="sxs-lookup"><span data-stu-id="47a8e-105">For more information about this diagram, see the [entity relationship diagram legend](entity-relationship-diagram-legend.md).</span></span>

<span data-ttu-id="47a8e-106">Un développeur de packages d’installation doit envisager de remplir le groupe de tables de fichiers de tables après avoir divisé l’application en [composants et fonctionnalités](components-and-features.md) et après avoir rempli le [groupe de tables principales](core-tables-group.md).</span><span class="sxs-lookup"><span data-stu-id="47a8e-106">An installer package developer should consider populating the file table group of tables after breaking the application into [components and features](components-and-features.md) and after populating the [core tables group](core-tables-group.md).</span></span> <span data-ttu-id="47a8e-107">Le groupe de tables file contient tous les fichiers appartenant à l’installation, et la plupart de ces fichiers sont répertoriés dans le [tableau file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="47a8e-107">The file table group contains all of the files belonging to the installation and most of these files are listed in the [File table](file-table.md).</span></span> <span data-ttu-id="47a8e-108">La [table de répertoires](directory-table.md) n’est pas affichée dans la figure, mais elle est étroitement liée au groupe de tables de fichiers.</span><span class="sxs-lookup"><span data-stu-id="47a8e-108">The [Directory table](directory-table.md) is not shown in the figure but is closely related to the file table group.</span></span> <span data-ttu-id="47a8e-109">La table de répertoires fournit la structure de répertoire de l’installation.</span><span class="sxs-lookup"><span data-stu-id="47a8e-109">The Directory table gives the directory structure of the installation.</span></span>

<span data-ttu-id="47a8e-110">Le groupe de fichiers des tables contient toutes les tables liées aux fichiers.</span><span class="sxs-lookup"><span data-stu-id="47a8e-110">The file group of tables contains all of the tables that are related to files.</span></span>

-   <span data-ttu-id="47a8e-111">Le [tableau fichier](file-table.md) répertorie les fichiers appartenant à l’installation.</span><span class="sxs-lookup"><span data-stu-id="47a8e-111">The [File table](file-table.md) lists files belonging to the installation.</span></span> <span data-ttu-id="47a8e-112">Les fichiers qui ne sont pas répertoriés dans le tableau de fichiers incluent les fichiers de disque, qui sont répertoriés dans la table des médias.</span><span class="sxs-lookup"><span data-stu-id="47a8e-112">Files that are not listed in the File table include disk files, which are listed in Media table.</span></span> <span data-ttu-id="47a8e-113">Étant donné que chaque fichier appartient à un composant, la table de fichiers a une clé externe dans la table des composants.</span><span class="sxs-lookup"><span data-stu-id="47a8e-113">Because every file belongs to a component, the File table has an external key into the Component table.</span></span>
-   <span data-ttu-id="47a8e-114">La [table RemoveFile](removefile-table.md) contient une liste de fichiers à supprimer par l' [action RemoveFiles](removefiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="47a8e-114">The [RemoveFile table](removefile-table.md) contains a list of files to be removed by the [RemoveFiles action](removefiles-action.md).</span></span>
-   <span data-ttu-id="47a8e-115">Le [tableau des polices](font-table.md) répertorie les fichiers de polices à inscrire auprès du système.</span><span class="sxs-lookup"><span data-stu-id="47a8e-115">The [Font table](font-table.md) lists font files to be registered with the system.</span></span>
-   <span data-ttu-id="47a8e-116">La [table Selfreg](selfreg-table.md) répertorie les fichiers de module de l’installation qui sont auto-inscrits.</span><span class="sxs-lookup"><span data-stu-id="47a8e-116">The [SelfReg table](selfreg-table.md) lists module files of the installation that are self-registered.</span></span>
-   <span data-ttu-id="47a8e-117">La [table des médias](media-table.md) répertorie le support source et les disques appartenant à l’installation.</span><span class="sxs-lookup"><span data-stu-id="47a8e-117">The [Media table](media-table.md) lists the source media and disks belonging to the installation.</span></span>
-   <span data-ttu-id="47a8e-118">La [table BindImage](bindimage-table.md) répertorie les fichiers qui sont liés aux dll importées par les exécutables.</span><span class="sxs-lookup"><span data-stu-id="47a8e-118">The [BindImage table](bindimage-table.md) lists files that are bound to DLLs imported by executables.</span></span>
-   <span data-ttu-id="47a8e-119">La [table MoveFile](movefile-table.md) spécifie les fichiers qui sont déplacés au cours de l’installation.</span><span class="sxs-lookup"><span data-stu-id="47a8e-119">The [MoveFile table](movefile-table.md) specifies which files are moved during the installation.</span></span>
-   <span data-ttu-id="47a8e-120">La [table DuplicateFile](duplicatefile-table.md) spécifie les fichiers qui sont dupliqués pendant l’installation.</span><span class="sxs-lookup"><span data-stu-id="47a8e-120">The [DuplicateFile table](duplicatefile-table.md) specifies which files are duplicated during the installation.</span></span>
-   <span data-ttu-id="47a8e-121">La [table inifile](inifile-table.md) répertorie les fichiers. ini et les informations que l’application doit définir dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="47a8e-121">The [IniFile table](inifile-table.md) lists the .ini files and the information that the application needs to set in the file.</span></span>
-   <span data-ttu-id="47a8e-122">La [table RemoveIniFile](removeinifile-table.md) contient les informations qu’une application doit supprimer d’un fichier. ini.</span><span class="sxs-lookup"><span data-stu-id="47a8e-122">The [RemoveIniFile table](removeinifile-table.md) contains the information an application needs to delete from a .ini file.</span></span>
-   <span data-ttu-id="47a8e-123">La [table d’environnement](environment-table.md) est utilisée pour définir les valeurs des variables d’environnement.</span><span class="sxs-lookup"><span data-stu-id="47a8e-123">The [Environment table](environment-table.md) is used to set the values of environment variables.</span></span>
-   <span data-ttu-id="47a8e-124">Le [tableau icône](icon-table.md) contient des informations sur les icônes qui sont copiées dans un fichier dans le cadre de l’annonce du produit.</span><span class="sxs-lookup"><span data-stu-id="47a8e-124">The [Icon table](icon-table.md) provides icon information which is copied to a file as a part of product advertisement.</span></span>
-   <span data-ttu-id="47a8e-125">La [table FileSFPCatalog](filesfpcatalog-table.md) associe les fichiers spécifiés aux fichiers de catalogue de protection des fichiers système.</span><span class="sxs-lookup"><span data-stu-id="47a8e-125">The [FileSFPCatalog table](filesfpcatalog-table.md) associates specified files with system file protection catalog files.</span></span>

    <span data-ttu-id="47a8e-126">**Windows Vista, Windows Server 2003 et Windows XP :** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="47a8e-126">**Windows Vista, Windows Server 2003 and Windows XP:** Not supported.</span></span>

-   <span data-ttu-id="47a8e-127">La [table SFPCatalog](sfpcatalog-table.md) contient des catalogues de protection de fichiers système.</span><span class="sxs-lookup"><span data-stu-id="47a8e-127">The [SFPCatalog table](sfpcatalog-table.md) contains system file protection catalogs.</span></span>

    <span data-ttu-id="47a8e-128">**Windows Vista, Windows Server 2003 et Windows XP :** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="47a8e-128">**Windows Vista, Windows Server 2003 and Windows XP:** Not supported.</span></span>

-   <span data-ttu-id="47a8e-129">La [table MsiFileHash](msifilehash-table.md) est utilisée pour stocker un hachage 128 bits d’un fichier source fourni par le package Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="47a8e-129">The [MsiFileHash table](msifilehash-table.md) is used to store a 128-bit hash of a source file provided by the Windows Installer package.</span></span>

 

 




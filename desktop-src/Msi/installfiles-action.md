---
description: L’action InstallFiles copie les fichiers spécifiés dans la table de fichiers du répertoire source vers le répertoire de destination.
ms.assetid: 187ad82f-13f5-4ea3-913c-2ae7561a6ee6
title: Action InstallFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2a0206ec5a64974f27375e175f25ce1888b430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529133"
---
# <a name="installfiles-action"></a><span data-ttu-id="26564-103">Action InstallFiles</span><span class="sxs-lookup"><span data-stu-id="26564-103">InstallFiles Action</span></span>

<span data-ttu-id="26564-104">L’action InstallFiles copie les fichiers spécifiés dans la table de fichiers du répertoire source vers le répertoire de destination.</span><span class="sxs-lookup"><span data-stu-id="26564-104">The InstallFiles action copies files specified in the File table from the source directory to the destination directory.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="26564-105">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="26564-105">Sequence Restrictions</span></span>

<span data-ttu-id="26564-106">L’action InstallFiles doit venir après l’action [InstallValidate](installvalidate-action.md) et avant toute action dépendante d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="26564-106">The InstallFiles action must come after the [InstallValidate](installvalidate-action.md) action and before any file-dependent actions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="26564-107">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="26564-107">ActionData Messages</span></span>



| <span data-ttu-id="26564-108">Champ</span><span class="sxs-lookup"><span data-stu-id="26564-108">Field</span></span> | <span data-ttu-id="26564-109">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="26564-109">Description of action data</span></span>                      |
|-------|-------------------------------------------------|
| <span data-ttu-id="26564-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="26564-110">\[1\]</span></span> | <span data-ttu-id="26564-111">Identificateur du fichier installé.</span><span class="sxs-lookup"><span data-stu-id="26564-111">Identifier of installed file.</span></span>                   |
| <span data-ttu-id="26564-112">\[6\]</span><span class="sxs-lookup"><span data-stu-id="26564-112">\[6\]</span></span> | <span data-ttu-id="26564-113">Taille du fichier installé en octets.</span><span class="sxs-lookup"><span data-stu-id="26564-113">Size of installed file in bytes.</span></span>                |
| <span data-ttu-id="26564-114">\[9\]</span><span class="sxs-lookup"><span data-stu-id="26564-114">\[9\]</span></span> | <span data-ttu-id="26564-115">Identificateur du répertoire contenant le fichier installé.</span><span class="sxs-lookup"><span data-stu-id="26564-115">Identifier of directory holding installed file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="26564-116">Notes</span><span class="sxs-lookup"><span data-stu-id="26564-116">Remarks</span></span>

<span data-ttu-id="26564-117">L’action InstallFiles opère sur les fichiers spécifiés dans la [table de fichiers](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="26564-117">The InstallFiles action operates on files specified in the [File table](file-table.md).</span></span> <span data-ttu-id="26564-118">Chaque fichier est installé en fonction de l’état d’installation du composant associé du fichier dans la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="26564-118">Each file is installed based on the installation state of the file's associated component in the [Component table](component-table.md).</span></span> <span data-ttu-id="26564-119">Seuls les fichiers dont les composants sont résolus à l’état **msiInstallStatelocal** peuvent être copiés.</span><span class="sxs-lookup"><span data-stu-id="26564-119">Only those files whose components are resolved to the **msiInstallStatelocal** state are eligible for copying.</span></span>

<span data-ttu-id="26564-120">L’action InstallFiles implémente les colonnes suivantes de la table de fichiers.</span><span class="sxs-lookup"><span data-stu-id="26564-120">The InstallFiles action implements the following columns of the File table.</span></span>

-   <span data-ttu-id="26564-121">La colonne FileName spécifie le nom du fichier cible.</span><span class="sxs-lookup"><span data-stu-id="26564-121">The FileName column specifies the target file name.</span></span>
-   <span data-ttu-id="26564-122">La colonne version spécifie la version du fichier.</span><span class="sxs-lookup"><span data-stu-id="26564-122">The Version column specifies the file version.</span></span>
-   <span data-ttu-id="26564-123">La colonne attributs spécifie les bits d’indicateur d’attribut de fichier et d’installation.</span><span class="sxs-lookup"><span data-stu-id="26564-123">The Attributes column specifies the file and installation attribute flag bits.</span></span>
-   <span data-ttu-id="26564-124">La colonne file spécifie le jeton de fichier unique.</span><span class="sxs-lookup"><span data-stu-id="26564-124">The File column specifies the unique file token.</span></span>
-   <span data-ttu-id="26564-125">La colonne FileSize spécifie la taille du fichier non compressé en octets.</span><span class="sxs-lookup"><span data-stu-id="26564-125">The FileSize column specifies the uncompressed file size in bytes.</span></span>
-   <span data-ttu-id="26564-126">La colonne Language spécifie l’identificateur de langue du fichier.</span><span class="sxs-lookup"><span data-stu-id="26564-126">The Language column specifies the file language identifier.</span></span>
-   <span data-ttu-id="26564-127">La colonne Sequence spécifie le numéro de séquence sur le support.</span><span class="sxs-lookup"><span data-stu-id="26564-127">The Sequence column specifies the sequence number on media.</span></span>

<span data-ttu-id="26564-128">L’action InstallFiles implémente les colonnes suivantes de la table des composants.</span><span class="sxs-lookup"><span data-stu-id="26564-128">The InstallFiles action implements the following columns of the Component table.</span></span>

-   <span data-ttu-id="26564-129">La \_ colonne Directory spécifie une référence à un élément de [table de répertoire](directory-table.md) .</span><span class="sxs-lookup"><span data-stu-id="26564-129">The Directory\_ column specifies a reference to a [Directory table](directory-table.md) item.</span></span>
-   <span data-ttu-id="26564-130">La colonne composant spécifie un nom unique pour l’élément de composant.</span><span class="sxs-lookup"><span data-stu-id="26564-130">The Component column specifies a unique name for the component item.</span></span>

<span data-ttu-id="26564-131">Le fichier spécifié est copié uniquement si l’une des conditions suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="26564-131">The specified file is copied only if one of the following is true:</span></span>

-   <span data-ttu-id="26564-132">Le fichier n’est pas installé actuellement sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="26564-132">The file is not currently installed on the local computer.</span></span>
-   <span data-ttu-id="26564-133">Le fichier se trouve sur l’ordinateur local, mais son numéro de version est inférieur à celui du fichier figurant dans la [table de fichiers](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="26564-133">The file is on the local computer but has a lower version number than the file in the [File table](file-table.md).</span></span>
-   <span data-ttu-id="26564-134">Le fichier se trouve sur l’ordinateur local, mais il n’y a aucun numéro de version associé.</span><span class="sxs-lookup"><span data-stu-id="26564-134">The file is on the local computer, but there is no associated version number.</span></span>

<span data-ttu-id="26564-135">Le répertoire source de chaque fichier à copier est déterminé par le sourceMode, qui à son tour dépend de la valeur dans la colonne Cabinet de la table multimédia.</span><span class="sxs-lookup"><span data-stu-id="26564-135">The source directory for each file to be copied is determined by the sourceMode, which in turn depends on the value in the Cabinet column of the Media table.</span></span> <span data-ttu-id="26564-136">Pour une présentation complète du mode Source, consultez la [table Media](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="26564-136">For a full discussion of the source mode, see the [Media table](media-table.md).</span></span>

<span data-ttu-id="26564-137">Si le répertoire source d’un fichier à copier réside sur un support amovible, tel qu’une disquette ou un CD-ROM, l’action InstallFiles vérifie que le média source approprié est inséré avant de tenter de copier le fichier.</span><span class="sxs-lookup"><span data-stu-id="26564-137">If the source directory for a file to be copied resides on removable media such as a floppy disk or CD-ROM, the InstallFiles action verifies that the proper source media is inserted before attempting to copy the file.</span></span> <span data-ttu-id="26564-138">InstallFiles recherche des médias du même type amovible avec un nom de [*volume*](v-gly.md) qui correspond à la valeur spécifiée dans la colonne VolumeLabel de la table multimédia.</span><span class="sxs-lookup"><span data-stu-id="26564-138">The InstallFiles searches for media of the same removable type with a [*volume*](v-gly.md) label that matches the value given in the VolumeLabel column of the Media table.</span></span> <span data-ttu-id="26564-139">Si un volume monté correspondant est trouvé, le processus de copie de fichiers se poursuit.</span><span class="sxs-lookup"><span data-stu-id="26564-139">If a matching mounted volume is found, the file copying process proceeds.</span></span> <span data-ttu-id="26564-140">Si aucune correspondance n’est trouvée, une boîte de dialogue demande à l’utilisateur d’insérer le média approprié.</span><span class="sxs-lookup"><span data-stu-id="26564-140">If no match is found, a dialog box requests that the user to insert the proper media.</span></span> <span data-ttu-id="26564-141">Dans ce cas, la boîte de dialogue utilise le nom du support trouvé dans la colonne DiskPrompt de la table Media dans le cadre de l’invite.</span><span class="sxs-lookup"><span data-stu-id="26564-141">In this case, the dialog box uses the media name found in the DiskPrompt column of the Media table as part of the prompt.</span></span>

<span data-ttu-id="26564-142">ATTENTION : l’action InstallFiles peut supprimer un fichier d’origine sans le remplacer.</span><span class="sxs-lookup"><span data-stu-id="26564-142">Caution must be exercised because the InstallFiles action can delete an original file and not replace it.</span></span> <span data-ttu-id="26564-143">Cela se produit lorsque l’action InstallFiles rencontre une erreur lors du remplacement d’un fichier plus ancien et que l’utilisateur choisit d’ignorer l’erreur.</span><span class="sxs-lookup"><span data-stu-id="26564-143">This occurs when the InstallFiles action experiences an error while replacing an older file and the user chooses to ignore the error.</span></span> <span data-ttu-id="26564-144">Le comportement par défaut du programme d’installation consiste à supprimer un ancien fichier avant de vous assurer que le nouveau fichier est correctement copié.</span><span class="sxs-lookup"><span data-stu-id="26564-144">The default behavior of installer is to delete an old file before ensuring the new file is copied correctly.</span></span>

<span data-ttu-id="26564-145">Pour connaître les règles de contrôle de version des fichiers utilisées par le programme d’installation, consultez règles de contrôle de [version de fichier](file-versioning-rules.md).</span><span class="sxs-lookup"><span data-stu-id="26564-145">For the file versioning rules used by the installer, see [File Versioning Rules](file-versioning-rules.md).</span></span>

 

 




---
description: Le hachage de fichier est disponible avec Windows Installer. Pour plus d’informations, consultez MsiGetFileHash et la table MsiFileHash. La table MsiFileHash peut uniquement être utilisée avec des fichiers sans version.
ms.assetid: 608859ac-6640-4c28-b4f0-34ab36d804d7
title: Aucun fichier n’a une version avec contrôle de hachage de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 415019838ac29418b13b513b393a18af2131510f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528173"
---
# <a name="neither-file-has-a-version-with-file-hash-check"></a><span data-ttu-id="dcd66-105">Aucun fichier n’a une version avec contrôle de hachage de fichier</span><span class="sxs-lookup"><span data-stu-id="dcd66-105">Neither File Has a Version with File Hash Check</span></span>

<span data-ttu-id="dcd66-106">Le hachage de fichier est disponible avec Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="dcd66-106">File hashing is available with Windows Installer.</span></span> <span data-ttu-id="dcd66-107">Pour plus d’informations, consultez [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) et la [table MsiFileHash](msifilehash-table.md).</span><span class="sxs-lookup"><span data-stu-id="dcd66-107">For more information, see [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) and the [MsiFileHash table](msifilehash-table.md).</span></span> <span data-ttu-id="dcd66-108">La table MsiFileHash peut uniquement être utilisée avec des fichiers sans version.</span><span class="sxs-lookup"><span data-stu-id="dcd66-108">The MsiFileHash table can only be used with unversioned files.</span></span>

<span data-ttu-id="dcd66-109">Si le fichier de clé d’un composant en cours d’installation (Copy-A) porte le même nom qu’un fichier déjà installé à l’emplacement cible (Copy-B), le programme d’installation compare le numéro de version, la date et la langue des deux fichiers.</span><span class="sxs-lookup"><span data-stu-id="dcd66-109">If the key file of a component being installed (copy-A) has the same name as a file already installed in the target location (copy-B), the installer compares the version number, date, and language of the two files.</span></span>

<span data-ttu-id="dcd66-110">Si aucun fichier n’a un numéro de version, le programme d’installation utilise la logique illustrée par le diagramme de fluide suivant pour déterminer s’il faut remplacer tous les fichiers installés appartenant au composant.</span><span class="sxs-lookup"><span data-stu-id="dcd66-110">If neither file has a version number, the installer uses the logic illustrated by the following flow diagram to determine whether to replace all of the installed files belonging to the component.</span></span> <span data-ttu-id="dcd66-111">Étant donné que le programme d’installation installe uniquement les composants entiers, si le fichier de clé installé est remplacé, tous les fichiers du composant sont remplacés.</span><span class="sxs-lookup"><span data-stu-id="dcd66-111">Because the installer only installs entire components, if the installed key file is replaced then, all of the component's files are replaced.</span></span>

<span data-ttu-id="dcd66-112">Notez que ce diagramme illustre les règles de contrôle de [version de fichier](file-versioning-rules.md)par défaut, qui peuvent être remplacées en définissant la propriété [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="dcd66-112">Note that this diagram illustrates the default [File Versioning Rules](file-versioning-rules.md), which can be overridden by setting the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> <span data-ttu-id="dcd66-113">La valeur par défaut de la propriété **REINSTALLMODE** est « omus ».</span><span class="sxs-lookup"><span data-stu-id="dcd66-113">The default value of the **REINSTALLMODE** property is "omus".</span></span>

![règles de contrôle de version des fichiers par défaut en cas de substitution par le paramètre de propriété REINSTALLMODE](images/waiflow2b.png)

<span data-ttu-id="dcd66-115">Consultez les exemples de contrôle de version de fichier par défaut lors du [remplacement de fichiers existants](replacing-existing-files.md).</span><span class="sxs-lookup"><span data-stu-id="dcd66-115">See the examples of default file versioning in [Replacing Existing Files](replacing-existing-files.md).</span></span>

-   [<span data-ttu-id="dcd66-116">Les deux fichiers ont une version</span><span class="sxs-lookup"><span data-stu-id="dcd66-116">Both Files Have a Version</span></span>](both-files-have-a-version.md)
-   [<span data-ttu-id="dcd66-117">Aucun fichier n’a une version</span><span class="sxs-lookup"><span data-stu-id="dcd66-117">Neither File Has a Version</span></span>](neither-file-has-a-version.md)
-   [<span data-ttu-id="dcd66-118">Un fichier a une version</span><span class="sxs-lookup"><span data-stu-id="dcd66-118">One File Has a Version</span></span>](one-file-has-a-version.md)

 

 




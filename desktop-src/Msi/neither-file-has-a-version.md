---
description: Si aucun fichier n’a un numéro de version, le Windows Installer utilise la logique illustrée par le diagramme de fluide suivant pour déterminer s’il faut remplacer tous les fichiers installés appartenant au composant.
ms.assetid: 82cb0d96-f49f-408e-a8c6-a0d1ee9af8c7
title: Aucun fichier n’a une version
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5360bb7b6b4deda54156006073f353ab65ab2b2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553405"
---
# <a name="neither-file-has-a-version"></a><span data-ttu-id="40f24-103">Aucun fichier n’a une version</span><span class="sxs-lookup"><span data-stu-id="40f24-103">Neither File Has a Version</span></span>

<span data-ttu-id="40f24-104">Si le fichier de clé d’un composant en cours d’installation (Copy-A) porte le même nom qu’un fichier déjà installé à l’emplacement cible (Copy-B), le programme d’installation compare le numéro de version, la date et la langue des deux fichiers.</span><span class="sxs-lookup"><span data-stu-id="40f24-104">If the key file of a component being installed (copy-A) has the same name as a file already installed in the target location (copy-B), the installer compares the version number, date, and language of the two files.</span></span>

<span data-ttu-id="40f24-105">Si aucun fichier n’a un numéro de version, le programme d’installation utilise la logique illustrée par le diagramme de fluide suivant pour déterminer s’il faut remplacer tous les fichiers installés appartenant au composant.</span><span class="sxs-lookup"><span data-stu-id="40f24-105">If neither file has a version number, the installer uses the logic illustrated by the following flow diagram to determine whether to replace all of the installed files belonging to the component.</span></span> <span data-ttu-id="40f24-106">Étant donné que le programme d’installation installe uniquement les composants entiers, si le fichier de clé installé est remplacé, tous les fichiers du composant sont remplacés.</span><span class="sxs-lookup"><span data-stu-id="40f24-106">Because the installer only installs entire components, if the installed key file is replaced, then all of the component's files are replaced.</span></span>

<span data-ttu-id="40f24-107">Notez que ce diagramme illustre les règles de contrôle de [version de fichier](file-versioning-rules.md)par défaut, qui peuvent être remplacées en définissant la propriété [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="40f24-107">Note that this diagram illustrates the default [File Versioning Rules](file-versioning-rules.md), which can be overridden by setting the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> <span data-ttu-id="40f24-108">La valeur par défaut de la propriété **REINSTALLMODE** est « omus ».</span><span class="sxs-lookup"><span data-stu-id="40f24-108">The default value of the **REINSTALLMODE** property is "omus".</span></span>

![règles de contrôle de version des fichiers par défaut lorsque aucun fichier ne possède un numéro de version](images/waiflow2.png)

<span data-ttu-id="40f24-110">Consultez les exemples de contrôle de version de fichier par défaut lors du [remplacement de fichiers existants](replacing-existing-files.md).</span><span class="sxs-lookup"><span data-stu-id="40f24-110">See the examples of default file versioning in [Replacing Existing Files](replacing-existing-files.md).</span></span>

-   [<span data-ttu-id="40f24-111">Les deux fichiers ont une version</span><span class="sxs-lookup"><span data-stu-id="40f24-111">Both Files Have a Version</span></span>](both-files-have-a-version.md)
-   [<span data-ttu-id="40f24-112">Aucun fichier n’a une version avec contrôle de hachage de fichier</span><span class="sxs-lookup"><span data-stu-id="40f24-112">Neither File Has a Version with File Hash Check</span></span>](neither-file-has-a-version-with-file-hash-check.md)
-   [<span data-ttu-id="40f24-113">Un fichier a une version</span><span class="sxs-lookup"><span data-stu-id="40f24-113">One File Has a Version</span></span>](one-file-has-a-version.md)

 

 




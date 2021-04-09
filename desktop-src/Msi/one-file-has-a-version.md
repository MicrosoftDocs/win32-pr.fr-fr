---
description: Si un seul des fichiers a un numéro de version, le Windows Installer utilise la logique illustrée par le diagramme de fluide suivant pour déterminer s’il faut remplacer tous les fichiers installés appartenant au composant.
ms.assetid: 1eda5521-6e23-49b8-9870-f5370def487e
title: Un fichier a une version
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417060119f8b13b1545161faa80552c79e8ca9aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114167"
---
# <a name="one-file-has-a-version"></a><span data-ttu-id="91b90-103">Un fichier a une version</span><span class="sxs-lookup"><span data-stu-id="91b90-103">One File Has a Version</span></span>

<span data-ttu-id="91b90-104">Si le fichier de clé d’un composant en cours d’installation (Copy-A) porte le même nom qu’un fichier déjà installé à l’emplacement cible (Copy-B), le programme d’installation compare le numéro de version, la date et la langue des deux fichiers.</span><span class="sxs-lookup"><span data-stu-id="91b90-104">If the key file of a component being installed (copy-A) has the same name as a file already installed in the target location (copy-B), the installer compares the version number, date, and language of the two files.</span></span>

<span data-ttu-id="91b90-105">Si un seul des fichiers a un numéro de version, le programme d’installation utilise la logique illustrée par le diagramme de déroulement suivant pour déterminer s’il faut remplacer tous les fichiers installés appartenant au composant.</span><span class="sxs-lookup"><span data-stu-id="91b90-105">If only one of the files has a version number, the installer uses the logic illustrated by the following flow diagram to determine whether to replace all of the installed files belonging to the component.</span></span> <span data-ttu-id="91b90-106">Étant donné que le programme d’installation installe uniquement les composants entiers, si le fichier de clé installé est remplacé, tous les fichiers du composant sont remplacés.</span><span class="sxs-lookup"><span data-stu-id="91b90-106">Because the installer only installs entire components, if the installed key file is replaced, then all of the component's files are replaced.</span></span>

<span data-ttu-id="91b90-107">Notez que ce diagramme illustre les règles de contrôle de [version de fichier](file-versioning-rules.md)par défaut, qui peuvent être remplacées en définissant la propriété [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="91b90-107">Note that this diagram illustrates the default [File Versioning Rules](file-versioning-rules.md), which can be overridden by setting the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> <span data-ttu-id="91b90-108">La valeur par défaut de la propriété **REINSTALLMODE** est « omus ».</span><span class="sxs-lookup"><span data-stu-id="91b90-108">The default value of the **REINSTALLMODE** property is "omus".</span></span>

![règles de contrôle de version de fichier par défaut lorsqu’un seul fichier a un numéro de version](images/waiflow3.png)

<span data-ttu-id="91b90-110">Consultez les exemples de contrôle de version de fichier par défaut lors du [remplacement de fichiers existants](replacing-existing-files.md).</span><span class="sxs-lookup"><span data-stu-id="91b90-110">See the examples of default file versioning in [Replacing Existing Files](replacing-existing-files.md).</span></span>

-   [<span data-ttu-id="91b90-111">Les deux fichiers ont une version</span><span class="sxs-lookup"><span data-stu-id="91b90-111">Both Files Have a Version</span></span>](both-files-have-a-version.md)
-   [<span data-ttu-id="91b90-112">Aucun fichier n’a une version</span><span class="sxs-lookup"><span data-stu-id="91b90-112">Neither File Has a Version</span></span>](neither-file-has-a-version.md)
-   [<span data-ttu-id="91b90-113">Aucun fichier n’a une version avec contrôle de hachage de fichier</span><span class="sxs-lookup"><span data-stu-id="91b90-113">Neither File Has a Version with File Hash Check</span></span>](neither-file-has-a-version-with-file-hash-check.md)

 

 




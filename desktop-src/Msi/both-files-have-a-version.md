---
description: Si les deux fichiers ont un numéro de version, le Windows Installer utilise la logique illustrée par le diagramme de fluide suivant pour déterminer s’il faut remplacer tous les fichiers installés appartenant au composant.
ms.assetid: c4c8a23b-e1c2-4c96-b708-7cbcbcab4cd4
title: Les deux fichiers ont une version
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb52c7333e5455d40475c9f845643535b271d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864429"
---
# <a name="both-files-have-a-version"></a><span data-ttu-id="05462-103">Les deux fichiers ont une version</span><span class="sxs-lookup"><span data-stu-id="05462-103">Both Files Have a Version</span></span>

<span data-ttu-id="05462-104">Si le fichier de clé d’un composant en cours d’installation (Copy-A) porte le même nom qu’un fichier déjà installé à l’emplacement cible (Copy-B), le programme d’installation compare le numéro de version et la langue des deux fichiers.</span><span class="sxs-lookup"><span data-stu-id="05462-104">If the key file of a component being installed (copy-A) has the same name as a file already installed in the target location (copy-B), the installer compares the version number and language of the two files.</span></span>

<span data-ttu-id="05462-105">Si les deux fichiers ont un numéro de version, le programme d’installation utilise la logique illustrée par le diagramme de fluide suivant pour déterminer s’il faut remplacer tous les fichiers installés appartenant au composant.</span><span class="sxs-lookup"><span data-stu-id="05462-105">If both files have a version number, the installer uses the logic illustrated by the following flow diagram to determine whether to replace all of the installed files belonging to the component.</span></span> <span data-ttu-id="05462-106">Étant donné que le programme d’installation installe uniquement les composants entiers, si le fichier de clé installé est remplacé, tous les fichiers du composant sont remplacés.</span><span class="sxs-lookup"><span data-stu-id="05462-106">Because the installer only installs entire components, if the installed key file is replaced then all of the component's files are replaced.</span></span>

<span data-ttu-id="05462-107">Notez que ce diagramme illustre les règles de contrôle de [version de fichier](file-versioning-rules.md)par défaut, qui peuvent être remplacées en définissant la propriété [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="05462-107">Note that this diagram illustrates the default [File Versioning Rules](file-versioning-rules.md), which can be overridden by setting the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> <span data-ttu-id="05462-108">La valeur par défaut de la propriété **REINSTALLMODE** est « omus ».</span><span class="sxs-lookup"><span data-stu-id="05462-108">The default value of the **REINSTALLMODE** property is "omus".</span></span>

![règles de contrôle de version des fichiers par défaut lorsque les deux fichiers portent le même nom ou le même numéro de version](images/waiflow1.png)

<span data-ttu-id="05462-110">Le diagramme précédent peut également être utilisé avec des fichiers sans langue spécifiée.</span><span class="sxs-lookup"><span data-stu-id="05462-110">The previous diagram can also be used with files with no language specified.</span></span> <span data-ttu-id="05462-111">Si Copy-a a un langage spécifié et que Copy-B n’a pas de langue spécifiée, Copy-B est remplacé par Copy-A.</span><span class="sxs-lookup"><span data-stu-id="05462-111">If copy-A has a specified language and copy-B has no specified language, copy-B is replaced with copy-A.</span></span> <span data-ttu-id="05462-112">Si Copy-A et Copy-B n’ont aucune langue spécifiée, Copy-B n’est pas remplacé.</span><span class="sxs-lookup"><span data-stu-id="05462-112">If copy-A and copy-B both have no language specified, then copy-B is not replaced.</span></span>

<span data-ttu-id="05462-113">Consultez des exemples de contrôle de version de fichier par défaut lors du [remplacement de fichiers existants](replacing-existing-files.md).</span><span class="sxs-lookup"><span data-stu-id="05462-113">See examples of default file versioning in [Replacing Existing Files](replacing-existing-files.md).</span></span>

-   [<span data-ttu-id="05462-114">Aucun fichier n’a une version</span><span class="sxs-lookup"><span data-stu-id="05462-114">Neither File Has a Version</span></span>](neither-file-has-a-version.md)
-   [<span data-ttu-id="05462-115">Aucun fichier n’a une version avec contrôle de hachage de fichier</span><span class="sxs-lookup"><span data-stu-id="05462-115">Neither File Has a Version with File Hash Check</span></span>](neither-file-has-a-version-with-file-hash-check.md)
-   [<span data-ttu-id="05462-116">Un fichier a une version</span><span class="sxs-lookup"><span data-stu-id="05462-116">One File Has a Version</span></span>](one-file-has-a-version.md)

 

 



